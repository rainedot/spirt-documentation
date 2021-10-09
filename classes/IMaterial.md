# IMaterial

{% hint style="info" %}
You can access `IMaterial` instance through `MatSystem` [table](../tables/MatSystem.md)
{% endhint %}

## Functions

{% hint style="warning" %}
In examples below all `material` is `IMaterial` instance
{% endhint %}

## ColorModulate

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| r | float | Red color value |
| g | float | Green color value |
| b | float | Blue color value |

```lua
material:ColorModulate(1.0, 1.0, 1.0)
```

## AlphaModulate

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| a | float | Alpha color value |

```lua
material:AlphaModulate(0.5)
```

## GetName

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | string | Name of the material |

```lua
local mat_name = material:GetName()
```

## IsErrorMaterial

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| is_broken | bool | Is this material is error material |

```lua
local is_error = material:IsErrorMaterial()
```

## SetMaterialVarFlag

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| flag | int | Flag |
| value | bool | Flag's value |

```lua
material:SetMaterialVarFlag(bit.blshift(1, 15), true) -- IgnoreZ
```
