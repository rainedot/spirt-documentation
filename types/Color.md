# Color

{% hint style="info" %}
RGBA values are clamped fractions from `0.0` to `1.0`
{% endhint %}

## Functions

## new

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| instance | Color | New instance of Color |

```lua
local clr = Color.new()
```

## new

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| r | float | Red (0.0 - 1.0) | + |
| g | float | Green (0.0 - 1.0) | + |
| b | float | Blue (0.0 - 1.0) | + |
| a | float | Alpha (0.0 - 1.0) | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| instance | Color | New instance of a Color |

```lua
local my_clr = Color.new(1.0, 1.0, 1.0)
```

## RGBA

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| r | int | Red (0 - 255) | + |
| g | int | Green (0 - 255) | + |
| b | int | Blue (0 - 255) | + |
| a | int | Alpha (0 - 255) | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| instance | Color | New instance of a Color |

```lua
local my_clr = Color.RGBA(255, 100, 255, 255)
```

## HSLA

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| h | float | Hue (0.0 - 1.0) | + |
| s | float | Saturation (0.0 - 1.0) | + |
| l | float | Lightness (0.0 - 1.0) | + |
| a | float | Alpha (0.0 - 1.0) | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| instance | Color | New instance of a Color |

```lua
local my_clr = Color.HSLA(0.5, 0.5, 0.5, 1.0)
```

## Fields:

| Name | Type | Description |
| :--- | :--- | :--- |
| r | float | Fraction from 0.0 to 1.0 |
| g | float | Fraction from 0.0 to 1.0 |
| b | float | Fraction from 0.0 to 1.0 |
| a | float | Fraction from 0.0 to 1.0 |
