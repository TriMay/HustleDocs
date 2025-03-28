# Utils
- class_name Utils
- extends Node
- script "res://framework/utils.gd"


-----
## Method Descriptions

### func filter_filename
- func filter_filename(text) -> String

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func int_abs
- func int_abs(n:int) -> int

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_copiable_properties
- func get_copiable_properties(node:Node) -> Array

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func int_sign
- func int_sign(n:int) -> int

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func int_sign2
- func int_sign2(n:int) -> int

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func frames
- func frames(n, fps:int=60) -> float

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func split_lines
- func split_lines(string) -> Array

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func int_clamp
- func int_clamp(n:int, min_:int, max_:int) -> int

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func int_min
- func int_min(n1:int, n2:int) -> int

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func int_max
- func int_max(n1:int, n2:int) -> int

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func starts_with
- func starts_with(string:String, pattern:String) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func map
- func map(value, istart, istop, ostart, ostop) -> float

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func map_int
- func map_int(value:int, istart:int, istop:int, ostart:int, ostop:int) -> int

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func map_pow
- func map_pow(value, istart, istop, ostart, ostop, power) -> float

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func tree_set_all_process
- func tree_set_all_process(p_node:Node, p_active:bool, p_self_too:bool=false)

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func snap
- func snap(value, step) -> float

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func approach
- func approach(a, b, amount) -> float

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func int_lerp
- func int_lerp(a:int, b:int, f:int) -> int

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_closest_node
- func get_closest_node(node:Node2D, node_list:Array) -> Node2D

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_first_player
- func get_first_player(node) -> Node

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func ang2vec
- func ang2vec(angle) -> Vector2

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_angle_from_to
- func get_angle_from_to(node, position) -> float

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func angle_diff
- func angle_diff(from, to) -> float

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func comma_sep
- func comma_sep(number) -> String

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func float_time
- func float_time() -> float

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func wave
- func wave(from, to, duration, offset:int=0) -> float

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func pulse
- func pulse(duration:float=1.0, width:float=0.5) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func remove_duplicates
- func remove_duplicates(array:Array) -> Array

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func is_in_circle
- func is_in_circle(point:Vector2, circle_center:Vector2, circle_radius:float) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func veci_distance_to
- func veci_distance_to(start:Vector2, end:Vector2) -> Vector2

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func veci_to_vec
- func veci_to_vec(veci:Vector2) -> Vector2

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func sin_0_1
- func sin_0_1(value) -> float

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func veci_length
- func veci_length(v:Vector2) -> Vector2

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func clamp_cell
- func clamp_cell(cell:Vector2, map:Array2D) -> Vector2

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func stepify
- func stepify(s, step) -> float

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func line
- func line(start:Vector2, end:Vector2) -> Array

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func random_triangle_point
- func random_triangle_point(a, b, c) -> float

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func triangle_area
- func triangle_area(a, b, c) -> float

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_polygon_bounding_box
- func get_polygon_bounding_box(polygon:PoolVector2Array) -> Rect2

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func distance_to_line_segment
- func distance_to_line_segment(xy1, xy2, xy3) -> float

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func is_point_in_capsule
- func is_point_in_capsule(p:Vector2, xy1:Vector2, xy2:Vector2, radius:float) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func spring
- func spring(x:float, v:float, xt:float, zeta:float, omega:float, h:float) -> Array

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func compare
- func compare(val1, val2) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func pass_signal_along
- func pass_signal_along(from:Node, to:Node, signal_name, to_signal_name:String="")

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func vector_spring
- func vector_spring(vec:Vector2, vel:Vector2, target:Vector2, zeta:float, omega:float, h:float) -> Array

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func fixed_vec2_string
- func fixed_vec2_string(x:String, y:String) -> Dictionary

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func is_mouse_in_control
- func is_mouse_in_control(control:Control) -> bool

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func number_from_string
- func number_from_string(string) -> int

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### func get_files_in_folder
- func get_files_in_folder(folder:String, extension:String="") -> Array

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



-----
## Constant Descriptions

### const cardinal_dirs
- const cardinal_dirs : Array = [Vector2(1, 0), Vector2(0, 1), Vector2( - 1, 0), Vector2(0, - 1)]

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### const diagonal_dirs
- const diagonal_dirs : Array = [Vector2(1, 1), Vector2(1, - 1), Vector2( - 1, - 1), Vector2( - 1, 1)]

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### const dirs
- const dirs : Array = [Vector2(1, 0), Vector2(0, 1), Vector2( - 1, 0), Vector2(0, - 1), Vector2(1, 1), Vector2(1, - 1), Vector2( - 1, - 1), Vector2( - 1, 1)]

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')



### const INVALID_FILE_CHARS
- const INVALID_FILE_CHARS : String = "<>:/\\|?*"

[](https://hustledocs.trimaydev.com/docs/missing-description.md ':include')
