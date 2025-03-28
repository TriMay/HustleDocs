[](../wip.md ':include')

<div id="page_main"></div>


<script>

let data = {
    version: "1.8.18",
    name: "ThrowBox",
    inherits: "Hitbox",
    script_path: "res://characters/ThrowBox.gd",
    desc: "",
    signals: [
    ],
    constants: [
    ],
    properties: [
        { export:true, name:'_c_Throw_Data',
          type:'int', value:'0',
                desc:"" },
        { export:true, name:'throw_state',
          type:'String', value:'""',
                desc:"" },
    ],
    methods: [
        { name:'activate',
          params:[],
                desc:"" },
    ],
};


    Vue.createApp(ClassDocsComponent, data).mount("#page_main");
</script>