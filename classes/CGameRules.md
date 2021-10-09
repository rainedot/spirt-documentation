# CGameRules

{% hint style="info" %}
You can access GameRules class through [EntityList.GetGameRules](../tables/EntityList.md)
{% endhint %}

## Functions

## GetProp

### Parameters:

| Name | Type   | Description |
| :--- | :----- | :---------- |
| name | string | Netvar name |

### Return value:

| Name  | Type             | Description  |
| :---- | :--------------- | :----------- |
| value | Netvar dependant | Netvar value |

```lua
local game_rules = EntityList.GetGameRules()
local m_bFreezePeriod = game_rules:GetProp("m_bFreezePeriod")
print("FreezePeriod: ", m_bFreezePeriod)
```

## SetProp

### Parameters:

| Name        | Type             | Description    |
| :---------- | :--------------- | :------------- |
| name        | string           | Netvar name    |
| value       | Netvar dependant | Netvar value   |
| array index | int              | Index in array |

```lua
local game_rules = EntityList.GetGameRules()
game_rules:SetProp("m_bCTCantBuy", true)
```
