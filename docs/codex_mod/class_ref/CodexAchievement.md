<div id="page_main"></div>


<script>

let data = {
    version: "1.9.20",
    updated: "2024-10-07",
    name: "CodexAchievement",
    inherits: "Reference",
    script_path: "",
    scene_path: "",
    desc: "",
    signals: [
    ],
    constants: [
    ],
    properties: [
        { name:'title',
          type:'String', value:'""',
                desc:"" },
        { name:'desc',
          type:'String', value:'""',
                desc:"" },
        { name:'icon',
          type:'Variant', value:'null',
                desc:"" },
        { name:'locked_title',
          type:'String', value:'""',
                desc:"" },
        { name:'locked_desc',
          type:'String', value:'""',
                desc:"" },
        { name:'locked_icon',
          type:'Variant', value:'null',
                desc:"" },
        { name:'secret',
          type:'bool', value:'false',
                desc:"" },
        { name:'unlocked',
          type:'bool', value:'false',
                desc:"" },
        { name:'highlight_color',
          type:'Color', value:'Color(1.0, 1.0, 1.0)',
                desc:"" },
        { name:'counter_id',
          type:'String', value:'""',
                desc:"" },
        { name:'counter_target',
          type:'int', value:'-1',
                desc:"" },
        { name:'counter_limit',
          type:'bool', value:'false',
                desc:"" },
    ],
    methods: [
    ],
};


    Vue.createApp(ClassDocsComponent, data).mount("#page_main");
</script>