# Members
```julia
abstract type Approximation end
```

```julia
x::Vector{Int}
y::Vector{Int}
id::Vector{Int}
```
# Actions

- For domain operators
```julia
get_number_of_dimensions()
# get_integration_points_and_weights()
get_jacobe()
get_shape_functions()
get_gradients_of_shape_functions()
get_2nd_gradients_of_shape_functions()
# get_3rd_gradients_of_shape_functions()
```