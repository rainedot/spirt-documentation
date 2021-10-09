# Vector

{% hint style="info" %}
`Vector` is a standard three-dimensional vector. For two-dimensional vectors refer to `Vector2`.
{% endhint %}

## Functions

## new

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| instance | Vector | New instance of a Vector |

```lua
local my_vec = Vector.new()
```

## new

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| x | float | x value |
| y | float | y value |
| z | float | z value |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| instance | Vector | New instance of a Vector |

```lua
local my_vec = Vector.new(2.0, 3.0, 9.0)
```

## Arithmetics:

### add

#### Usage:

```lua
local vec1 = Vector.new(1.0, 2.0, 3.0)
local vec2 = Vector.new(3.0, 2.0, 1.0)
local add = vec1 + vec2
-- Expected value of add: Vec(4.0, 4.0, 4.0)
```

### sub

#### Usage:

```lua
local vec1 = Vector.new(4.0, 2.0, 6.0)
local vec2 = Vector.new(2.0, 1.0, 2.0)
local sub = vec1 - vec2
-- Expected value of sub: Vec(2.0, 1.0, 4.0)
```

### mul

#### Usage:

```lua
local vec1 = Vector.new(1.0, 2.0, 3.0)
local vec2 = Vector.new(3.0, 2.0, 1.0)
local mul = vec1 * vec2
-- Expected value of mul: Vec(3.0, 4.0, 3.0)
```

### div

#### Usage:

```lua
local vec1 = Vector.new(6.0, 2.0, 3.0)
local vec2 = Vector.new(3.0, 2.0, 1.0)
local div = vec1 / vec2
-- Expected value of div: Vec(2.0, 1.0, 3.0)
```

### len

#### Usage:

```lua
local vec1 = Vector.new(1.0, 2.0, 3.0)
local len = #vec1
-- Expected value of len: sqrt(1^2 + 2^2 + 3^2) = 3.741
```

## Length

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| length | float | Vector length|

#### Usage:

```lua
local my_vec = Vector.new(3.0, 2.0, 8.0)
local length = my_vec:Length()
```

## Length2D

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| length | float | Vector length|

#### Usage:

```lua
local my_vec = Vector.new(3.0, 2.0, 8.0)
local length = my_vec:Length2D()
--Expected value for length: sqrt(3^2 + 2^2) = 3.6055
```

## DistTo

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| dist | float | Distance between self and another vector|

#### Usage:

```lua
local my_vec = Vector.new(3.0, 2.0, 8.0)
local dest = Vector.new(6.0, 4.0, 16.0)
local length = my_vec:DistTo(dest)
```

## Dot

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| dot | float | Dot product of two vectors |

#### Usage:

```lua
local my_vec = Vector.new(3.0, 2.0, 8.0)
local my_vec2 = Vector.new(4.0, 3.0, 1.0)
local dot = my_vec:Dot(my_vec2)
-- Expected value for dot: ((3.0 * 4.0) + (2.0 * 3.0) + (8.0 * 1.0)) = (12 + 6 + 8) = 26
```

## Cross

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| cross | Vector | Cross product of two vectors |

#### Usage:

```lua
local my_vec = Vector.new(3.0, 2.0, 8.0)
local my_vec2 = Vector.new(4.0, 3.0, 1.0)
local dot = my_vec:Cross(my_vec2)
```

## Fields:

| Name | Type | Description |
| :--- | :--- | :--- |
| x | float | x value |
| y | float | y value |
| z | float | z value |

```lua
local my_vec = Vector.new(1.0, 2.0, 3.0);
local x = my_vec.x --1.0
local y = my_vec.y --2.0
local z = my_vec.z --3.0
```
