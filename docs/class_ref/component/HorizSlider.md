[](../../wip.md ':include')

<div id="page_main"></div>


<script>

let data = {
    version: "1.8.23",
    name: "UI Component: HorizSlider",
    inherits: "VBoxContainer",
    script_path: "",
    scene_path: "res://ui/HorizSlider/HorizSlider.tscn",
    desc: "",
    signals: [
        { name:'data_changed',
          params:[],
                desc:"" },
    ],
    constants: [
    ],
    properties: [
        { onready:true, name:'default',
          type:'Node', value:'$Direction.value',
                desc:"" },
        { export:true, name:'centered',
          type:'bool', value:'true',
                desc:"" },
        { export:true, name:'min_value',
          type:'int', value:'0',
                desc:"" },
        { export:true, name:'max_value',
          type:'int', value:'100',
                desc:"" },
        { name:'buffer_value_changed',
          type:'bool', value:'false',
                desc:"" },
    ],
    methods: [
        { name:'_input',
          params:['event:InputEvent'],
                desc:"" },
        { name:'_ready',
          params:[],
                desc:"" },
        { name:'on_value_changed',
          params:['value'],
                desc:"" },
        { name:'_process',
          params:['_delta'],
                desc:"" },
        { name:'get_value',
          params:[], type:'int',
                desc:"" },
        { name:'get_data',
          params:[], type:'Dictionary',
                desc:"" },
    ],
};


    Vue.createApp(ClassDocsComponent, data).mount("#page_main");
</script>