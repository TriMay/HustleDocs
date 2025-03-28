<div id="page_main"></div>


<script>
    let data = {
        version: "1.9.0",
        updated: "2024-04-03",
        desc: "",
        name: "FixedMath",
        script_path: "res://lib/tbfg.dll",
        methods: [
            { name:'add', type:'fixed', params:['a:fixed', 'b:fixed'], desc:"Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of ``a + b``." },
            { name:'sub', type:'fixed', params:['a:fixed', 'b:fixed'], desc:"Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of ``a - b``." },
            { name:'div', type:'fixed', params:['a:fixed', 'b:fixed'], desc:"Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of ``a / b``." },
            { name:'mul', type:'fixed', params:['a:fixed', 'b:fixed'], desc:"Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of ``a * b``." },
            { name:'powu', type:'fixed', params:['n:fixed', 'p:int'], desc:"Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of ``n`` to the power of ``p``.\n\n``p`` must be a positive integer." },
        
            { name:'eq', type:'bool', params:['a:fixed', 'b:fixed'], desc:"Returns ``true`` if ``a`` is equal to ``b``, otherwise returns ``false``." },
            { name:'gt', type:'bool', params:['a:fixed', 'b:fixed'], desc:"Returns ``true`` if ``a`` greater than ``b``, otherwise returns ``false``." },
            { name:'lt', type:'bool', params:['a:fixed', 'b:fixed'], desc:"Returns ``true`` if ``a`` less than ``b``, otherwise returns ``false``." },
            { name:'ge', type:'bool', params:['a:fixed', 'b:fixed'], desc:"Returns ``true`` if ``a`` greater than or equal to ``b``, otherwise returns ``false``." },
            { name:'le', type:'bool', params:['a:fixed', 'b:fixed'], desc:"Returns ``true`` if ``a`` less than or equal to ``b``, otherwise returns ``false``." },
            
            { name:'round', type:'int', params:['n:fixed'], desc:"Returns ``n`` rounded to the nearest integer number." },
            { name:'floor', type:'int', params:['n:fixed'], desc:"Returns ``n`` rounded down to the nearest integer number." },
            { name:'ceil', type:'int', params:['n:fixed'], desc:"Returns ``n`` rounded up to the nearest integer number." },
            { name:'abs', type:'fixed', params:['n:fixed'], desc:"Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of the unsigned value of ``n``" },
            { name:'sign', type:'int', params:['n:fixed'], desc:"Returns ``-1`` if ``n`` is negative, ``+1`` if ``n`` is positive, and ``0`` if `n` is 0" },
            
            { name:'lerp_string', type:'fixed', params:['a:fixed', 'b:fixed', 'ratio:fixed'], desc:"Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of some value between ``a`` and ``b``, where ``a`` is returned if ``ratio`` is \"0.0\", ``b`` is returned if ``ratio`` is \"1.0\", and the halfway point in between is returned if ``ratio`` is \"0.5\"" },
            { name:'lerp_angle', type:'fixed', params:['a:fixed', 'b:fixed', 'ratio:fixed'], desc:"Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of some angle between the angle ``a`` and angle ``b``, where ``a`` is returned if ``ratio`` is \"0.0\", ``b`` is returned if ``ratio`` is \"1.0\", and the halfway point in between is returned if ``ratio`` is \"0.5\"" },
            { name:'angle_dist', type:'fixed', params:['a:fixed', 'b:fixed'], desc:"Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of the difference between two angles." },
            { name:'deg2rad', type:'fixed', params:['degrees:fixed'], desc:"Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of ``degrees`` converted into radians" },
            { name:'vec_to_angle', type:'fixed', params:['x:fixed', 'y:fixed'], desc:"Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of the angle pointing towards a specified 2D vector" },
            { name:'angle_to_vec', type:'Dictionary', params:['radians:fixed'], desc:"Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) }, representing the normalized vector pointing towards the specified angle" },
            
            { name:'rotate_vec', type:'Dictionary', params:['x:fixed', 'y:fixed', 'radians:fixed'], desc:"Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) } of the vector rotated by ``radians``." },
            { name:'vec_add', type:'Dictionary', params:['x1:fixed', 'y1:fixed', 'x2:fixed', 'y2:fixed'], desc:"Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) } of the sum of two 2D vectors." },
            { name:'vec_sub', type:'Dictionary', params:['x1:fixed', 'y1:fixed', 'x2:fixed', 'y2:fixed'], desc:"Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) } of ``{x1, y1} - {x2, y2}``" },
            { name:'vec_mul', type:'Dictionary', params:['x:fixed', 'y:fixed', 'mul:fixed'], desc:"Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) } of a 2D Vector multiplied by ``mul``" },
            { name:'vec_div', type:'Dictionary', params:['x:fixed', 'y:fixed', 'div:fixed'], desc:"Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) } of a 2D Vector divided by ``div``" },
            { name:'vec_round', type:'Dictionary', params:['x:fixed', 'y:fixed'], desc:"Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) } of a 2D Vector with both x and y parts rounded to the nearest integer." },
            
            { name:'vec_len', type:'fixed', params:['x:fixed', 'y:fixed'], desc:"Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of the distance between the specified 2D vector and ``{x:\"0\", y:\"0\"}``" },
            { name:'vec_len_squared', type:'fixed', params:['x:fixed', 'y:fixed'], desc:"Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of ``x*x + y*y``, effectively the length of the vector squared.  Useful for more efficiently comparing distances if the exact length is not needed, as this function will skip the square root calculation needed for vector length." },
            { name:'vec_dist', type:'fixed', params:['x1:fixed', 'y1:fixed', 'x2:fixed', 'y2:fixed'], desc:"Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of the distance between two specified 2D vectors" },
            { name:'normalized_vec', type:'Dictionary', params:['x:fixed', 'y:fixed'], desc:"Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) } of the specified 2D vector normalized (i.e. converted to a distance of 1 from ``{x:\"0\", y:\"0\"}`` towards the same angle)" },
            { name:'normalized_vec_times', type:'Dictionary', params:['x:fixed', 'y:fixed', 'length:fixed'], desc:"Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) } of the specified 2D vector converted to a distance of ``length`` from ``{x:\"0\", y:\"0\"}`` towards the same angle" },
            
        ],
    };


    Vue.createApp(ClassDocsComponent, data).mount("#page_main");
</script>