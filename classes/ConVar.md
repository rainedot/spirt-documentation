# ConVar

{% hint style="info" %}
You can access `ConVar` instance through [CVar](../tables/CVar.md)
{% endhint %}

## Functions

{% hint style="warning" %}
In all examples below, `cvar` is an instance of `ConVar`.
{% endhint %}

## GetString

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | string | ConVar value as a string |

```lua
local string_value = cvar:GetString()
```

## GetInt

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | int | ConVar value as int |

```lua
local int_value = cvar:GetInt()
```

## GetFloat

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | float | ConVar value as a float |

```lua
local float_value = cvar:GetFloat()
```

## GetColor

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | Color | ConVar value as a Color |

```lua
local color_value = cvar:GetColor()
```

## SetInt

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | int | New convar's value |

```lua
local var = cvar:SetInt(1)
```

## SetString

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | string | New convar's value |

```lua
local var = cvar:SetString("Hello world, it's me")
```

## SetFloat

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | float | New convar's value |

```lua
local var = cvar:SetFloat(1.0)
```

## SetColor

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | Color | New convar's value |

```lua
local var = cvar:SetColor(Color.new())
```
