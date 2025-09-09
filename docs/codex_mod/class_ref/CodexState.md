# CodexState
- class_name CodexState
- extends Reference





---
## Property Descriptions

### var icon
- var icon : Texture = null

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var title
- var title : String = ""

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var desc
- var desc : String = ""

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var visible
- var visible : bool = true

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var visibility_set
- var visibility_set : bool = false

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var type
- var type : String = ""

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var air_type
- var air_type : String = ""

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var length
- var length : int = -1

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var endless
- var endless : bool = false

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var iasa
- var iasa : int = -1

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var anim_name
- var anim_name : String = ""

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var interrupt_types
- var interrupt_types : Array = []

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var stances
- var stances : Array = []

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var tags
- var tags : Array = []

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var change_stance
- var change_stance : String = ""

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var super_req
- var super_req : int = 0

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var super_cost
- var super_cost : int = 0

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var hitbox_data
- var hitbox_data : Dictionary = {}

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var tick_data
- var tick_data : Dictionary = {}

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var custom_stats
- var custom_stats : Dictionary = {}

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')




---
## Method Descriptions

### func _init
- func _init(state=null)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func define
- func define(data=null)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func duplicate
- func duplicate() -> CodexState

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func copy_to
- func copy_to(copy)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func duplicate_all_hitbox_data
- func duplicate_all_hitbox_data() -> Dictionary

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func parse_state
- func parse_state(state:StateInterface)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func parse_dictionary
- func parse_dictionary(data:Dictionary)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func define_hitbox
- func define_hitbox(name:String, data, force_new:bool=false)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_visible
- func set_visible(value:bool)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_visible
- func get_visible() -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_interrupt_tick
- func set_interrupt_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func unset_interrupt_tick
- func unset_interrupt_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_projectile_tick
- func set_projectile_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func unset_projectile_tick
- func unset_projectile_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_start_armor_tick
- func set_start_armor_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func unset_start_armor_tick
- func unset_start_armor_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_end_armor_tick
- func set_end_armor_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func unset_end_armor_tick
- func unset_end_armor_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_start_invulnerability_tick
- func set_start_invulnerability_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func unset_start_invulnerability_tick
- func unset_start_invulnerability_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_end_invulnerability_tick
- func set_end_invulnerability_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func unset_end_invulnerability_tick
- func unset_end_invulnerability_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_start_projectile_invuln_tick
- func set_start_projectile_invuln_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func unset_start_projectile_invuln_tick
- func unset_start_projectile_invuln_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_end_projectile_invuln_tick
- func set_end_projectile_invuln_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func unset_end_projectile_invuln_tick
- func unset_end_projectile_invuln_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_start_grab_invuln_tick
- func set_start_grab_invuln_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func unset_start_grab_invuln_tick
- func unset_start_grab_invuln_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_end_grab_invuln_tick
- func set_end_grab_invuln_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func unset_end_grab_invuln_tick
- func unset_end_grab_invuln_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_start_aerial_invuln_tick
- func set_start_aerial_invuln_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func unset_start_aerial_invuln_tick
- func unset_start_aerial_invuln_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_end_aerial_invuln_tick
- func set_end_aerial_invuln_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func unset_end_aerial_invuln_tick
- func unset_end_aerial_invuln_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_start_grounded_invuln_tick
- func set_start_grounded_invuln_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func unset_start_grounded_invuln_tick
- func unset_start_grounded_invuln_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_end_grounded_invuln_tick
- func set_end_grounded_invuln_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func unset_end_grounded_invuln_tick
- func unset_end_grounded_invuln_tick(tick:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_gimmick_tick
- func set_gimmick_tick(tick:int, text:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func unset_gimmick_tick
- func unset_gimmick_tick(tick:int, text:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_gimmick_tick_range
- func set_gimmick_tick_range(start:int, end:int, text:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_tick_item
- func set_tick_item(tick:int, type:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func unset_tick_item
- func unset_tick_item(tick:int, type:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func parse_source_script
- func parse_source_script(source_code:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func apply_known_script
- func apply_known_script(path:String, state)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func script_has_keyphrase
- func script_has_keyphrase(haystack:String, needle:String) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')




