# Codex Examples


## Moveset
```gdscript
extends Node

func register(codex):
    ### Set custom description on moves
    ### Move descriptions are bbcode enabled
    ### See https://docs.godotengine.org/en/3.5/tutorials/ui/bbcode_in_richtextlabel.html
    codex.moveset["Grab"].desc = "The Best Move"
    codex.moveset["Burst"].desc = "The Worst Move"
    codex.moveset["Taunt"].desc = "Your Only Move"
    
    
    ### Correct move visibility
    codex.moveset["CustomMove"].visible = true
    codex.moveset["UnusedMove"].visible = false
    
    
    ### Add missed frame data
    codex.moveset["ProjectileMove"].set_projectile_tick(5)
    codex.moveset["InvulnerableMove"].set_start_invulnerability_tick(3)
    codex.moveset["InvulnerableMove"].set_end_invulnerability_tick(8)
    codex.moveset["ArmorMove"].set_start_armor_tick(4)
    codex.moveset["ArmorMove"].set_end_armor_tick(9)
    codex.moveset["GimmickMove"].set_gimmick_tick(7, "Custom Gimmick")
    codex.moveset["GimmickMove2"].set_gimmick_tick_range(2, 6, "Custom Gimmick")
    
    
    ### Add custom move stats
    codex.moveset["GimmickMove"].custom_stats["Gimmick Cost"] = "5"
    codex.moveset["GimmickMove2"].custom_stats["Any Title"] = "Any Value"
    
    
    ### Add custom tags
    ### Players can view moves by specific tags, like they can for stances
    codex.tags = ["Sword", "Hammer"]
    codex.moveset["SwordMove"].tags = ["Sword"]
    codex.moveset["HammerMove"].tags = ["Sword"]
    codex.moveset["DualMove"].tags = ["Sword", "Hammer"]
    ### OR
    codex.tag_moves("Sword", ["SwordMove", "DualMove"])
    codex.tag_moves("Hammer", ["HammerMove", "DualMove"])
    
    
    ### Copy a move, useful to show move variants
    codex.moveset["Copy"] = codex.moveset["Original"].duplicate()
    
    
    ### Add additional move
    ### Options match variable names of CodexState
    ### hitbox_data uses CodexState.define_hitbox() for each entry.  See Hitboxes example.
    ### Can also be used to modify the data of an existing move
    codex.define_state("FakeMove", {
        "icon" : load("res://path/to/icon.png"),
        "title" : "Title Here",
        "desc" : "Description Here",
        "length" : 30,
        "stances" : ["Normal"],
        "hitbox_data" : {
            "Hitbox1" {
                "damage": 50,
                "start": 5,
                "active": 4,
            },
            "Hitbox2" {
                "damage": 50,
                "start": 5,
                "active": 4,
            }
        }
    })
```


## Stances
```gdscript
extends Node

func register(codex):
    ### add a stance to stance list
    codex.stances.append("SpecialStance")
    
    ### remove a stance from stance list
    codex.stances.erase("DebugStance")
    
    ### set full stance list
    codex.stances = ["Normal", "SpecialStance", "Sword", "Bow"]
    
    
    ### add move to stance
    codex.moveset["Attack"].stances.append("SpecialStance")
    
    ### remove move from stance
    codex.moveset["Attack"].stances.erase("DebugStance")
    
    ### set all stances a move appears in
    codex.moveset["Attack"].stances = ["Normal", "SpecialStance", "Sword", "Bow"]
```


## Hitbox Data
```gdscript
extends Node

func register(codex):
    ### Correct hitbox stats
    ### Check CodexHitbox for full list of options
    codex.moveset["Attack"].hitbox_data["Hitbox"].damage = 64
    codex.moveset["Attack"].hitbox_data["Hitbox"].combo_damage = 32
    codex.moveset["Attack"].hitbox_data["Hitbox"].minimum_damage = 12
    
    codex.moveset["Attack"].hitbox_data["Hitbox"].stun = 30
    codex.moveset["Attack"].hitbox_data["Hitbox"].combo_stun = 40
    
    codex.moveset["Attack"].hitbox_data["Hitbox"].is_grab = false
    codex.moveset["Attack"].hitbox_data["Hitbox"].is_hit_grab = false
    codex.moveset["Attack"].hitbox_data["Hitbox"].is_guard_break = true

    
    ### Copy a hitbox
    codex.moveset["Attack"].hitbox_data["CopyHitbox"] = codex.moveset["Attack"].hitbox_data["Hitbox"].duplicate()
    
    
    ### Add additional hitbox data
    ### Options match variable names of CodexHitbox
    ### Can also be used to modify the data of an existing hitbox
    codex.moveset["Attack"].define_hitbox("FakeHitbox", {
        "damage": 64,
        "stun": 30,
        "knockback": 5.0,
        "knockback_x": 1.0,
        "knockback_y": 0.0,
        "start": 5,
        "active": 4,
        "hits_standing": true,
        "hits_grounded": true,
        "hits_aerial": true,
        "di_modifier": 1.0,
        "sdi_modifier": 1.0,
        "di_modifier": 1.0
    })
    
    
    ### Remove hitboxes not meant to be seen
    codex.moveset["Attack"].hitbox_data.erase("DebugHitbox")
    codex.moveset["Attack"].hitbox_data.erase("UnusedHitbox")
```


## Stats Tab
```gdscript
extends Node

func register(codex):
    ### Correct character stats
    ### Check CodexStats for full list of options
    codex.stats.max_health = 420
    codex.stats.air_options = 3
    codex.stats.free_cancels = 1
    codex.stats.damage_taken = 0.5
    codex.stats.knockback_taken = 2.0
    
    
    ### Stats tab sprite
    codex.stats.sprite_texture = load("res://mod/character/codex_pose.png")
    codex.stats.sprite_position = Vector2(0, -5)
```


## Custom Tabs
```gdscript
extends Node

func register(codex):
    ### Add a character summary.
    ### Summary tab is bbecode enabled.
    ### See https://docs.godotengine.org/en/3.5/tutorials/ui/bbcode_in_richtextlabel.html
    codex.summary = "Character Summary Here"
    ### OR
    codex.summary = """GDScript lets you write multiple-line strings with tripple-quotes.
Though do note that tabs at the start of lines here will show up in the text on Codex.
GDScript will not error for mismatched tabs in a multi-line string, so this is fine.
    """
    
    
    ### Add a custom basic text tab.
    ### Text tabs are bbcode enabled.
    ### See https://docs.godotengine.org/en/3.5/tutorials/ui/bbcode_in_richtextlabel.html
    codex.add_custom_text_tab("Tab Title Here", "Description Here")
    
    
    ### Only major difference between Summary and other custom text tabs:
    ### Summary tab always appears at the left side of the tab row
    ### All custom tabs appear on the right side, in the order they were added
    
    
    ### Add a .tscn as a custom tab.
    ### The root node of said scene should be any Control or Control extending node type, such as any Container.
	codex.add_custom_scene_tab("Tab Title Here", load("res://YourMod/path/to/custom/ui/scene.tscn"))

```