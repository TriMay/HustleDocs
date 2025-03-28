# Character Codex Library

Although Codex tries its best to parse as much info as possible automatically, sometimes there are certain (usually unique and code-based) mechanics that it can't understand on its own, or other times you may want to simply add more context with descriptions on your characters moveset or add a summary paragraph of the character.

For these reasons, almost every single aspect of the codex page is customizable.

## Getting Started

!> **Note:** This guide assumes you have a character mod in development, and therefore have a Godot install setup for YOMI Hustle modding.  If you do not have Godot setup for character creation yet, please check [Getting Started](getting_started)

First thing you will need to do is download the [Character Codex Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=3165815605) from the Steam Workshop by subscribing to it.

Once subscribed, the mods zip will be downloaded to your computer in the following location:
- ``{SteamLibrary}/steamapps/workshop/content/2212330/3165815605/``
- **Default:** ``C:/Program Files (x86)/Steam/steamapps/workshop/content/2212330/3165815605/``
- (2212330 being YOMI Hustles ID, 3165815605 being Codexs ID)

It is recommended that you copy ``_tri_char_codex.zip`` from this folder, to the ``mods`` folder next to your Godot editor (you will need to create the ``mods`` folder if you have not already), as shown in the images below:

> ![Create mods folder next to godot editor](https://hustledocs.trimaydev.com/img/codex_create_mods.png)

> ![Copy zip from workshop folder to mods folder](https://hustledocs.trimaydev.com/img/codex_copy_to_mods.png)

Doing so will allow you to test changes you make to your character's Codex page directly in your decompiled copy of the game, and get debug info from the editor, rather than needing to export your character and check from the final build of the game.

## Setting Up Codex.gd

In order to customize your character's Codex page, you will need to create a custom script named ``Codex.gd`` (case-sensitive) in the same folder as your character tscn file.

> ![Create Codex.gd next to your character tscn](https://hustledocs.trimaydev.com/img/codex_create_script.png)

The following example template will add a custom subtitle and a summary to your character's Codex page:

```gdscript
extends Node

func register(codex):
    codex.set_subtitle("The Cool Character")
    codex.set_summary("""Custom Summary Here
Godot lets you use triple quotes to make multi-line strings
    """)
```

The important part is that the Codex mod will look for a ``Codex.gd`` script next to your character file, and if one exists, it will call that script's ``register(codex)`` function.  Codex will provide the ``codex`` input parameter of this function with a [``CodexData``](codex_mod/class_ref/CodexData.md) object, which you can use to change almost anything on your character's Codex page.

## Codex Examples

> **Give moves custom descriptions**
> ```gdscript
> extends Node
> 
> func register(codex):
>     codex.moveset["Grab"].desc = "The Best Move"
>     codex.moveset["Burst"].desc = "The Worst Move"
>     codex.moveset["Taunt"].desc = "Your Only Move"
> ```

> **Correct move visibility**
>
> *(Codex will try to automatically figure out which moves are selectable and which are not, but sometimes it will make mistakes as it can't understand custom code-based mechanics)*
> ```gdscript
> extends Node
> 
> func register(codex):
>     codex.moveset["CustomMove"].visible = true
>     codex.moveset["UnusedMove"].visible = false
> ```

> **Set a custom portrait**
>
> *(By default, Codex will use your character's "Character Portrait 2" if it is set, otherwise it will use "Character Portrait")*
> ```gdscript
> extends Node
> 
> func register(codex):
>     codex.banner = load("res://path/to/custom_portrait.png")
>     codex.banner_offset = Vector2(32, 32)
> ```

> **Add a custom text tab**
> ```gdscript
> extends Node
> 
> func register(codex):
>     codex.add_custom_text_tab("Custom Tab Title", """
> [b]Allows Godot bbcode.[/b]
> [u]Summary tabs do as well[/u]
>     """)
> ```

> **Customize Stats tab**
> ```gdscript
> extends Node
> 
> func register(codex):
>     codex.stats.max_health = 1000
>     codex.stats.air_options = 2
>     codex.stats.free_cancels = 2
>
>     # ALTERNATIVELY
>
>     codex.stats.define({
>         "max_health": 1000,
>         "air_options": 2,
>         "free_cancels": 2,
>     })
> ```