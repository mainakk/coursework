# Code Cleanup Guide and Change Log

This record documents readability edits to the embedded MATLAB transcriptions and conventions for future coursework imports. The notebooks are canonical; reconstructed `.m` sources are embedded and generated only temporarily for execution.

## Rules for future imports

- Preserve source files, equations, objective functions, constraints, starting values, solver choice, loop order, and historical variants. Do not repair suspected errors during a readability pass; document them for review or put alternatives in a separate experiment.
- Rename cryptic variables when their meaning is clear from code or source material. Prefer physical concepts such as coordinates, lengths, bounds, objective values, and optimizer results. Retain mathematical notation when it directly matches an equation and is easier to read.
- Retain names required by MATLAB/Octave callback interfaces. Avoid renaming functions/files unless every call site and embedded path can be updated consistently.
- Add only brief comments for non-obvious model structure, packed-vector layouts, callback requirements, or preserved anomalies. Avoid comments that merely repeat code.
- Update notebook source cells, refresh saved runtime output, report failures and non-convergence honestly, and validate notebook JSON and embedded-source completeness.
- For each imported assignment, append the input provenance, affected notebook/source cells, renamed identifiers, comments added, and unresolved concerns below.

## Current readability pass

Only identifier names and explanatory comments were intentionally changed; no formulation or algorithm change was intended. MATLAB callback outputs such as `c` and `ceq` remain unchanged where required.

Source PDFs: HW1 `originals/2011/VMSO_assignment1/codes.pdf`; HW2
`originals/2011/vmso hw2/code2.pdf`; HW3
`originals/2011/vmso3/code3.pdf` and `originals/2011/vmso31/code3.pdf`.

### Assignment 1

- `problem-1/HW1_1_1.m`: `constraint_bounds` → `inequality_limits`.
- `problem-1/tran.m`: `x` → `design_variables`, `f` → `objective_value`.
- `problem-1/outfun.m`: `x` → `design_variables`, `optimValues` → `optimizer_values`, `state` → `callback_state`.
- `problem-1/outfun1.m`: `x` → `design_variables`, `optimValues` → `optimizer_values`, `state` → `callback_state`.
- `problem-1/outfun2.m`: `x` → `design_variables`, `optimValues` → `optimizer_values`, `state` → `callback_state`.
- `river-fence/river_fence.m`: `n` → `segment_count`, `Area` → `target_area`, `ymax` → `river_intercept`, `xmaxx` → `river_horizontal_span`, `xminn` → `river_start_x`, `slope` → `river_slope`, `lb` → `lower_bounds`, `y0` → `initial_design`, `A` → `linear_constraint_matrix`, `b` → `linear_constraint_limits`, `y` → `optimized_design`, `fval` → `fence_length`, `exitflag` → `exit_flag`, `output` → `solver_output`.
- `river-fence/river1.m`: `n` → `segment_count`, `y` → `design`, `f` → `fence_length`, `k` → `segment_index`.
- `river-fence/area.m`: `n` → `segment_count`, `Area` → `target_area`, `y` → `design`.
- `problem-1/HW1_1_1.m`: optimizer vector `x` became `design_variables`, and optimizer output `fval` became `objective_value`; scalar contour variables `x` and `y` remain mathematical symbols.

### Assignment 2

- `reflection-geometry/geometry1.m`: `theta` → `mirror_angle`, `x` → `source_point`, `y` → `destination_point`, `a` → `mirror_radius`, `p` → `reflection_points`, `d` → `total_path_length`, `m1` → `source_ray_slope`, `m2` → `destination_ray_slope`, `m` → `mirror_tangent_slope`, `i` → `incidence_angle`, `r` → `reflection_angle`.
- `plane-mirror/Reflection_PlaneMirror_2D.m`: `x` → `source_point`, `y` → `destination_point`, `m` → `mirror_slope`, `c` → `mirror_intercept`, `M` → `mirror_equation`, `z0` → `initial_reflection_point`, `z` → `reflection_point`, `fval` → `path_length`, `exitflag` → `exit_flag`, `xmin` → `plot_x_min`, `xmax` → `plot_x_max`, `ymin` → `plot_y_min`, `ymax` → `plot_y_max`.
- `plane-mirror/reflection.m`: `x` → `source_point`, `y` → `destination_point`, `z` → `reflection_point`, `d` → `total_path_length`.
- `spherical-mirror/Reflection_SphericalMirror.m`: `x` → `source_point`, `y` → `destination_point`, `a` → `mirror_radius`, `M` → `mirror_equation`, `theta0` → `initial_mirror_angle`, `theta_dmin` → `minimum_path_angle`, `dmin` → `minimum_path_length`, `theta_dmax` → `maximum_path_angle`, `dmax_neg` → `negative_maximum_path_length`, `exitflag` → `optimizer_exit_flag`, `z_dmin` → `minimum_reflection_point`, `z_dmax` → `maximum_reflection_point`.
- `spherical-mirror/reflection_spherical.m`: `x` → `source_point`, `y` → `destination_point`, `a` → `mirror_radius`, `theta` → `mirror_angle`, `f` → `path_length`.
- `spherical-mirror/reflection_spherical1.m`: `x` → `source_point`, `y` → `destination_point`, `a` → `mirror_radius`, `theta` → `mirror_angle`, `f` → `negative_path_length`.
- `cylindrical-mirror/Reflection_Cylindrical.m`: `x` → `source_point`, `y` → `destination_point`, `a` → `cylinder_radius`, `z0` → `initial_reflection_parameters`, `z_dmin` → `minimum_reflection_parameters`, `dmin` → `minimum_path_length`, `z_dmax` → `maximum_reflection_parameters`, `dmax_neg` → `maximum_search_objective`, `exitflag` → `optimizer_exit_flag`, `X` → `surface_x`, `Y` → `surface_y`, `Z` → `surface_z`.
- `cylindrical-mirror/Reflection_Cylindrical_Extern.m`: `x` → `source_point`, `y` → `destination_point`, `a` → `cylinder_radius`, `z0` → `initial_reflection_parameters`, `z_dmin` → `minimum_reflection_parameters`, `dmin` → `minimum_path_length`, `z_dmax` → `maximum_reflection_parameters`, `dmax_neg` → `maximum_search_objective`, `exitflag` → `optimizer_exit_flag`, `X` → `surface_x`, `Y` → `surface_y`, `Z` → `surface_z`, `incident_angle` → `incidence_angle`.
- `cylindrical-mirror/reflection_cylinder.m`: `x` → `source_point`, `y` → `destination_point`, `a` → `cylinder_radius`, `z` → `reflection_parameters`, `f` → `path_length`.
- `cylindrical-mirror/reflection_cylinder1.m`: `x` → `source_point`, `y` → `destination_point`, `a` → `cylinder_radius`, `z` → `reflection_parameters`, `g` → `path_length`, `f` → `reciprocal_path_objective`.
- `plane-refraction/refraction_plane.m`: `x` → `source_point`, `y` → `destination_point`, `cx` → `source_medium_speed`, `cy` → `destination_medium_speed`, `cpos` → `positive_side_speed`, `cneg` → `negative_side_speed`, `m1` → `endpoint_line_slope`, `c1` → `endpoint_line_intercept`, `z0` → `initial_refraction_point`, `sgnx` → `source_side_distance`, `sgny` → `destination_side_distance`, `m` → `interface_slope`, `c` → `interface_intercept`, `M` → `interface_equation`, `z` → `refraction_point`, `fval` → `travel_time`, `exitflag` → `exit_flag`.
- `plane-refraction/refraction.m`: `x` → `source_point`, `y` → `destination_point`, `cx` → `source_medium_speed`, `cy` → `destination_medium_speed`, `z` → `refraction_point`, `t` → `travel_time`.
- `cylindrical-mirror/reflection_cylinder1.m`: a short comment flags the source’s use of `source_point(3)` in the second endpoint term; the formula is preserved.

### Assignment 3

- `vmso3/wire2d_simulation.m`: `n` → `segment_count`, `d` → `segment_length`, `zeta` → `initial_x_positions`, `head_movement` → `endpoint_vertical_position`, `L` → `wire_length`, `theta0` → `initial_segment_angles`, `theta` → `optimal_segment_angles`, `f` → `objective_value`, `exitflag` → `optimizer_exit_flag`, `options` → `solver_output`, `x` → `x_coordinates`, `y` → `y_coordinates`, `i` → `point_index`, `j` → `segment_index`.
- `vmso3/wire2d.m`: `n` → `segment_count`, `d` → `segment_length`, `zeta` → `initial_x_positions`, `head_movement` → `endpoint_vertical_position`, `theta` → `segment_angles`, `x` → `x_coordinates`, `y` → `y_coordinates`, `k` → `point_index`, `f` → `displacement_norm`.
- `vmso3/cloth_simulation.m`: `n` → `mesh_subdivisions`, `d` → `mesh_edge_length`, `zeta` → `initial_x_grid`, `eta` → `initial_y_grid`, `corner_movement` → `corner_height`, `k` → `column_indices`, `l` → `row_indices`, `L` → `cloth_length`, `Aeq` → `fixed_node_constraint_matrix`, `beq` → `fixed_node_constraint_values`, `r0` → `initial_node_coordinates`, `r` → `optimized_node_coordinates`, `fval` → `objective_value`, `exitflag` → `optimizer_exit_flag`, `output` → `solver_output`, `x` → `x_coordinates`, `y` → `y_coordinates`, `z` → `z_coordinates`, `i` → `outer_grid_index`, `j` → `inner_grid_index`.
- `vmso3/cloth.m`: `n` → `mesh_subdivisions`, `zeta` → `initial_x_grid`, `eta` → `initial_y_grid`, `k` → `column_indices`, `l` → `row_indices`, `r` → `node_coordinates`, `f` → `displacement_norm`, `i` → `node_index`.
- `vmso3/dist.m`: `n` → `mesh_subdivisions`, `d` → `mesh_edge_length`, `r` → `node_coordinates`, `k` → `constraint_index`, `i` → `inner_grid_index`, `j` → `outer_grid_index`.
- `vmso31/wire2d_simulation.m`: `n` → `segment_count`, `d` → `segment_length`, `zeta` → `initial_x_positions`, `head_movement` → `endpoint_vertical_position`, `L` → `wire_length`, `theta0` → `initial_segment_angles`, `theta` → `optimal_segment_angles`, `f` → `objective_value`, `exitflag` → `optimizer_exit_flag`, `options` → `solver_output`, `x` → `x_coordinates`, `y` → `y_coordinates`, `i` → `point_index`, `j` → `segment_index`.
- `vmso31/wire2d.m`: `n` → `segment_count`, `d` → `segment_length`, `zeta` → `initial_x_positions`, `head_movement` → `endpoint_vertical_position`, `theta` → `segment_angles`, `x` → `x_coordinates`, `y` → `y_coordinates`, `k` → `point_index`, `f` → `displacement_norm`.
- `vmso31/cloth_simulation.m`: `n` → `mesh_subdivisions`, `d` → `mesh_edge_length`, `zeta` → `initial_x_grid`, `eta` → `initial_y_grid`, `corner_movement` → `corner_height`, `k` → `column_indices`, `l` → `row_indices`, `L` → `cloth_length`, `Aeq` → `fixed_node_constraint_matrix`, `beq` → `fixed_node_constraint_values`, `r0` → `initial_node_coordinates`, `r` → `optimized_node_coordinates`, `fval` → `objective_value`, `exitflag` → `optimizer_exit_flag`, `output` → `solver_output`, `x` → `x_coordinates`, `y` → `y_coordinates`, `z` → `z_coordinates`, `i` → `outer_grid_index`, `j` → `inner_grid_index`.
- `vmso31/cloth.m`: `n` → `mesh_subdivisions`, `zeta` → `initial_x_grid`, `eta` → `initial_y_grid`, `k` → `column_indices`, `l` → `row_indices`, `r` → `node_coordinates`, `f` → `displacement_norm`, `i` → `node_index`.
- `vmso31/dist.m`: `n` → `mesh_subdivisions`, `d` → `mesh_edge_length`, `r` → `node_coordinates`, `k` → `constraint_index`, `i` → `inner_grid_index`, `j` → `outer_grid_index`.
- Both cloth simulations now describe the pinned corner and packed x/y/z coordinate blocks. Both distance functions note that the original single-step diagonal constraint index advance is preserved.

## Validation and known limitations

All assignment entry points were run after renaming with GNU Octave 11.3.0 and `optim` 1.6.3; refreshed output is stored in each notebook. Assignment 1’s reciprocal optimization completes while river-fence reaches its iteration limit. All six Assignment 2 entry points execute. Assignment 3 wire optimizations reach their iteration limits and both cloth optimizations fail in Octave. These are not reported as converged solutions; MATLAB/Optimization Toolbox may behave differently.

## Follow-up readability refinements

- Assignment 1, `problem-1/HW1_1_1.m`: `f` → `objective_contour`; `g1`–`g5` → `constraint_variable_sum`, `constraint_weighted_sum`, `constraint_third_linear`, `nonnegative_first_variable`, and `nonnegative_second_variable`.
- Assignment 2, `spherical-mirror/Reflection_SphericalMirror.m`: misspelled `incindent_angle_dmin`/`incindent_angle_dmax` and abbreviated `reflection_angle_dmin`/`reflection_angle_dmax` → `incidence_angle_minimum_path`, `incidence_angle_maximum_path`, `reflection_angle_minimum_path`, and `reflection_angle_maximum_path`.
- Assignment 2, `cylindrical-mirror/Reflection_Cylindrical.m` and `Reflection_Cylindrical_Extern.m`: angle result variables ending in `_dmin`/`_dmax` → names ending in `_minimum_path`/`_maximum_path`; `incident_angle` → `incidence_angle`.
- Assignment 2, `plane-refraction/refraction_plane.m`: `xmin`, `xmax`, `ymin`, `ymax` → `plot_x_min`, `plot_x_max`, `plot_y_min`, `plot_y_max`.
- Assignment 2, plane/spherical mirror and refraction entry points: anonymous plot-equation parameters now use `mirror_x`/`mirror_y` or `interface_x`/`interface_y` rather than names that imply whole endpoint vectors. Their equations are unchanged.
- Assignment 3, `vmso3/wire2d.m` and `vmso31/wire2d.m`: loop index `j` → `segment_index`.
- Comments added: explain the pinned cloth corner and packed x/y/z optimizer vector; flag the preserved diagonal-constraint index advance and suspicious cylindrical maximum-path formula.
- Refreshed all stored Octave outputs after these refinements.
