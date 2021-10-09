# Render

## Functions

## Line

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| start | Vector2 | Startpoint of the line |
| end | Vector2 | Endpoint of the line |
| clr | Color | Linecolor |

### Usage:

```lua
Render.Line(Vector2.new(0.0, 0.0), Vector2.new(5.0, 6.0), Color.new(1.0, 1.0, 1.0, 1.0))
```

## PolyLine

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| clr | Color | Line color |
| vec | Vector | Variadic vector (there can be an infinite number of vectors) |

### Usage:

```lua
Render.PolyLine(Color.new(1.0, 1.0, 1.0, 1.0), Vector2.new(100, 100), Vector2.new(100, 500), Vector2.new(500, 100))
```

## PolyFilled

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| clr | Color | Line color |
| vec | Vector | Variadic vector (there can be an infinite number of vectors) |

### Usage:

```lua
Render.PolyFilled(Color.new(1.0, 1.0, 1.0, 1.0), Vector2.new(100, 100), Vector2.new(100, 500), Vector2.new(500, 100))
```

## Box

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| start | Vector2 | Startpoint of the box |
| end | Vector2 | Endpoint of the box |
| clr | Color | Boxcolor |
| rounding | float | Box rounding |

### Usage:

```lua
Render.Box(Vector2.new(0.0, 0.0), Vector2.new(4.0, 5.0), Color.new(1.0, 1.0, 1.0, 1.0))
```

## BoxFilled

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| start | Vector2 | Startpoint of the box |
| end | Vector2 | Endpoint of the box |
| clr | Color | Boxcolor |
| rounding | float | Box rounding |

### Usage:

```lua
Render.BoxFilled(Vector2.new(0.0, 0.0), Vector2.new(4.0, 5.0), Color.new(1.0, 1.0, 1.0, 1.0))
```

## GradientBoxFilled

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| start | Vector2 | Beginning of the box |
| end | Vector2 | End of the box |
| t_l | Color | Color top left |
| t_r | Color | Color top right |
| b_l | Color | Color bottom left |
| b_r | Color | Color bottom right |

### Usage:

```lua
Render.GradientBoxFilled(Vector2.new(100, 100), Vector2.new(300, 300), Color.new(0, 0, 0, 1), Color.new(0, 0, 0, 1), Color.new(1, 1, 1, 1), Color.new(1, 1, 1, 1))
```

## Circle

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| pos | Vector2 | Center of the circle | + |
| rad | float | Radius | + |
| seg | int | Amount of segments | + |
| clr | Color | Circlecolor | + |
| th  | float | Circle thickness | - |
| start  | int (degree) | Circle start degree | - |
| end  | int (degree) | Circle end degree | - |

### Usage:

```lua
Render.Circle(Vector2.new(0.0, 0.0), 2.0, 30, Color.new(1.0, 1.0, 1.0, 1.0))
```

## CircleFilled

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| pos | Vector2 | Center of the circle | + |
| rad | float | Radius | + |
| seg | int | Amount of segments | + |
| clr | Color | Circlecolor | + |
| start  | int (degree) | Circle start degree | - |
| end  | int (degree) | Circle end degree | - |

### Usage:

```lua
Render.CircleFilled(Vector2.new(0.0, 0.0), 2.0, 30, Color.new(1.0, 1.0, 1.0, 1.0))
```

## Circle3D

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| pos | Vector | 3-dimensional position |
| seg | int | Amount of segments |
| rad | float | Radius |
| clr | Color | Circle color |

### Usage:

```lua
Render.Circle3D(Vector.new(0, 0, 0), 58, 10.0, Color.new(1.0, 1.0, 1.0))
```

## Circle3DFilled

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| pos | Vector | 3-dimensional position | + |
| seg | int | Amount of segments | + |
| rad | float | Radius | + |
| clr | Color | Circle color | + |
| border | bool | Add border | - |

### Usage:

```lua
Render.Circle3DFilled(Vector.new(0, 0, 0), 58, 10.0, Color.new(1.0, 1.0, 1.0))
```

## Text

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| text | string | Text | + |
| pos | Vector2 | Text position | + |
| clr | Color | Textcolor | + |
| size | int | Textsize | + |
| font | Font\* | Text font | - |
| out | bool | Text outline | - |
| centered | bool | Text centered | - |

### Usage:

```lua
Render.Text("Anarchist is cute", Vector2.new(0.0, 0.0), Color.new(1.0, 1.0, 1.0, 1.0), 20)
```

## WeaponIcon

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| index | int | Weapon index | + |
| pos | Vector2 | Icon position | + |
| clr | Color | Icon color | + |
| size | int | Icon size | + |
| out | bool | Icon outline | - |
| centered | bool | Icon centered | - |

### Usage:

```lua
Render.WeaponIcon(7, Vector2.new(100, 100), Color.new(1.0, 1.0, 1.0), 16)
```

## CalcTextSize

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| text | string | Text | + |
| size | int | Textsize | + |
| font | Font\* | Text font | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| size | Vector2 | Textsize |

### Usage:

```lua
local text_size = Render.CalcTextSize("Hello world, it's me", 16)
print("X size: "..tostring(text_size.x).." | Y size: "..tostring(text_size.y))

local font = Render.InitFont("Arial", 16)
text_size = Render.CalcTextSize("Hello world, it's me", 16, font)
print("X size: "..tostring(text_size.x).." | Y size: "..tostring(text_size.y))
```

## CalcWeaponIconSize

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| index | int | Weapon index |
| size | int | Icon size |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| size | Vector2 | Iconsize |

### Usage:

```lua
local icon_size = Render.CalcWeaponIconSize(7, 16)
print("X size: "..tostring(icon_size.x).." | Y size: "..tostring(icon_size.y))
```

## InitFont

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| name | string | Font name | + |
| size | int | Font size | + |
| flags | string table | Font flags| - |

### Font Flags

b = bold
i = italic
r = no anti-aliasing

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| font | Font\* | Created Font |

### Usage:

```lua
verdana = Render.InitFont("Verdana", 11, {'b', 'i', 'r'})

Cheat.RegisterCallback("draw", function()
    Render.Text("Hello world, it's me", Vector2.new(10.0, 15.0), Color.new(1.0, 1.0, 1.0), 11, verdana)
end)
```

## WorldToScreen

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vec | Vector | 3-dimensional position |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| vec | Vector2 | 2-dimensional screen position |

### Usage:

```lua
local screen_pos = Render.WorldToScreen(Vector.new(0, 0, 0))
```

## LoadImage

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| Image | bytes | Image |
| Size | Vector2 | Size |

### Return:

| Name | Type | Description |
| :--- | :--- | :--- |
| Image | image\* | - |

### Usage:

```lua
local image_size = Vector2.new(746 / 5, 1070 / 5)
local url = "https://anime.is-inside.me/EsXF20B5.png"
local bytes = Http.Get(url)
local image_loaded = Render.LoadImage(bytes, image_size)
```

## LoadImageFromFile

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| path | string | Path to image |
| size | Vector2 | Image Size |

### Usage:

```lua
local size = Vector2.new(100, 100)
local pos = Vector2.new(50, 50)
local image = Render.LoadImageFromFile("C:\\Users\\usr\\Desktop\\logo.png", size)

Cheat.RegisterCallback("draw", function()
    Render.Image(image, pos, size)
end)
```

## Image

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| img | Bytes | Images | + |
| pos | Vector2 | Position | + |
| size | Vector2 | Image Size | + |
| Color | Color | Image Color modulation | - |
| rounding | float | Image Rounding | - |

### Usage:

```lua
local image_size = Vector2.new(220, 257)
local url = "https://upload.wikimedia.org/wikipedia/en/7/71/Franxx_Zero_Two.jpg"
local bytes = Http.Get(url)
local image_loaded = Render.LoadImage(bytes, image_size)
Cheat.RegisterCallback("draw", function()
    Render.Image(image_loaded, Vector2.new(100, 100), image_size)
end)
```

## GetMenuPos

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| vec | Vector2 | Menu position |

### Usage:

```lua
local menu_pos = Render.GetMenuPos()
print(menu_pos.x, menu_pos.y)
```

## GetMenuSize

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| vec | Vector2 | Menu size |

### Usage:

```lua
local menu_sz = Render.GetMenuSize()
print(menu_sz.x, menu_sz.y)
```
