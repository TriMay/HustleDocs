[](../wip.md ':include')

<div id="page_main"></div>


<script>

let data = {
    version: "1.8.18",
    name: "ActionUIData",
    inherits: "Control",
    script_path: "res://ui/ActionSelector/ActionUIData/ActionUIData.gd",
    scene_path: "res://ui/ActionSelector/ActionUIData/ActionUIData.tscn",
    desc: "", // @TODO
    signals: [
        { name:'data_changed',
          params:[],
                desc:"Emitted when the player changes selections made in this ActionUIData scene. See [_ready()](#func__ready)\n\nThe game listens to this signal and restarts the prediction when it is emitted." },
    ],
    constants: [
    ],
    properties: [
        { export:true, unused:true, name:'display_offset',
          type:'Vector2', value:'Vector2()',
                desc:"*Unused.*" },
        { unused:true, name:'facing',
          type:'int', value:'- 1',
                desc:"*Unused, use [set_facing()](#func_set_facing) and [get_facing()](#func_get_facing) instead.*" },
        { name:'action_buttons',
          type:'Node', value:'null',
                desc:"Direct reference to the Action Menu" },
        { name:'fighter',
          type:'Fighter', value:'null',
                desc:"Direct reference to the [Fighter](class_ref/Fighter) object this ActionUIData belongs to." },
    ],
    methods: [
        { name:'_ready',
          params:[],
                desc:"Called when this node and it's child nodes are \"ready\". **See [Node._ready()](https://docs.godotengine.org/en/3.5/classes/class_node.html#class-node-method-ready)**\n\nConnects the data_changed signal of all child nodes to this nodes [data_changed](#signal_data_changed) signal." },
        { name:'on_opponent_button_selected',
          params:['button:Node'],
                desc:"Called by the Action Menu when the player selects a state for the opponent prediction, while the state that owns this ActionUIData is selected. ``button`` is a direct reference to the ActionButton selected.\n\n*The method is empty by default and should be overridden to have any effect.*" },
        { name:'on_button_selected',
          params:[],
                desc:"Called by the Action Menu when the player selects the state that owns this ActionUIData.\n\n*The method is empty by default and should be overridden to have any effect.*" },
        { name:'get_data',
          params:[], type:'Dictionary',
                desc:"Called by the Action Menu when the player has locked in their selection, or when the prediction resets after [data_changed](#signal_data_changed) is emitted.\n\n\
The returned [Dictionary](https://docs.godotengine.org/en/3.5/classes/class_dictionary.html) is provided to the state that owns this ActionUIData and is available in it's script via it's [data](class_ref/StateInterface#prop_data) variable during the states execution.\n\n\
By default, depending on how many child nodes this ActionUIData contains, the data returned is either the data from the child nodes get_data() function directly if there is only one child, or if there are two or more children it will be a Dictionary of each child nodes get_data() values organized by child nodes names.\n\n\
```gdscript\n# Example for one 8Way child\ndata[\"x\"] # or data.x\ndata[\"y\"] # or data.y\n\n# Example for an 8Way named \"Direction\" and a Slider named \"Distance\"\ndata[\"Direction\"][\"x\"] # or data.Direction.x\ndata[\"Direction\"][\"y\"] # or data.Direction.y\ndata[\"Distance\"][\"x\"] # or data.Distance.x\n```" },
        { name:'set_facing',
          params:['facing:int'],
                desc:"Called by the Action Menu at the start of each turn, providing the facing int (1 if right, -1 if left) of the [Fighter](class_ref/Fighter).  Calls the set_facing() function of all child nodes that have it." },
        { name:'get_facing',
          params:[], type:'int',
                desc:"Returns the value of the ``get_facing()`` function of the first child node that has it." },
        { name:'init',
          params:[], // @TODO give it a "Called By" description
                desc:"Calls the ``init()`` function of all child nodes that have it." },
        { name:'fighter_update',
          params:[],
                desc:"Called by the Action Menu at the start of each turn, and when another state is selected that isn't the one that owns this ActionUIData.\n\n*The method is empty by default and should be overridden to have any effect.*" },
    ],
};


    Vue.createApp(ClassDocsComponent, data).mount("#page_main");
</script>