# How to setup Character Options

## Creating an Options Page

With Codex, you are able to add an options page, selectable from the character screen when selecting your character, or when viewing your character's Codex page. The following Codex.gd example adds one of each option type to the character's options page:

```gdscript
extends Node

func register(codex):
    pass
    ### register function is NOT required to use options


func setup_options(options, params):
	options.add_label("Hello World")
	
    options.add_seperator()
    
    ### for all options other than label and seperator:
    ### the first input indicates the option id
    ### the second input indicates the options displayed label text
    
	options.add_toggle("toggle_id", "Toggle Label")
	options.add_textline("text_id", "Textline Label")
    options.add_number("number_id", "Number Label")
    options.add_slider("slider_id", "Slider Label")
    options.add_color("color_id", "Color Label")
    
	var dropdown = options.add_dropdown("dropdown_id", "Dropdown Label")
	dropdown.add_seperator()
	dropdown.add_item("Value One")
	dropdown.add_seperator("With Text")
    dropdown.add_item("Value Two", "two") ### will be displayed as "Value Two", but saved as "two"
    dropdown.add_item("Value Three") ### will be displayed and saved as "Value Three"
```

``options`` will be a reference to a [``CharOptionsPage``](codex_mod/class_ref/CharOptionsPage.md#charoptionspage) associated with your character.

## Option Defaults

You may also provide each option with a default value, and optional parameters
    
```gdscript
func setup_options(options, params):
	options.add_seperator("Advanced Options")
    
    options.add_label("The following options [u]have defaults and optional parameters[/u]")
    
	options.add_toggle("toggle_a", "Hello Toggle", true, {
        "group": "button_group"
    })
	options.add_toggle("toggle_b", "Goodbye Toggle", false, {
        "group": "button_group"
    })
	options.add_textline("text", "Hello Textline", "Deafult", {
		"secret": true,
		"max_length": 10,
		"placeholder_text": "placeholder",
	})
    options.add_number("number", "Hello Number", 10, {
		"min_value": -32,
		"max_value": 32,
		"step": 1,
		"rounded": true,
	})
    options.add_slider("slider", "Hello Slider", 20, {
		"min_value": -32,
		"max_value": 32,
		"step": 1,
		"rounded": true,
	})
    options.add_color("color", "Hello Color", "00C0FF")
    
	var other_dropdown = options.add_dropdown("dropdown", "Hello Dropdown", "a")
	other_dropdown.add_item("a")
	other_dropdown.add_item("b")
	other_dropdown.add_item("c")
```

## Using Option Data

You may access your characters stored option values via [``load_all_char_options``](codex_mod/class_ref/CharCodexLibrary#func_load_all_char_options), like this example:
```gdscript
    var codex_lib = get_node_or_null("/root/CharCodexLibrary")
    if is_instance_valid(codex_lib):
        var options_data = codex_lib.load_all_char_options(self)
        ### your code here
```

!> The above code, when used in your Fighter script (or a CharacterState with ``host`` instead of ``self``), will be **client-side**, and **the effect will only be shown to the current player of the character, and may cause multiplayer desyncs.**

**However**, Codex offers a method to sync data in multiplayer via modifying style data.  To set this up, you will be required to add [``modify_style_data``](codex_mod/class_ref/Codex.gd#func_modify_style_data) to your Codex.gd file

```gdscript
extends Node

func setup_options(options, params):
    options.add_toggle("alt_skin", "Use Alternate Skin")
    options.add_toggle("alt_intro", "Use Alternate Intro", true)


func modify_style_data(style, params):
    var codex_lib = params.codex_library
    var char_path = params.char_path
    var options_data = codex_lib.load_all_char_options(char_path)
    
    style.use_alternate_skin = options_data.get("alt_skin", false)  ### false will be the default if alt_skin is not set
    style.use_alternate_intro = options_data.get("alt_intro", true)  ### true will be the default if alt_intro is not set
```

You will then need to check for the modifications you added to the style, in your Fighter.  You can do this by either overriding your Fighter's [``apply_style``](class_ref/Fighter#func_apply_style) function, or checking their [``applied_style``](class_ref/Fighter#prop_applied_style) variable.

```gdscript
extends Fighter

var options_applied = false
var using_skin_two = false
var using_intro_two = false

func apply_style(style):
    .apply_style(style)
    if style != null:
        ### apply_style is called every frame, a variable like this makes sure options are only applied once
        if options_applied == false:
            options_applied = true 
            using_skin_two = style.get("use_alternate_skin", false)
            using_intro_two = style.get("use_alternate_intro", true)
```

Alternatively, checking applied_style, in a CharacterState

```
extends CharacterState

func _frame_0():
    if host.applied_style != null:
        if host.applied_style.get("use_alternate_intro", false):
            return "OtherIntro"
```

!> **Note:** the input of apply_style, and the applied_style variable, may both be null, or may not contain your modifications if the player does not have Codex installed, thus why the above examples check for both of these cases.

!> The above setup also allows Codex to remain **optional**, and doesn't require the opponent to install Codex either, as the data is stored and synced through the style.  If you wish for your character to require Options, consider adding "tri_char_codex" to the requirements of your character's _metadata, and mark your Steam Workshop page as requiring Character Codex Library.

## Unlockable Options

setup_options is called each time the character's options page is made to appear.  As such, you can setup dynamically unlockable options, such as requiring certain character achievements, like this example:

```gdscript
extends Node


func setup_achievements(list):
    list.set_title("unlock_skin", "Unlocked Alt Skin")
    list.set_desc("unlock_skin", "Required to use the alternate skin of this character")


func setup_options(options, params):
    var codex_lib = params.codex_library
    var char_path = params.char_path
    var achievements_list = codex_lib.get_achievement_list(char_path)
    
    if achievements_list.is_unlocked("unlock_skin"):
        options.add_toggle("use_skin", "Use Unlockable Skin")

    
func modify_style_data(style, params):
    var codex_lib = params.codex_library
    var char_path = params.char_path
    var options_data = codex_lib.load_all_char_options(char_path)
    
    style.alt_skin = options_data.get("use_skin", false)  ### false will be the default if use_skin is not set
```