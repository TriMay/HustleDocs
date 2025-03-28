<div id="page_main"></div>


<script>

let data = {
    version: "1.9.20",
    updated: "2024-10-09",
    name: "All Codex.gd Fuctions",
    inherits: "Node",
    script_path: "",
    scene_path: "",
    desc: "The following is a list of all functions the Codex Library will search for in your custom Codex.gd file.\n\n***All functions are optional, and safely ignored if missing from your Codex.gd file.***",
    signals: [
    ],
    constants: [
    ],
    properties: [
    ],
    methods: [
        { name:'register',
          params:['codex:CodexData'],
                desc:"" },
        { name:'setup_achievements',
          params:['list:CodexAchievementList'],
                desc:"" },
        { name:'setup_advanced_achievements',
          params:['list:CodexAchievementList', 'params:Dictionary'],
                desc:"" },
        { name:'setup_options',
          params:['options:CharOptionsPage', 'params:Dictionary'],
                desc:"" },
        { name:'modify_style_data',
          params:['style_data:Dictionary', 'params:Dictionary'],
                desc:"" },
        { name:'new_save',
          params:[], type:'Dictionary',
                desc:"" },
    ],
};


    Vue.createApp(ClassDocsComponent, data).mount("#page_main");
</script>