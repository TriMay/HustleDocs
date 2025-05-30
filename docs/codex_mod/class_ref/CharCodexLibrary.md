<div id="page_main"></div>


<script>

let data = {
    version: "1.9.20",
    updated: "2024-10-08",
    name: "CharCodexLibrary",
    inherits: "Node",
    script_path: "",
    scene_path: "",
    desc: "",
    signals: [
        { name:'achievement_unlocked',
          params:['achievement_list', 'achievement_id'],
                desc:"" },
    ],
    constants: [
        { name:'SAVE_DIR',
          type:'String', value:'"user://cloud/codex_char_saves"',
                desc:"" },
        { name:'LEGACY_SAVE_DIR',
          type:'String', value:'"user://codex_char_saves"',
                desc:"" },
        { name:'CODEX_SETTINGS_SAVE_PATH',
          type:'String', value:'"user://cloud/codex_settings.json"',
                desc:"" },
    ],
    properties: [
        { name:'codex_cache',
          type:'Dictionary', value:'{}',
                desc:"" },
        { name:'codex_save_data',
          type:'Dictionary', value:'{}',
                desc:"" },
        { name:'codex_achievements',
          type:'Dictionary', value:'{}',
                desc:"" },
        { name:'codex_has_options',
          type:'Dictionary', value:'{}',
                desc:"" },
        { name:'prefers_more_info',
          type:'bool', value:'false',
                desc:"" },
        { name:'preferred_tab',
          type:'String', value:'""',
                desc:"" },
        { name:'fixed',
          type:'FixedMath', value:'FixedMath.new()',
                desc:"" },
        { onready:true, name:'BlankCodexScene',
          type:'PackedScene', value:'load("res://_tri_char_codex/CodexPage.tscn")',
                desc:"" },
    ],
    methods: [
        { name:'_init',
          params:[],
                desc:"" },
        { name:'_ready',
          params:[],
                desc:"" },
        { name:'generate_node',
          params:['char_path:String'], type:'Node',
                desc:"" },
        { name:'generate_options_node',
          params:['char_path:String'], type:'Node',
                desc:"" },
        { name:'has_cached',
          params:['char_path:String'], type:'bool',
                desc:"" },
        { name:'can_generate',
          params:['char_path:String'], type:'bool',
                desc:"" },
        { name:'char_has_options',
          params:['char_path:String'], type:'bool',
                desc:"" },
        { name:'save_all_char_options',
          params:['fighter', 'value'], type:'bool',
                desc:"" },
        { name:'load_all_char_options',
          params:['fighter'], type:'Variant',
                desc:"" },
        { name:'save_codex_setting',
          params:['key:String', 'value'], type:'bool',
                desc:"" },
        { name:'load_codex_setting',
          params:['key:String'], type:'Variant',
                desc:"" },
        { name:'__attempt_load_char_instance',
          params:['char_path'], type:'Fighter',
                desc:"" },
        { name:'__attempt_load_codex_script',
          params:['char_path'], type:'Node',
                desc:"" },
        { name:'__get_codex_script_path',
          params:['char_path:String'], type:'String',
                desc:"" },
        { name:'__analyze_and_cache',
          params:['char_path:String'],
                desc:"" },
        { name:'__register_codex_override',
          params:['codex_data:CodexData'],
                desc:"" },
        { name:'__parse_instance_moveset',
          is_static:true, params:['char_instance:Node'], type:'Dictionary',
                desc:"" },
        { name:'__parse_moveset_visibility',
          is_static:true, params:['codex_data:CodexData'],
                desc:"" },
        { name:'__parse_hitbox_data_visibility',
          is_static:true, params:['state:CodexState'],
                desc:"" },
        { name:'array_has_any',
          is_static:true, params:['haystack:Array', 'needles:Array'], type:'bool',
                desc:"" },
        { name:'__parse_state_data',
          is_static:true, params:['state:StateInterface', 'char_instance:Node=null'], type:'CodexState',
                desc:"" },
        { name:'__parse_state_hitboxes',
          is_static:true, params:['state:StateInterface', 'char_instance:Node'], type:'Dictionary',
                desc:"" },
        { name:'__parse_hitbox_data',
          is_static:true, params:['hitbox:Hitbox', 'char_instance=null'], type:'CodexHitbox',
                desc:"" },
        { name:'__parse_is_hit_grab',
          is_static:true, params:['hitbox:Hitbox', 'char_instance:Node'], type:'bool',
                desc:"" },
        { name:'__parse_state_script_source',
          is_static:true, params:['state_data:CodexState', 'source_code:String'],
                desc:"" },
        { name:'code_keyphrase_test',
          is_static:true, params:['haystack:String', 'needle:String'], type:'bool',
                desc:"" },
        { name:'__generate_from_cache',
          params:['char_path:String'], type:'Node',
                desc:"" },
        { name:'__generate_error',
          params:['error:String'], type:'Node',
                desc:"" },
        { name:'load_for_extra',
          params:['fighter:Node', 'key=null', 'default=null', 'reload:bool=false'], type:'Variant',
                desc:"" },
        { name:'raw_load_char_data',
          params:['char_path:String', 'key=null', 'default=null'], type:'Variant',
                desc:"" },
        { name:'raw_save_char_data',
          params:['char_path:String', 'key=null', 'value=null'], type:'bool',
                desc:"" },
        { name:'init_char_data',
          params:['char_path:String'],
                desc:"" },
        { name:'raw_reset_char_data',
          params:['char_path:String'],
                desc:"" },
        { name:'get_new_char_data',
          params:['char_path:String'], type:'Dictionary',
                desc:"" },
        { name:'get_save_file_path',
          params:['char_path:String'], type:'String',
                desc:"" },
        { name:'get_legacy_save_file_path',
          params:['char_path:String'], type:'String',
                desc:"" },
        { name:'__cache_achievement_list',
          params:['char_path:String'],
                desc:"" },
        { name:'get_achievement_list',
          params:['char_path:String'], type:'CodexAchievementList',
                desc:"" },
        { name:'unlock_achievement',
          params:['fighter', 'achievement_id:String', 'multiplayer_only:bool=false'], type:'bool',
                desc:"" },
        { name:'relock_achievement',
          params:['fighter', 'achievement_id:String', 'multiplayer_only:bool=false'], type:'bool',
                desc:"" },
        { name:'is_achievement_unlocked',
          params:['fighter', 'achievement_id:String'], type:'bool',
                desc:"" },
        { name:'is_achievement_array_unlocked',
          params:['fighter', 'achievements:Array'], type:'bool',
                desc:"" },
        { name:'achievement_target_met',
          params:['fighter', 'achievement_id'], type:'bool',
                desc:"" },
        { name:'get_unlocked_achievements',
          params:['fighter'], type:'Array',
                desc:"" },
        { name:'increment_counter',
          params:['fighter', 'counter_id:String', 'by_amount:int=1', 'multiplayer_only:bool=false'], type:'int',
                desc:"" },
        { name:'set_counter',
          params:['fighter', 'counter_id:String', 'to_amount:int=1', 'multiplayer_only:bool=false'], type:'int',
                desc:"" },
        { name:'get_counter',
          params:['fighter', 'counter_id:String'], type:'int',
                desc:"" },
        { name:'__modify_style_data',
          params:['char_path', 'style_data'], type:'Dictionary',
                desc:"" },
        { name:'track_win',
          params:["fighter"],
                desc:"" },
        { name:'num_wins',
          params:["fighter"], type:'int',
                desc:"" },
        { name:'__on_game_started',
          params:[],
                desc:"" },
        { name:'__on_game_won',
          params:["winner", "game"],
                desc:"" },
        { name:'__on_game_forfeit',
          params:["loser", "game"],
                desc:"" },
    ],
};

    Vue.createApp(ClassDocsComponent, data).mount("#page_main");
</script>