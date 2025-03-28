[](../wip.md ':include')

<div id="page_main"></div>


<script>

let data = {
    version: "1.8.18",
    name: "HurtboxState",
    inherits: "CollisionBox",
    script_path: "res://HurtboxState.gd",
    desc: "",
    signals: [
    ],
    constants: [
    ],
    properties: [
        { export:true, name:'start_tick',
          type:'int', value:'1',
                desc:"" },
        { export:true, name:'active_ticks',
          type:'int', value:'1',
                desc:"" },
        { export:true, name:'endless',
          type:'bool', value:'false',
                desc:"" },
        { name:'started',
          type:'bool', value:'false',
                desc:"" },
        { name:'ended',
          type:'bool', value:'false',
                desc:"" },
        { name:'current_tick',
          type:'int', value:'0',
                desc:"" },
        { name:'prev_state',
          type:'UNKNOWN_TYPE',
                desc:"" },
    ],
    methods: [
        { name:'_ready',
          params:[],
                desc:"" },
        { name:'start',
          params:['host'],
                desc:"" },
        { name:'tick',
          params:['host'],
                desc:"" },
        { name:'copy_to',
          params:['hurtbox_state'],
                desc:"" },
        { name:'end',
          params:['host'], type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'can_draw_box',
          params:[], type:'UNKNOWN_TYPE',
                desc:"" },
    ],
};


    Vue.createApp(ClassDocsComponent, data).mount("#page_main");
</script>