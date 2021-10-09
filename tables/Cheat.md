# Cheat

## Functions

## RegisterCallback

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| event_name | string | Event names |
| callback | function | Callback |

{% hint style="info" %}
You can view callbacks list [here](callbacks.md).
{% endhint %}

```lua
Cheat.RegisterCallback("draw", function()
    Render.Text("Hello world, it's me", Vector2.new(10.0, 15.0), Color.new(1.0, 1.0, 1.0), 16)
end)
```

## AngleToForward

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| ang | QAngle | Input angle |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| vec | Vector | Output vector |

```lua
local vec = Cheat.AngleToForward(QAngle.new())
```

## VectorToAngle

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vec | Vector | Input vector |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| ang | QAngle | Output angle |

```lua
local ang = Cheat.VectorToAngle(Vector.new(100, 100, 100))
```

## IsMenuVisible

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is menu opened or not |

```lua
local is_visible = Cheat.IsMenuVisible()
```

## GetMousePos

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | Vector2 | Mouse position on screen |

```lua
local mouse_pos = Cheat.GetMousePos()
```

## IsKeyDown

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| key | int | Virtual key code |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is key down |

{% hint style="info" %}
You can find all virtual keys [here](https://docs.microsoft.com/en-us/windows/win32/inputdev/virtual-key-codes)
{% endhint %}

```lua
local is_key_pressed = Cheat.IsKeyDown(0x1)
```

## GetCheatUserName

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| name | string | Spirthack's account username |

```lua
local username = Cheat.GetCheatUserName()
```

## GetBinds

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| binds | table (`ActiveBind`s array)| Binds |

```lua
local binds = Cheat.GetBinds()
print("Name", "isActive", "Value")
for i = 1, #binds do
    print(binds[i]:GetName(), binds[i]:IsActive(), binds[i]:GetValue())
end
```