# MatSystem

## Functions

## CreateMaterial

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| name | string | Material name |
| mat_val | keyvalues | Material value |
| callback | function | on Material Created callback |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | IMaterial\* | Material |

```lua
local function onAnimatedWireFrameLoaded(mat)
  MatSystem.OverrideMaterial("LocalHands", mat)
end

-- animated wireframe
MatSystem.CreateMaterial("testing_material",  [[
  "VertexLitGeneric"
  {
    "$basetexture" "nature/urban_puddle01a_ssbump"
    "$additive" "1"
    "$selfillum" "1"
    "$nocull" "1"
    "$wireframe" "1"
    "Proxies"
    {
            "TextureScroll"
            {
                    "texturescrollvar" "$BasetextureTransform"
                    "texturescrollrate" "0.5"
                    "texturescrollangle" "90"
            }
    }
  }
]], onAnimatedWireFrameLoaded)
```

## FindMaterial

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| name | string | Name of material |
| group | string | Material Group |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | IMaterial\* | IMaterial pointer |

```lua
local mat = MatSystem.FindMaterial("dev/glow_armsrace", "")
```

## FirstMaterial

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | unsigned short | First material |

```lua
local mat = MatSystem.FirstMaterial()
```

## NextMaterial

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| current | unsigned short | Current material handle |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | unsigned short | Next material handle |

```lua
local mat = MatSystem.FirstMaterial()
local next_mat = MatSystem.NextMaterial(mat)
```

## GetMaterial

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| mat | unsigned short | Material Handle |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | IMaterial\* | Material |

```lua
local mat = MatSystem.FirstMaterial()
local mat_ptr = MatSystem.GetMaterial(mat)
```

## OverrideMaterial

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| type | string | Material type | + |
| mat | IMaterial\* | Material pointer | + |
| Color | color | Material Color | - |

{% hint style="info" %}
Types can be (case sensetivity):

- Enemies
- Teammates
- Weapon
- Grenades
- Localplayer
- LocalWeapon
- LocalHands
- Ragdolls
- Attachments

{% endhint %}

```lua
MatSystem.OverrideMaterial("Enemies", mat_ptr)
```

## RemoveOverrideMaterial

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| type | string | Material type |
| mat | IMaterial\* | Material pointer |

```lua
MatSystem.RemoveOverrideMaterial("Enemies", mat_ptr)
```
