# CharOptionsPage
- class_name CharOptionsPage
- extends VBoxContainer





---
## Property Descriptions

### var option_values
- var option_values : Dictionary = {}

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var tracked_option_nodes
- var tracked_option_nodes : Dictionary = {}

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var button_groups
- var button_groups : Dictionary = {}

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')




---
## Method Descriptions

### func _ready
- func _ready()

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func add_label
- func add_label(label:String, params:Dictionary={}) -> Node

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func add_seperator
- func add_seperator(label:String="", params:Dictionary={}) -> Node

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func add_toggle
- func add_toggle(id:String, label:String, default:bool=false, params:Dictionary={}) -> Node

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func add_textline
- func add_textline(id:String, label:String, default:String="", params:Dictionary={}) -> Node

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func add_number
- func add_number(id:String, label:String, default:int=0, params:Dictionary={}) -> Node

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func add_slider
- func add_slider(id:String, label:String, default:int=0, params:Dictionary={}) -> Node

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func add_dropdown
- func add_dropdown(id:String, label:String, default=null, params:Dictionary={}) -> Node

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func add_color
- func add_color(id:String, label:String, default=null, params:Dictionary={}) -> Node

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func add_custom_scene
- func add_custom_scene(id:String, scene, default=null, params:Dictionary={}) -> Node

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func add_custom_decor
- func add_custom_decor(scene, params:Dictionary={}) -> Node

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __parse_as_scene
- func __parse_as_scene(scene) -> Node

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __add_tracked_node
- func __add_tracked_node(id:String, node:Node, default=null, params:Dictionary={})

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __add_decoration_node
- func __add_decoration_node(node:Node, params:Dictionary={})

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func __get_named_button_group
- func __get_named_button_group(group_name) -> ButtonGroup

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func set_value
- func set_value(value)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_data
- func get_data() -> Variant

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')




---
## Signal Descriptions

### signal data_changed
- signal data_changed()

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')




