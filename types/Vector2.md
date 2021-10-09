# Vector2

{% hint style="info" %}
`Vector2` is a two-dimensional vector. For standard three-dimensional vectors refer to `Vector`.
{% endhint %}

## Functions

## new

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| instance | Vector2 | New instance of a Vector2 |

```lua
local my_vec2 = Vector2.new()
```

## new

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| x | float | x value |
| y | float | y value |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| instance | Vector2 | New instance of a Vector2 |

```lua
local my_vec2 = Vector2.new(1.0, 2.0)
```

## Arithmetics:

### add

#### Usage:

```lua
local vec1 = Vector2.new(1.0, 2.0)
local vec2 = Vector2.new(3.0, 2.0)
local add = vec1 + vec2
-- Expected value of add: Vec(4.0, 4.0)
```

### sub

#### Usage:

```lua
local vec1 = Vector2.new(4.0, 2.0)
local vec2 = Vector2.new(2.0, 1.0)
local sub = vec1 - vec2
-- Expected value of sub: Vec(2.0, 1.0)
```

### mul

#### Usage:

```lua
local vec1 = Vector2.new(1.0, 2.0)
local vec2 = Vector2.new(3.0, 2.0)
local mul = vec1 * vec2
-- Expected value of mul: Vec(3.0, 4.0)
```

### div

#### Usage:

```lua
local vec1 = Vector2.new(6.0, 2.0)
local vec2 = Vector2.new(3.0, 2.0)
local div = vec1 / vec2
-- Expected value of div: Vec(2.0, 1.0)
```

### len

#### Usage:

```lua
local vec1 = Vector2.new(1.0, 2.0)
local len = #vec1
-- Expected value of len: sqrt(1^2 + 2^2) = 2.2360
```

## Length

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| length | float | Vector length|

#### Usage:

```lua
local my_vec = Vector2.new(3.0, 2.0)
local length = my_vec:Length()
```

## Fields:

| Name | Type | Description |
| :--- | :--- | :--- |
| x | float | x value |
| y | float | y value |
