# C_BasePlayer

## Functions

## GetProp

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| name | string | Netvar name |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | Netvar dependant | Netvar value |

```lua
local player = EntityList.GetLocalPlayer()
local health = player:GetProp("m_iHealth")
print("Local player health: ", health)
```

## SetProp

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| name | string | Netvar name |
| value | Netvar dependant | Netvar value |
| array index | int | Index in array |

```lua
Cheat.RegisterCallback("draw", function()
    local player = EntityList.GetLocalPlayer()
    player:SetProp("m_iHealth", 1)
end)
```

## GetClassID

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| id | int | Class id |

```lua
local entity = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local player = entity:GetPlayer()
local class_id = player:GetClassID()
print(class_id)
```

## EntIndex

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | int | Entity index |

```lua
local entity = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local player = entity:GetPlayer()
local ent_index = player:EntIndex()
print(ent_index)
```

## SetModelIndex

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| index | int | Model index |

```lua
--soonTM
```

## IsVisible

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| from | Vector | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is player visible |

```lua
local entity = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local player = entity:GetPlayer()
local is_visible = player:IsVisible(Vector.new(0, 0, 0))
print(is_visible)
```

## GetEyePosition

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| vec | Vector | Eye position in 3D space |

```lua
local entity = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local player = entity:GetPlayer()
local eye_pos = player:GetEyePosition()
print(eye_pos.x, eye_pos.y, eye_pos.z)
```

## GetActiveWeapon

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| weapon | C_BaseCombatWeapon\* | Pointer to active weapon |

```lua
local entity = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local player = entity:GetPlayer()
local active_weapon = player:GetActiveWeapon()
```

## GetHitboxCenter

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| vec | Vector | Hitbox center |

```lua
local entity = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local player = entity:GetPlayer()
local hitbox_center = player:GetHitboxCenter(0)
print(hitbox_center.x, hitbox_center.y, hitbox_center.z)
```

## GetName

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| name | string | Name |

```lua
local entity = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local player = entity:GetPlayer()
local pl_name = player:GetName()
print(pl_name)
```

## IsDormant

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is player dormant |

```lua
local entity = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local player = entity:GetPlayer()
local is_dormant = player:IsDormant()
print(is_dormant)
```

## IsTeamMate

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is player teammate |

```lua
local entity = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local player = entity:GetPlayer()
local is_teammate = player:IsTeamMate()
print(is_teammate)
```

## GetSequenceActivity

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| sec | int | Sequence |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| act | int | Sequence activity |

```lua
--soonTM
```

## DrawHitbox

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| index | int | Hitbox index |
| clr | Color | Color |
| tick_n | int | Tick |

```lua
Cheat.RegisterCallback("draw", function()
    local entity = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
    local player = entity:GetPlayer()
    player:DrawHitbox(3, Color.new(1, 1, 1, 1), GlobalVars.tickcount-1)
end)
```

## GetNetworkState

### Return value:

| Name | Type |
| :--- | :--- |
| Network State | int |

{% hint style="info" %}
States:

```text
    returns -1 if player is dormant and data is not available or too old,
    returns 0 if player is not dormant,
    returns 1 if player is dormant but cheat has 100% info where is player,
    returns 2 if player is dormant but we've received info from shared esp,
    returns 3 if player is dormant but updated by sounds,
    returns 4 if player is dormant and is not updated
```

{% endhint %}

```lua
Cheat.RegisterCallback("createmove", function()
    local players = EntityList.GetPlayers()
    local local_player = EntityList.GetLocalPlayer()
    for table_index, player_pointer in pairs(players) do
        if player_pointer == local_player then goto skip end
        local get_network_state = player_pointer:GetNetworkState()
        local player_name = player_pointer:GetName()
        print("Name:", player_name, "Network State:", get_network_state)
        ::skip::
    end
end)
```

## GetESPAlpha

### Return value:

| Name | Type |
| :--- | :--- |
| ESP Alpha | float |

```lua
Cheat.RegisterCallback("createmove", function()
    local players = EntityList.GetPlayers()
    local local_player = EntityList.GetLocalPlayer()
    for table_index, player_pointer in pairs(players) do
        if player_pointer == local_player then goto skip end
        local esp_alpha = player_pointer:GetESPAlpha()
        local player_name = player_pointer:GetName()
        print("Name:", player_name, "ESP Alpha:", esp_alpha)
        ::skip::
    end
end)
```

## GetPlayerInfo

### Return value:

| Name | Type |
| :--- | :--- |
| Player Info | PlayerInfo |

```lua
local local_player = EntityList.GetLocalPlayer()

if local_player == nil then
    return
end

local player_info = local_player:GetPlayerInfo()

local SteamID32 = player_info.iSteamID
print(SteamID32)
```
