# Menu

## Functions

## FindVar

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| tab_name | string | Tab name | + |
| sub_tab_name | string | Subtab name | + |
| group_name | string | Group name | + |
| opt_name | string | Option name | + |
| combo_val | string | Tab combo value(for example, "Enemies") | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | CheatVar\* | CheatVar value |

```lua
local var = Menu.FindVar("Aimbot", "Ragebot", "Accuracy", "Hit Chance")
print(var:Get())
```

## Switch

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| tab | string | Tab name | - |
| group | string | Group | + |
| name | string | Name | + |
| def_val | bool | Default value | + |
| callback | function | Change callback | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | CheatVar | Cheatvar for switch |

```lua
local switch = Menu.Switch("spirthack", "Switch", false, function(val)
    print(val)
end)
```

## SwitchColor

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| tab | string | Tab name | - |
| group | string | Group | + |
| name | string | Name | + |
| def_val | bool | Default value | + |
| def_clr | Color | Default color | + |
| callback | function | Change callback | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | CheatVar | Cheatvar for switch |

```lua
local switch = Menu.SwitchColor("spirthack", "Switch", false, Color.new(1.0, 1.0, 1.0, 1.0), function(val)
    print(val)
end)
```

## SliderInt

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| tab | string | Tab name | - |
| group | string | Group | + |
| name | string | Name | + |
| def_val | int | Default value | + |
| min | int | Minimal value | + |
| max | int | Maximum value | + |
| callback | function | Change callback | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | CheatVar | Cheatvar for slider |

```lua
local sliderint = Menu.SliderInt("spirthack", "Slider", 50, 0, 100, function(val)
    print(val)
end)
```

## SliderIntColor

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| tab | string | Tab name | - |
| group | string | Group | + |
| name | string | Name | + |
| def_val | int | Default value | + |
| min | int | Minimal value | + |
| max | int | Maximum value | + |
| def_clr | Color | Color | + |
| callback | function | Change callback | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | CheatVar | Cheatvar for slider |

```lua
local sliderint = Menu.SliderIntColor("spirthack", "Slider", 50, 0, 100, Color.new(1.0, 1.0, 1.0, 1.0), function(val)
    print(val)
end)
```

## SliderFloat

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| tab | string | Tab name | - |
| group | string | Group | + |
| name | string | Name | + |
| def_val | float | Default value | + |
| min | float | Minimal value | + |
| max | float | Maximum value | + |
| callback | function | Change callback | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | CheatVar | Cheatvar for slider |

```lua
local sliderfloat = Menu.SliderFloat("spirthack", "Slider", 50.0, 0.0, 100.0, function(val)
    print(val)
end)
```

## SliderFloatColor

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| tab | string | Tab name | - |
| group | string | Group | + |
| name | string | Name | + |
| def_val | float | Default value | + |
| min | float | Minimal value | + |
| max | float | Maximum value | + |
| def_clr | Color | Color | + |
| callback | function | Change callback | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | CheatVar | Cheatvar for slider |

```lua
local sliderfloat = Menu.SliderFloatColor("spirthack", "Slider", 50.0, 0.0, 100.0, Color.new(1.0, 1.0, 1.0, 1.0), function(val)
    print(val)
end)
```

## Combo

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| tab | string | Tab name | - |
| group | string | Group | + |
| name | string | Name | + |
| elements | table | Elements | + |
| def_value | int | Default value index | + |
| callback | function | Change callback | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | CheatVar | Cheatvar for combo |

```lua
local combo = Menu.Combo("spirthack", "Combo", {"Element 1", "Element 2", "Element 3"}, 0, function(val)
    print(val)
end)
```

## ComboColor

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| tab | string | Tab name | - |
| group | string | Group | + |
| name | string | Name | + |
| elements | table | Elements | + |
| def_value | int | Default value index | + |
| def_clr | Color | Color | + |
| callback | function | Change callback | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | CheatVar | Cheatvar for combo |

```lua
local combo = Menu.ComboColor("spirthack", "Combo", {"Element 1", "Element 2", "Element 3"}, 0, Color.new(1.0, 1.0, 1.0, 1.0), function(val)
    print(val)
end)
```

## MultiCombo

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| tab | string | Tab name | - |
| group | string | Group | + |
| name | string | Name | + |
| elements | table | Values | + |
| def_value | int | Default values | + |
| callback | function | Change callback | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | CheatVar | Cheatvar for MultiCombo |

{% hint style="info" %}
To retrieve/set values use CheatVar:Get(int el_idx), CheatVar:Set(int el_idx, bool value)
{% endhint %}

```lua
local combo = Menu.MultiCombo("spirthack", "MultiCumbo", {"Element 1", "Element 2", "Element 3"}, 0, function(val)
    print(val)
end)
combo:SetBool(1, true)
```

## TextBox

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| tab | string | Tab name | - |
| group | string | Group | + |
| name | string | Name | + |
| max_size | size_t | Max size | + |
| def_value | string | Default value  | + |
| callback | function | Change callback | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | CheatVar | Cheatvar for textbox |

```lua
local textbox = Menu.TextBox("spirthack", "TextBox", 64, "Value", function(val)
    print(val)
end)
```

## Text

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| tab | string | Tab name | - |
| group | string | Group | + |
| name | string | Name | + |

```lua
Menu.Text("spirthack", "Text")
```

## Button

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| tab | string | Tab name | - |
| group | string | Group | + |
| name | string | Name | + |
| callback | function | Click callback | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | CheatVar | Cheatvar for button |

```lua
local button = Menu.Button("spirthack", "Test", function()
    print("clicked!")
end)
```

## ColorEdit

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| tab | string | Tab name | - |
| group | string | Group | + |
| name | string | Name | + |
| def_value | Color | Default value  | + |
| callback | function | Change callback | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | CheatVar | Cheatvar for coloredit |

```lua
local coloredit = Menu.ColorEdit("spirthack", "Test", Color.new(1.0, 1.0, 1.0, 1.0), function(val)
    print(val)
end)
```

## Hotkey

### Parameters:

| Name | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| tab | string | Tab name | - |
| group | string | Group | + |
| name | string | Name | + |
| def_value | int | Default value  | + |
| callback | function | Change callback | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | CheatVar | Cheatvar for hotkey |

```lua
local hotkey = Menu.Hotkey("spirthack", "Test", 0x45, function(val)
    print(val)
end)
```

## DestroyItem

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| element | CheatVar\* | Menu Item |

```lua
local button = Menu.Button("spirthack", "Button")
Menu.Button("spirthack", "Delete 1st button"):RegisterCallback(function()
  print("Deleted")
  Menu.DestroyItem(button)
end)
```
