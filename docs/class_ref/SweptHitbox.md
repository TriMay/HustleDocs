[](../wip.md ':include')

<div id="page_main"></div>


<script>

let data = {
    version: "1.8.18",
    name: "SweptHitbox",
    inherits: "Hitbox",
    script_path: "res://mechanics/SweptHitbox.gd",
    desc: "",
    signals: [
    ],
    constants: [
    ],
    properties: [
        { export:true, name:'_c_Raycast',
          type:'int', value:'0',
                desc:"" },
        { export:true, name:'to_x',
          type:'int', value:'0',
                desc:"" },
        { export:true, name:'to_y',
          type:'int', value:'0',
                desc:"" },
    ],
    methods: [
        { name:'func _fixed_clamp(',
          type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'func _fixed_max(',
          type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'func _fixed_min(',
          type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'_aabb_intersect',
          params:['aabb:Dictionary'], type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'_seg_seg_intersect',
          params:['start:int', 'delta:int', 'padding:int', 'n1:int', 'n2:int'], type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'_seg_rect_intersect',
          params:['box:CollisionBox'], type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'_seg_rect_test',
          params:['box:CollisionBox'], type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'_seg_rect_delta',
          params:['box:CollisionBox'], type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'get_sweep_center',
          params:[], type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'get_sweep_center_float',
          params:[], type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'to_x_facing',
          params:[], type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'get_aabb',
          params:[],
                desc:"" },
        { name:'overlaps',
          params:['box:CollisionBox'], type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'box_draw',
          params:[], type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'spawn_whiff_particle',
          params:[],
                desc:"" },
        { name:'get_center',
          params:[], type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'get_center_float',
          params:[], type:'UNKNOWN_TYPE',
                desc:"" },
        { name:'get_overlap_center_float',
          params:['box:CollisionBox'], type:'UNKNOWN_TYPE',
                desc:"" },
    ],
};



    Vue.createApp(ClassDocsComponent, data).mount("#page_main");
</script>