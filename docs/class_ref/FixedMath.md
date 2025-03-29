# FixedMath
- class_name FixedMath
- script "res://lib/tbfg.dll"



---
## Method Descriptions

### func add
- func add(a:fixed, b:fixed) -> fixed

Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of ``a + b``.



### func sub
- func sub(a:fixed, b:fixed) -> fixed

Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of ``a - b``.



### func div
- func div(a:fixed, b:fixed) -> fixed

Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of ``a / b``.



### func mul
- func mul(a:fixed, b:fixed) -> fixed

Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of ``a * b``.



### func powu
- func powu(n:fixed, p:int) -> fixed

Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of ``n`` to the power of ``p``.

``p`` must be a positive integer.



### func eq
- func eq(a:fixed, b:fixed) -> bool

Returns ``true`` if ``a`` is equal to ``b``, otherwise returns ``false``.



### func gt
- func gt(a:fixed, b:fixed) -> bool

Returns ``true`` if ``a`` greater than ``b``, otherwise returns ``false``.



### func lt
- func lt(a:fixed, b:fixed) -> bool

Returns ``true`` if ``a`` less than ``b``, otherwise returns ``false``.



### func ge
- func ge(a:fixed, b:fixed) -> bool

Returns ``true`` if ``a`` greater than or equal to ``b``, otherwise returns ``false``.



### func le
- func le(a:fixed, b:fixed) -> bool

Returns ``true`` if ``a`` less than or equal to ``b``, otherwise returns ``false``.



### func round
- func round(n:fixed) -> int

Returns ``n`` rounded to the nearest integer number.



### func floor
- func floor(n:fixed) -> int

Returns ``n`` rounded down to the nearest integer number.



### func ceil
- func ceil(n:fixed) -> int

Returns ``n`` rounded up to the nearest integer number.



### func abs
- func abs(n:fixed) -> fixed

Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of the unsigned value of ``n``



### func sign
- func sign(n:fixed) -> int

Returns ``-1`` if ``n`` is negative, ``+1`` if ``n`` is positive, and ``0`` if `n` is 0



### func lerp_string
- func lerp_string(a:fixed, b:fixed, ratio:fixed) -> fixed

Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of some value between ``a`` and ``b``, where ``a`` is returned if ``ratio`` is "0.0", ``b`` is returned if ``ratio`` is "1.0", and the halfway point in between is returned if ``ratio`` is "0.5"



### func lerp_angle
- func lerp_angle(a:fixed, b:fixed, ratio:fixed) -> fixed

Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of some angle between the angle ``a`` and angle ``b``, where ``a`` is returned if ``ratio`` is "0.0", ``b`` is returned if ``ratio`` is "1.0", and the halfway point in between is returned if ``ratio`` is "0.5"



### func angle_dist
- func angle_dist(a:fixed, b:fixed) -> fixed

Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of the difference between two angles.



### func deg2rad
- func deg2rad(degrees:fixed) -> fixed

Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of ``degrees`` converted into radians



### func vec_to_angle
- func vec_to_angle(x:fixed, y:fixed) -> fixed

Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of the angle pointing towards a specified 2D vector



### func angle_to_vec
- func angle_to_vec(radians:fixed) -> Dictionary

Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) }, representing the normalized vector pointing towards the specified angle



### func rotate_vec
- func rotate_vec(x:fixed, y:fixed, radians:fixed) -> Dictionary

Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) } of the vector rotated by ``radians``.



### func vec_add
- func vec_add(x1:fixed, y1:fixed, x2:fixed, y2:fixed) -> Dictionary

Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) } of the sum of two 2D vectors.



### func vec_sub
- func vec_sub(x1:fixed, y1:fixed, x2:fixed, y2:fixed) -> Dictionary

Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) } of ``{x1, y1} - {x2, y2}``



### func vec_mul
- func vec_mul(x:fixed, y:fixed, mul:fixed) -> Dictionary

Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) } of a 2D Vector multiplied by ``mul``



### func vec_div
- func vec_div(x:fixed, y:fixed, div:fixed) -> Dictionary

Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) } of a 2D Vector divided by ``div``



### func vec_round
- func vec_round(x:fixed, y:fixed) -> Dictionary

Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) } of a 2D Vector with both x and y parts rounded to the nearest integer.



### func vec_len
- func vec_len(x:fixed, y:fixed) -> fixed

Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of the distance between the specified 2D vector and ``{x:"0", y:"0"}``



### func vec_len_squared
- func vec_len_squared(x:fixed, y:fixed) -> fixed

Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of ``x*x + y*y``, effectively the length of the vector squared. Useful for more efficiently comparing distances if the exact length is not needed, as this function will skip the square root calculation needed for vector length.



### func vec_dist
- func vec_dist(x1:fixed, y1:fixed, x2:fixed, y2:fixed) -> fixed

Returns a [fixed number string](class_ref/FixedMath.md?id=FixedMath) of the distance between two specified 2D vectors



### func normalized_vec
- func normalized_vec(x:fixed, y:fixed) -> Dictionary

Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) } of the specified 2D vector normalized (i.e. converted to a distance of 1 from ``{x:"0", y:"0"}`` towards the same angle)



### func normalized_vec_times
- func normalized_vec_times(x:fixed, y:fixed, length:fixed) -> Dictionary

Returns a Dictionary { 'x' : [fixed](class_ref/FixedMath.md), 'y' : [fixed](class_ref/FixedMath.md) } of the specified 2D vector converted to a distance of ``length`` from ``{x:"0", y:"0"}`` towards the same angle




---
## Constant Descriptions


---
## Signal Descriptions
