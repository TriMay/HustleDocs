# CharCodexLibrary
- class_name CharCodexLibrary
- extends Node





---
## Property Descriptions

### var codex_cache
- var codex_cache : Dictionary = {}

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var codex_save_data
- var codex_save_data : Dictionary = {}

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var codex_achievements
- var codex_achievements : Dictionary = {}

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var codex_has_options
- var codex_has_options : Dictionary = {}

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var prefers_more_info
- var prefers_more_info : bool = false

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var preferred_tab
- var preferred_tab : String = ""

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var fixed
- var fixed : FixedMath = FixedMath.new()

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var BlankCodexScene
- var BlankCodexScene : PackedScene = load("res://_tri_char_codex/CodexPage.tscn")

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')




---
## Method Descriptions

### func _init
- func _init()

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func _ready
- func _ready()

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func generate_node
- func generate_node(char_path:String) -> Node

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func generate_options_node
- func generate_options_node(char_path:String) -> Node

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func has_cached
- func has_cached(char_path:String) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func can_generate
- func can_generate(char_path:String) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func char_has_options
- func char_has_options(char_path:String) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func load_all_char_options
- func load_all_char_options(fighter) -> Dictionary

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func save_all_char_options
- func save_all_char_options(fighter, value) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func save_codex_setting
- func save_codex_setting(key:String, value) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func load_codex_setting
- func load_codex_setting(key:String) -> Variant

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __attempt_load_char_instance
- func __attempt_load_char_instance(char_path) -> Fighter

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __attempt_load_codex_script
- func __attempt_load_codex_script(char_path) -> Node

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __get_codex_script_path
- func __get_codex_script_path(char_path:String) -> String

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __analyze_and_cache
- func __analyze_and_cache(char_path:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __register_codex_override
- func __register_codex_override(codex_data:CodexData)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __parse_instance_moveset
- func __parse_instance_moveset(char_instance:Node) -> Dictionary

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __parse_moveset_visibility
- func __parse_moveset_visibility(codex_data:CodexData)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __parse_hitbox_data_visibility
- func __parse_hitbox_data_visibility(state:CodexState)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func array_has_any
- func array_has_any(haystack:Array, needles:Array) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __parse_state_data
- func __parse_state_data(state:StateInterface, char_instance:Node=null) -> CodexState

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __parse_state_hitboxes
- func __parse_state_hitboxes(state:StateInterface, char_instance:Node) -> Dictionary

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __parse_hitbox_data
- func __parse_hitbox_data(hitbox:Hitbox, char_instance=null) -> CodexHitbox

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __parse_is_hit_grab
- func __parse_is_hit_grab(hitbox, char_instance:Node) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __parse_state_script_source
- func __parse_state_script_source(state_data:CodexState, source_code:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func code_keyphrase_test
- func code_keyphrase_test(haystack:String, needle:String) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __generate_from_cache
- func __generate_from_cache(char_path:String) -> Node

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __generate_error
- func __generate_error(text) -> Node

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __page_editor
- func __page_editor(page, char_path:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func load_for_extra
- func load_for_extra(fighter:Node, key=null, default=null, reload:bool=false) -> Variant

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func raw_load_char_data
- func raw_load_char_data(char_path:String, key=null, default=null) -> Variant

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func raw_save_char_data
- func raw_save_char_data(char_path:String, key, value) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func init_char_data
- func init_char_data(char_path:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func raw_reset_char_data
- func raw_reset_char_data(char_path:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_new_char_data
- func get_new_char_data(char_path:String) -> Dictionary

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_save_file_path
- func get_save_file_path(char_path:String) -> String

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_legacy_save_file_path
- func get_legacy_save_file_path(char_path:String) -> String

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __cache_achievement_list
- func __cache_achievement_list(char_path:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_achievement_list
- func get_achievement_list(char_path:String) -> CodexAchievementList

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func unlock_achievement
- func unlock_achievement(fighter, achievement_id:String, multiplayer_only:bool=false) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func relock_achievement
- func relock_achievement(fighter, achievement_id:String, multiplayer_only:bool=false) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func is_achievement_unlocked
- func is_achievement_unlocked(fighter, achievement_id:String) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func is_achievement_array_unlocked
- func is_achievement_array_unlocked(fighter, achievements:Array) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func achievement_target_met
- func achievement_target_met(fighter, achievement_id) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_unlocked_achievements
- func get_unlocked_achievements(fighter) -> Array

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func increment_counter
- func increment_counter(fighter, counter_id:String, by_amount:int=1, multiplayer_only:bool=false) -> int

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_counter
- func set_counter(fighter, counter_id:String, to_amount:int=1, multiplayer_only:bool=false) -> int

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_counter
- func get_counter(fighter, counter_id:String) -> int

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __modify_style_data
- func __modify_style_data(char_path, style_data) -> Dictionary

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func track_win
- func track_win(fighter)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func track_loss
- func track_loss(fighter)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func num_wins
- func num_wins(fighter) -> int

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func num_losses
- func num_losses(fighter) -> int

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __on_game_started
- func __on_game_started()

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __on_game_won
- func __on_game_won(winner, game)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __on_game_forfeit
- func __on_game_forfeit(loser, game)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')




---
## Constant Descriptions

### const SAVE_DIR
- const SAVE_DIR : String = "user://cloud/codex_char_saves"

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### const LEGACY_SAVE_DIR
- const LEGACY_SAVE_DIR : String = "user://codex_char_saves"

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### const CODEX_SETTINGS_SAVE_PATH
- const CODEX_SETTINGS_SAVE_PATH : String = "user://cloud/codex_settings.json"

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### const DEFAULT_CODEX_SETTINGS
- const DEFAULT_CODEX_SETTINGS : Dictionary = {
    "win_lost_stats": "wins_only",
    "no_fun_mode": false,
    "misclick_prevent": false,
    "wins": {},
    "losses": {}
}

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')




---
## Signal Descriptions

### signal achievement_unlocked
- signal achievement_unlocked(achievement_list, achievement_id)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### signal char_won
- signal char_won(char_path, amount)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### signal char_lost
- signal char_lost(char_path, amount)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')




