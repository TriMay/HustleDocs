# CodexData
- class_name CodexData
- extends Reference





---
## Property Descriptions

### var char_path
- var char_path : String = ""

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var banner
- var banner : Texture = null

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var banner_offset
- var banner_offset : Vector2 = Vector2(32, 32)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var banner_scale
- var banner_scale : Vector2 = Vector2(1, 1)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var banner_rotation
- var banner_rotation : float = 0

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var title
- var title : String = ""

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var subtitle
- var subtitle : String = ""

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var summary
- var summary : String = ""

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var moveset
- var moveset : Dictionary = {}

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var stances
- var stances : Array = []

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var tags
- var tags : Array = []

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var interrupt_types
- var interrupt_types : Array = []

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var custom_tabs
- var custom_tabs : Array = []

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var stats
- var stats : CodexStats = null

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var has_no_moveset
- var has_no_moveset : bool = false

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var has_no_stats
- var has_no_stats : bool = false

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var character_parsed
- var character_parsed : Fighter = null

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var error
- var error : String = ""

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var codex_handler
- var codex_handler : Node = null

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')




---
## Method Descriptions

### func _init
- func _init(char_path:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func parse_fighter
- func parse_fighter(char_instance:Node)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_title
- func set_title(value:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_title
- func get_title() -> String

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_summary
- func set_summary(value:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_summary
- func get_summary() -> String

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_subtitle
- func set_subtitle(value:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_subtitle
- func get_subtitle() -> String

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func add_custom_text_tab
- func add_custom_text_tab(tab_title:String, text:String)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func add_custom_scene_tab
- func add_custom_scene_tab(tab_title:String, scene:PackedScene)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func define_state
- func define_state(name:String, data, force_new:bool=false)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func tag_moves
- func tag_moves(tag:String, moves)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func load_char_data
- func load_char_data(key=null, default=null) -> Variant

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func save_char_data
- func save_char_data(key=null, value=null)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func reset_char_data
- func reset_char_data()

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')




