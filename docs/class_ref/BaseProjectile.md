<div id="page_main"></div>


<script>

let data = {
    version: "1.9.0",
    updated: "2024-04-04",
    name: "BaseProjectile",
    inherits: "BaseObj",
    script_path: "res://projectile/BaseProjectile.gd",
    scene_path: "res://projectile/BaseProjectile.tscn",
    desc: "Class for any game object that is not a [``Fighter``](class_ref/Fighter).\n\n_**Note:** Despite its name, objects extending BaseProjectile do not have to be standard projectiles.  BaseProjectile is flexible enough and meant to be used for ANY non-Fighter game object._",
    signals: [
        { name:'got_parried',
          params:[],
                desc:"" },
    ],
    constants: [
    ],
    properties: [
        { export:true, name:'immunity_susceptible',
          type:'bool', value:'true',
                desc:"" },
        { export:true, name:'deletes_other_projectiles',
          type:'bool', value:'true',
                desc:"" },
        { export:true, name:'fizzle_on_ceiling',
          type:'bool', value:'false',
                desc:"" },
        { export:true, name:'movable',
          type:'bool', value:'true',
                desc:"" },
        { export:true, name:'can_be_hit_by_melee',
          type:'bool', value:'false',
                desc:"" },
        { export:true, name:'hit_cancel_on_hit',
          type:'bool', value:'false',
                desc:"" },
        { export:true, name:'free_cancel_on_hit',
          type:'bool', value:'false',
                desc:"" },
        { export:true, name:'apply_hitlag_when_hit_by_melee',
          type:'bool', value:'true',
                desc:"" },
        { export:true, name:'projectile_immune',
          type:'bool', value:'false',
                desc:"" },
        { export:true, name:'hitlag_modifier',
          type:'fixed', value:'"1.0"',
                desc:"" },
        { name:'got_parried',
          type:'bool', value:'false',
                desc:"" },
        { name:'stopped',
          type:'bool', value:'false',
                desc:"" },
    ],
    methods: [
        { name:'_ready',
          params:[],
                desc:"" },
        { name:'get_opponent',
          params:[], type:'get_p2',
                desc:"" },
        { name:'get_fighter',
          params:[], type:'get_p1',
                desc:"" },
        { name:'disable',
          params:[],
                desc:"" },
        { name:'on_got_parried',
          params:[],
                desc:"" },
        { name:'_process',
          params:['delta'],
                desc:"" },
        { name:'on_hit_ceiling',
          params:[],
                desc:"" },
        { name:'can_hit_cancel',
          params:['_fighter'], type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'hit_by',
          params:['hitbox'], type:'UNKNOWN_TYPE',
                desc:"" },
    ],
};

    Vue.createApp(ClassDocsComponent, data).mount("#page_main");
</script>