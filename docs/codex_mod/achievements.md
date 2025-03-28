# How to setup Character Achievements

## Creating Achievements

Codex allows for you to give your characters unlockable achievements.  To setup achievements for your character, you may start with the following example code for your Codex.gd file:

```gdscript
extends Node

func register(codex):
    pass
    ### register function is NOT required to use achievements


func setup_achievements(list):
    list.set_title("test_cheivo", "Achievement 1")
    list.set_desc("test_cheivo", "Description Here")
    
    list.set_title("custom_chievo", "Achievement 2")
    list.set_desc("custom_chievo", "Description Here")
    
    list.set_title("any_id_here", "Achievement 3")
    list.set_desc("any_id_here", "Description Here")
```

``list`` will be a reference to a [``CodexAchievementList``](codex_mod/class_ref/CodexAchievementList.md#codexachievementlist) object associated with your character.

## Unlocking Achievements

In your character script, you can call ``CharCodexLibrary.unlock_achievement()`` with a reference to your fighter, and the achievement_id you wish to unlock.  Codex will take care of making sure the current player is the one in control of the character and not the opponent.

From a CharacterState script, that would look like this:
```gdscript
extends CharacterState

func _frame_0():
	var codex_lib = get_node_or_null("/root/CharCodexLibrary")
	if is_instance_valid(codex_lib):
        codex_lib.unlock_achievement(host, "test_cheivo")
```

From a Fighter script, that would look like this:
```gdscript
extends Fighter

func unlock_test():
	var codex_lib = get_node_or_null("/root/CharCodexLibrary")
	if is_instance_valid(codex_lib):
        codex_lib.unlock_achievement(self, "test_cheivo")
```

During testing, you may choose to relock achievements with the following function:
```gdscript
    codex_lib.relock_achievement(host, "hustle_five")
```

## Achievement Icons

By default, Codex comes with 2 icons for each achievement to display, one when locked and the other when unlocked.  You may instead choose to provide each achievement with it's own icon to display when unlocked like so:

```gdscript
func setup_achievements(list):
    list.set_title("test_cheivo", "Achievement 1")
    list.set_desc("test_cheivo", "Description Here")
    list.set_icon("test_cheivo", "res://YourMod/Chievos/Icon1.png")
    list.set_locked_icon("test_cheivo", "res://YourMod/Chievos/Locked.png")
```

Or you can setup an icon to use for your whole character.
```gdscript
func setup_achievements(list):
    list.default_locked_icon = "res://YourMod/Chievos/Locked.png"
    list.default_unlocked_icon = "res://YourMod/Chievos/Unlocked.png"
    
    list.set_title("test_cheivo", "Achievement 1")
    list.set_desc("test_cheivo", "Description Here")
```

You can mix and match, giving your character a character-wide locked icon while giving each achievement an unlocked icon
```gdscript
func setup_achievements(list):
    list.default_locked_icon = "res://YourMod/Chievos/Locked.png"
    
    list.set_title("test_cheivo", "Achievement 1")
    list.set_desc("test_cheivo", "Description Here")
    list.set_icon("test_cheivo", "res://YourMod/Chievos/Icon1.png")
```

Each are optional, any icon you don't provide will default to Codex's default trophy icons.

## Secret Achievements

You may choose to mark some achievements as secret achievements.  Secret achievements will not be displayed until unlocked, and will not count for 100% completion for your character.
```gdscript
func setup_achievements(list):
    list.default_locked_icon = "res://YourMod/Chievos/Locked.png"
    
    list.set_title("test_cheivo", "Achievement 1")
    list.set_desc("test_cheivo", "Description Here")
    list.set_icon("test_cheivo", "res://YourMod/Chievos/Icon1.png")
    list.mark_secret("test_chievo")
```

## Counters

Each achievement may be assigned a counter to keep track of how many times a player does an action.
```gdscript
func setup_achievements(list):
    list.default_locked_icon = "res://YourMod/Chievos/Locked.png"
    
    list.set_title("hustle_five", "Hustle 5 Times")
    list.set_desc("hustle_five", "You know you want to")
    list.set_icon("hustle_five", "res://YourMod/Chievos/Hustle.png")
    list.assign_counter("hustle_five", "hustles", 5)
    ### "hustle_five" is the achievement_id
    ### "hustles" is the counter_id
    ### 5 is the target value
```

This will NOT automatically unlock the achievement, in case you wish to make an achievement with multiple conditions, but it can be given a target value that can be checked before unlocking it.
```gdscript
extends CharacterState

func _frame_0():
	var codex_lib = get_node_or_null("/root/CharCodexLibrary")
	if is_instance_valid(codex_lib):
		codex_lib.increment_counter(host, "hustles")
		if codex_lib.achievement_target_met(host, "hustle_five"):
			codex_lib.unlock_achievement(host, "hustle_five")
```

You may also increment a counter by a custom amount...
```gdscript
    codex_lib.increment_counter(host, "hustles_times_two", 2)
```

...Or set the a counter to a specific value...
```gdscript
    codex_lib.set_counter(host, "hustle_used", 1337)
```

The counter target is also optional, and can be set to -1 or left out, which will cause the achievement to be displayed with no target.

## Alternate Setup

If desired or more convenient, the following function can be used with a Dictionary instead of the previously stated setup functions:
```
func setup_achievements(list):
    list.define("defined_chievo", {
        "title": "Title Here",
        "desc": "Description Here",
        "icon": "res://YourMod/IconHere.png",
        "secret": false,
        "counter_id ": "counter",
        "counter_target ": -1,
    })
```

Each key is optional and can be left out.

## Advanced Achievement Automation

By default, Codex does not parse your character file to setup achievements, for performance reasons.  If you need access to an instace of your character to automate setting up achievements based on nodes or variables avaiable in your character, you may choose to use ``setup_advanced_achievements(list, params)``

This may also be used to be given access to Codex's save data system.

```
func setup_advanced_achievements(list, params):
    var character = params.character
    var codex_lib = params.codex_library
    
    var legacy_save_data = codex_lib.raw_save_char_data(character.filename, "Unlocks", [])

    var ach_manager = character.get_node("AchievementManager")
    for ach in ach_manager.get_children():
        list.define(ach.name, {
            "title": ach.title,
            "desc": ach.description,
            "icon": ach.description
        })
        if legacy_save_data.has(ach.name):
            list.mark_unlocked(ach.name)
```

``params.character`` will be a reference to a temporary instance of your character

``params.codex_library`` will be a reference to [``CharCodexLibrary``](codex_mod/class_ref/CharCodexLibrary.md)

Note: it is not recommended to attempt to use any function that gives you cached CodexData here, as that is only setup when a player views a characters codex page, while achievement setup may be called during a match the first time a character calls to unlock one.  Save data is safe to use here, as that does not require CodexData either.

## Unlockables

!> Achievements, when checked in your Fighter script (or a CharacterState), will be **client-side**, and **the effect will only be shown to the current player of the character, and may cause multiplayer desyncs.**

**However**, Codex offers a method to sync data in multiplayer via modifying style data.  To set this up, you will be required to add [``modify_style_data``](codex_mod/class_ref/Codex.gd#func_modify_style_data) to your Codex.gd file

```gdscript
extends Node


func setup_achievements(list):
    list.set_title("unlock_skin", "Unlocked Alt Skin")
    list.set_desc("unlock_skin", "Required to use the alternate skin of this character")


func modify_style_data(style, params):
    var codex_lib = params.codex_library
    var char_path = params.char_path
    var achievements_list = codex_lib.get_achievement_list(char_path)
    
    if achievements_list.is_unlocked("unlock_skin"):
        style.use_alternate_skin = true
```

You will then need to check for the modifications you added to the style, in your Fighter.  You can do this by either overriding your Fighter's [``apply_style``](class_ref/Fighter#func_apply_style) function, or checking their [``applied_style``](class_ref/Fighter#prop_applied_style) variable.

```gdscript
extends Fighter

var unlocks_applied = false
var using_skin_two = false

func apply_style(style):
    .apply_style(style)
    if style != null:
        ### apply_style is called every frame, a variable like this makes sure options are only applied once
        if unlocks_applied == false:
            unlocks_applied = true 
            using_skin_two = style.get("use_alternate_skin", false)
```

Alternatively, checking applied_style, in a CharacterState

```
extends CharacterState

func _enter():
    if host.applied_style != null:
        if host.applied_style.get("use_alternate_intro", false):
            host.change_state("OtherIntro")
```

!> **Note:** the input of apply_style, and the applied_style variable, may both be null, or may not contain your modifications if the player does not have Codex installed, thus why the above examples check for both of these cases.

!> The above setup also allows Codex to remain **optional**, and doesn't require the opponent to install Codex either, as the data is stored and synced through the style.  If you wish for your character to require Achievements, consider adding "tri_char_codex" to the requirements of your character's _metadata, and mark your Steam Workshop page as requiring Character Codex Library.