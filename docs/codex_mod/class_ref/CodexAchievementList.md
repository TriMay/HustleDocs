# CodexAchievementList
- class_name CodexAchievementList
- extends Reference





---
## Property Descriptions

### var achievements
- var achievements : Dictionary = {}

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var counters
- var counters : Dictionary = {}

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var default_locked_title
- var default_locked_title : String = ""

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var default_locked_desc
- var default_locked_desc : String = ""

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var default_locked_icon
- var default_locked_icon : Variant = null

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var default_unlocked_icon
- var default_unlocked_icon : Variant = null

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var uses_default_fanfare
- var uses_default_fanfare : bool = true

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var uses_default_sound
- var uses_default_sound : bool = true

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')




---
## Method Descriptions

### func define
- func define(achievement_id:String, data:Dictionary)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_title
- func set_title(achievement_id:String, title:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_desc
- func set_desc(achievement_id:String, desc:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_icon
- func set_icon(achievement_id:String, icon)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_locked_title
- func set_locked_title(achievement_id:String, title:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_locked_desc
- func set_locked_desc(achievement_id:String, desc:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_locked_icon
- func set_locked_icon(achievement_id:String, icon)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_default_locked_title
- func set_default_locked_title(title:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_default_locked_desc
- func set_default_locked_desc(desc:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_default_locked_icon
- func set_default_locked_icon(icon)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func mark_secret
- func mark_secret(achievement_id:String, secret:bool=true)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func mark_unlocked
- func mark_unlocked(achievement_id:String, unlocked:bool=true)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func is_secret
- func is_secret(achievement_id:String) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func is_unlocked
- func is_unlocked(achievement_id:String) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func is_array_unlocked
- func is_array_unlocked(achievements:Array) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func assign_counter
- func assign_counter(achievement_id:String, counter_id:String, target_value:int=-1)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_counter_value
- func get_counter_value(counter_id:String) -> int

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_counter_value
- func set_counter_value(counter_id:String, value:int)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func is_target_met
- func is_target_met(achievement_id:String) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_totals
- func get_totals() -> Dictionary

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_unlocked_array
- func get_unlocked_array() -> Array

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_display_title
- func get_display_title(achievement_id:String) -> String

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_display_desc
- func get_display_desc(achievement_id:String) -> String

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_display_icon
- func get_display_icon(achievement_id:String) -> Texture

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_display_highlight
- func get_display_highlight(achievement_id:String, ignore_locked_check:bool=false) -> Color

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_debug_title
- func get_debug_title(achievement_id:String, as_unlocked:bool=true) -> String

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_debug_desc
- func get_debug_desc(achievement_id:String, as_unlocked:bool=true) -> String

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_debug_icon
- func get_debug_icon(achievement_id:String, as_unlocked:bool=true) -> Texture

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_debug_highlight
- func get_debug_highlight(achievement_id:String, as_unlocked:bool=true) -> Color

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_display_counter_value
- func get_display_counter_value(achievement_id:String) -> int

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_display_counter_target
- func get_display_counter_target(achievement_id:String) -> int

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_display_counter_text
- func get_display_counter_text(achievement_id:String) -> String

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __parse_to_texture
- func __parse_to_texture(input) -> Texture

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')




