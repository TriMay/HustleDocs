[](../wip.md ':include')

<div id="page_main"></div>


<script>
    
let data = {
    version: "1.8.18",
    name: "PlayerInfo",
    inherits: "Control",
    script_path: "res://ui/PlayerInfo.gd",
    desc: "",
    signals: [
    ],
    constants: [
    ],
    properties: [
        { name:'fighter',
          type:'Fighter',
                desc:"" },
        { name:'player_id',
          type:'int', value:'1',
                desc:"" },
        { name:'under_healthbar',
          type:'bool', value:'false',
                desc:"" },
    ],
    methods: [
        { name:'set_fighter',
          params:['fighter'],
                desc:"" },
        { name:'on_position_changed',
          params:['under_healthbar'],
                desc:"" },
    ],
};

    Vue.createApp(ClassDocsComponent, data).mount("#page_main");
</script>