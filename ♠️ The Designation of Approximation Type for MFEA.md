# Members
```julia
abstract type Approximation end
```

```julia
x::Vector{Int}
y::Vector{Int}
id::Vector{Int}
integration_points_and_weights::Pair{Vector{Float64},Float64}
```
# Actions

- For domain operators
```julia
get_number_of_dimensions()
# get_integration_points_and_weights()
get_jacobe()
get_shape_functions()
```

