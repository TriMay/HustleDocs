[](../wip.md ':include')

<div id="page_main"></div>


<script>

let data = {
    version: "1.8.18",
    name: "PlayerExtra",
    inherits: "HBoxContainer",
    script_path: "res://ui/ActionSelector/PlayerExtra.gd",
    desc: "",
    signals: [
        { name:'data_changed',
          params:[],
                desc:"" },
    ],
    constants: [
    ],
    properties: [
        { name:'fighter',
          type:'Fighter',
                desc:"" },
        { name:'player_id',
          type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'selected_move',
          type:'UNKNOWN_TYPE',
                desc:"" },
    ],
    methods: [
        { name:'_ready',
          params:[],
                desc:"" },
        { name:'on_data_changed',
          params:[],
                desc:"" },
        { name:'set_fighter',
          params:['fighter:Fighter'],
                desc:"" },
        { name:'get_extra',
          params:[], type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'show_options',
          params:[], type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'reset',
          params:[],
                desc:"" },
        { name:'update_selected_move',
          params:['move_state'],
                desc:"" },
    ],
};


    Vue.createApp(ClassDocsComponent, data).mount("#page_main");
</script>