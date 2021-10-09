# ActiveBind

{% hint style="info" %}
You can access `ActiveBind` instance through `GetBinds` [function](../tables/Cheat.md)
{% endhint %}

## Functions

## GetName

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| name | string | Bind Name |

```lua
bind:GetName()
```

## GetValue

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | string | Bind value |

```lua
bind:GetValue()
```

## IsActive

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is keybind active |

```lua
bind:IsActive()
```

## GetKey

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | int | keybind key |

```lua
bind:GetKey()
```

## GetMode

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | int | Key bind mode (1 for hold, 0 for toggle) |

```lua
bind:GetMode()
```
