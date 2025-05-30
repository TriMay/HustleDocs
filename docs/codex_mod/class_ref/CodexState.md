<div id="page_main"></div>


<script>

let data = {
    version: "1.9.0",
    updated: "2024-04-03",
    name: "CodexState",
    inherits: "Reference",
    script_path: "",
    scene_path: "",
    desc: "",
    signals: [
    ],
    constants: [
    ],
    properties: [
        { name:'icon',
          type:'Texture', value:'null',
                desc:"" },
        { name:'title',
          type:'String', value:'""',
                desc:"" },
        { name:'desc',
          type:'String', value:'""',
                desc:"" },
        { name:'visible',
          type:'bool', value:'true',
                desc:"" },
        { name:'visibility_set',
          type:'bool', value:'false',
                desc:"" },
        { name:'type',
          type:'String', value:'""',
                desc:"" },
        { name:'air_type',
          type:'String', value:'""',
                desc:"" },
        { name:'length',
          type:'int', value:'-1',
                desc:"" },
        { name:'endless',
          type:'bool', value:'false',
                desc:"" },
        { name:'iasa',
          type:'int', value:'-1',
                desc:"" },
        { name:'anim_name',
          type:'String', value:'""',
                desc:"" },
        { name:'interrupt_types',
          type:'Array', value:'[]',
                desc:"" },
        { name:'stances',
          type:'Array', value:'[]',
                desc:"" },
        { name:'tags',
          type:'Array', value:'[]',
                desc:"" },
        { name:'change_stance',
          type:'String', value:'""',
                desc:"" },
        { name:'super_req',
          type:'int', value:'0',
                desc:"" },
        { name:'super_cost',
          type:'int', value:'0',
                desc:"" },
        { name:'hitbox_data',
          type:'Dictionary', value:'{}',
                desc:"" },
        { name:'tick_data',
          type:'Dictionary', value:'{}',
                desc:"" },
        { name:'custom_stats',
          type:'Dictionary', value:'{}',
                desc:"" },
    ],
    methods: [
        { name:'_init',
          params:['state=null'],
                desc:"" },
        { name:'define',
          params:['data=null'],
                desc:"" },
        { name:'duplicate',
          params:[], type:'CodexState',
                desc:"" },
        { name:'copy_to',
          params:['copy'],
                desc:"" },
        { name:'duplicate_all_hitbox_data',
          params:[], type:'Dictionary',
                desc:"" },
        { name:'parse_state',
          params:['state:StateInterface'],
                desc:"" },
        { name:'parse_dictionary',
          params:['data:Dictionary'],
                desc:"" },
        { name:'define_hitbox',
          params:['name:String', 'data', 'force_new:bool=false'],
                desc:"" },
        { name:'set_visible',
          params:['value:bool'],
                desc:"" },
        { name:'get_visible',
          params:[], type:'bool',
                desc:"" },
        { name:'set_interrupt_tick',
          params:['tick:int'],
                desc:"" },
        { name:'unset_interrupt_tick',
          params:['tick:int'],
                desc:"" },
        { name:'set_projectile_tick',
          params:['tick:int'],
                desc:"" },
        { name:'unset_projectile_tick',
          params:['tick:int'],
                desc:"" },
        { name:'set_start_armor_tick',
          params:['tick:int'],
                desc:"" },
        { name:'unset_start_armor_tick',
          params:['tick:int'],
                desc:"" },
        { name:'set_end_armor_tick',
          params:['tick:int'],
                desc:"" },
        { name:'unset_end_armor_tick',
          params:['tick:int'],
                desc:"" },
        { name:'set_start_invulnerability_tick',
          params:['tick:int'],
                desc:"" },
        { name:'unset_start_invulnerability_tick',
          params:['tick:int'],
                desc:"" },
        { name:'set_end_invulnerability_tick',
          params:['tick:int'],
                desc:"" },
        { name:'unset_end_invulnerability_tick',
          params:['tick:int'],
                desc:"" },
        { name:'set_start_projectile_invuln_tick',
          params:['tick:int'],
                desc:"" },
        { name:'unset_start_projectile_invuln_tick',
          params:['tick:int'],
                desc:"" },
        { name:'set_end_projectile_invuln_tick',
          params:['tick:int'],
                desc:"" },
        { name:'unset_end_projectile_invuln_tick',
          params:['tick:int'],
                desc:"" },
        { name:'set_start_grab_invuln_tick',
          params:['tick:int'],
                desc:"" },
        { name:'unset_start_grab_invuln_tick',
          params:['tick:int'],
                desc:"" },
        { name:'set_end_grab_invuln_tick',
          params:['tick:int'],
                desc:"" },
        { name:'unset_end_grab_invuln_tick',
          params:['tick:int'],
                desc:"" },
        { name:'set_start_aerial_invuln_tick',
          params:['tick:int'],
                desc:"" },
        { name:'unset_start_aerial_invuln_tick',
          params:['tick:int'],
                desc:"" },
        { name:'set_end_aerial_invuln_tick',
          params:['tick:int'],
                desc:"" },
        { name:'unset_end_aerial_invuln_tick',
          params:['tick:int'],
                desc:"" },
        { name:'set_start_grounded_invuln_tick',
          params:['tick:int'],
                desc:"" },
        { name:'unset_start_grounded_invuln_tick',
          params:['tick:int'],
                desc:"" },
        { name:'set_end_grounded_invuln_tick',
          params:['tick:int'],
                desc:"" },
        { name:'unset_end_grounded_invuln_tick',
          params:['tick:int'],
                desc:"" },
        { name:'set_gimmick_tick',
          params:['tick:int', 'text:String'],
                desc:"" },
        { name:'unset_gimmick_tick',
          params:['tick:int', 'text:String'],
                desc:"" },
        { name:'set_gimmick_tick_range',
          params:['start:int', 'end:int', 'text:String'],
                desc:"" },
        { name:'set_tick_item',
          params:['tick:int', 'type:String'],
                desc:"" },
        { name:'unset_tick_item',
          params:['tick:int', 'type:String'],
                desc:"" },
        { name:'parse_source_script',
          params:['source_code:String'],
                desc:"" },
        { name:'apply_known_script',
          params:['path:String'],
                desc:"" },
        { name:'script_has_keyphrase',
          is_static:true, params:['haystack:String', 'needle:String'], type:'bool',
                desc:"" },
    ],
};


    Vue.createApp(ClassDocsComponent, data).mount("#page_main");
</script>