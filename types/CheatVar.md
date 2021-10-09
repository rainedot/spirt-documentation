# CheatVar

{% hint style="info" %}
You can access `CheatVar` instance through [Menu.FindVar](../tables/Menu.md)
{% endhint %}

## Functions

## Get

### Return value:

| Name  | Type                 | Description    |
| :---- | :------------------- | :------------- |
| value | depends on menu item | CheatVar value |

```lua
local val = var:Get()
```

## Set

### Parameters:

| Name  | Type                 | Description    |
| :---- | :------------------- | :------------- |
| value | depends on menu item | CheatVar value |

```lua
local val = var:Set(Color.new(1.0, 1.0, 1.0, 1.0))
```

## GetColor

### Return value:

| Name  | Type  | Description             |
| :---- | :---- | :---------------------- |
| value | Color | CheatVar value as Color |

```lua
local val = var:GetColor()
```

## SetColor

### Parameters:

| Name  | Type  | Description     | Required |
| :---- | :---- | :-------------- | :------- |
| value | Color | New Color value | +        |

```lua
var:SetColor(Color.new(1, 1, 1, 1))
```

## RegisterCallback

### Parameters:

| Name | Type     | Description | Required |
| :--- | :------- | :---------- | :------- |
| func | function | Callback    | +        |

```lua
var:RegisterCallback(function(val)
    print(val)
end)
```

## SetVisible

### Parameters:

| Name       | Type | Description     | Required |
| :--------- | :--- | :-------------- | :------- |
| visibility | bool | Item visibility | +        |

```lua
var:SetVisible(false)
```

## DestroyItem

{% hint style="warning" %}
DestroyItem was previously incorrectly listed here. It has been moved to to the [Menu API](../tables/Menu.md#destroyitem)
{% endhint %}

## GetName

### Return value:

| Name | Type   | Description             |
| :--- | :----- | :---------------------- |
| name | string | Returns CheatVar's name |

```lua
local bodyAim = Menu.FindVar("Aimbot", "Ragebot", "Misc", "Body Aim")
local name = bodyAim:GetName()

print(name)
```

## UpdateList

### Parameters:

| Name     | Type  | Description |
| :------- | :---- | :---------- |
| elements | table | Combo Items |

```lua
local combo = Menu.Combo("Neverlose", "Combo", {"Element 1", "Element 2", "Element 3"}, 0)
Menu.Button("neverlose", "update"):RegisterCallback(function()
    combo:UpdateList({"el1", "el2"})
end)
```

## GetList

### Return value:

| Name     | Type  | Description                   |
| :------- | :---- | :---------------------------- |
| elements | table | Returns all elements in combo |

```lua
local bodyAim = Menu.FindVar("Aimbot", "Ragebot", "Misc", "Body Aim")
local list = bodyAim:GetList()

for _, item in ipairs(list) do
  print(item)
end
```
