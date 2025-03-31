# ActionUIData
- class_name ActionUIData
- extends Control
- script "res://ui/ActionSelector/ActionUIData/ActionUIData.gd"
- scene "res://ui/ActionSelector/ActionUIData/ActionUIData.tscn"





---
## Property Descriptions

### var display_offset
- var display_offset : Vector2 = Vector2()

*Unused.*



### var facing
- var facing : int = - 1

*Unused, use [set_facing()](#func_set_facing) and [get_facing()](#func_get_facing) instead.*



### var action_buttons
- var action_buttons : Node = null

Direct reference to the Action Menu



### var state
- var state : CharacterState = null

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### var fighter
- var fighter : Fighter = null

Direct reference to the [Fighter](class_ref/Fighter) object this ActionUIData belongs to.




---
## Method Descriptions

### func _ready
- func _ready()

Called when this node and it's child nodes are "ready". **See [Node._ready()](https://docs.godotengine.org/en/3.5/classes/class_node.html#class-node-method-ready)**

Connects the data_changed signal of all child nodes to this nodes [data_changed](#signal_data_changed) signal.



### func on_opponent_button_selected
- func on_opponent_button_selected(button:Node)

Called by the Action Menu when the player selects a state for the opponent prediction, while the state that owns this ActionUIData is selected. ``button`` is a direct reference to the ActionButton selected.

*The method is empty by default and should be overridden to have any effect.*



### func on_button_selected
- func on_button_selected()

Called by the Action Menu when the player selects the state that owns this ActionUIData.

*The method is empty by default and should be overridden to have any effect.*



### func on_data_changed
- func on_data_changed()

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_data
- func get_data() -> Dictionary

Called by the Action Menu when the player has locked in their selection, or when the prediction resets after [data_changed](#signal_data_changed) is emitted.

The returned [Dictionary](https://docs.godotengine.org/en/3.5/classes/class_dictionary.html) is provided to the state that owns this ActionUIData and is available in it's script via it's [data](class_ref/StateInterface#prop_data) variable during the states execution.

By default, depending on how many child nodes this ActionUIData contains, the data returned is either the data from the child nodes get_data() function directly if there is only one child, or if there are two or more children it will be a Dictionary of each child nodes get_data() values organized by child nodes names.

```gdscript
# Example for one 8Way child
data["x"] # or data.x
data["y"] # or data.y

# Example for an 8Way named "Direction" and a Slider named "Distance"
data["Direction"]["x"] # or data.Direction.x\ndata["Direction"]["y"] # or data.Direction.y
data["Distance"]["x"] # or data.Distance.x
```



### func set_facing
- func set_facing(facing:int)

Called by the Action Menu at the start of each turn, providing the facing int (1 if right, -1 if left) of the [Fighter](class_ref/Fighter).  Calls the set_facing() function of all child nodes that have it.



### func get_facing
- func get_facing() -> int

Returns the value of the ``get_facing()`` function of the first child node that has it.



### func init
- func init()

Calls the ``init()`` function of all child nodes that have it.



### func fighter_update
- func fighter_update()

Called by the Action Menu at the start of each turn, and when another state is selected that isn't the one that owns this ActionUIData.\n\n*The method is empty by default and should be overridden to have any effect.*




---
## Signal Descriptions

### signal data_changed
- signal data_changed()

Emitted when the player changes selections made in this ActionUIData scene. See [_ready()](#func__ready)

The game listens to this signal and restarts the prediction when it is emitted.

