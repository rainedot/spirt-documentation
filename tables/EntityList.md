# EntityList

## Functions

## GetClientEntity

### Parameters:

| Name | Type | Description  |
| :--- | :--- | :----------- |
| ent  | int  | Entity index |

### Return value:

| Name | Type           | Description       |
| :--- | :------------- | :---------------- |
| ent  | C_BaseEntity\* | Pointer to entity |

```lua
local localplayer = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
```

## NumberOfEntities

### Parameters:

| Name               | Type | Description                      |
| :----------------- | :--- | :------------------------------- |
| inclNonNetworkable | bool | Include non-networkable entities |

### Return value:

| Name  | Type | Description                         |
| :---- | :--- | :---------------------------------- |
| value | int  | Number of entities currently in use |

```lua
local num_ents = EntityList.NumberOfEntities(false)
print(num_ents)
```

## GetHighestEntityIndex

### Return value:

| Name  | Type | Description          |
| :---- | :--- | :------------------- |
| value | int  | Highest entity index |

```lua
local highest_index = EntityList.GetHighestEntityIndex()
print(highest_index)
```

## GetClientEntityFromHandle

### Parameters:

| Name | Type          | Description   |
| :--- | :------------ | :------------ |
| h    | unsigned long | Entity handle |

### Return value:

| Name | Type           | Description       |
| :--- | :------------- | :---------------- |
| ent  | C_BaseEntity\* | Pointer to entity |

```lua
-- @summary: Get active weapon from weapon_handle
-- @hint: You can use GetActiveWeapon instead
local me = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local weapon_handle = me:GetProp("m_hActiveWeapon")
local weap = EntityList.GetClientEntityFromHandle(weapon_handle)
```

## GetPlayerResource

### Return value:

| Name            | Type               | Description |
| :-------------- | :----------------- | :---------- |
| Player Resource | CSPlayerResource\* | -           |

```lua
local player_resource = EntityList.GetPlayerResource()
local get_prop = player_resource:GetProp("m_szClan")

for key, value in pairs(get_prop) do
    print(key, value)
end
```

## GetGameRules

### Return value:

| Name       | Type          | Description |
| :--------- | :------------ | :---------- |
| Game Rules | CSGameRules\* | -           |

```lua
local game_rules = EntityList.GetGameRules()
local get_prop = game_rules:GetProp("m_bIsValveDS")
print(get_prop)
```

## GetEntitiesByClassID

### Parameters:

| Name | Type | Description |
| :--- | :--- | :---------- |
| id   | int  | Class id    |

### Return value:

| Name | Type           | Description   |
| :--- | :------------- | :------------ |
| ent  | C_BaseEntity\* | Player entity |

```lua
local ents = EntityList.GetEntitiesByClassID(40)
print("Found " .. tostring(#ents) .. " entities with id 40")
```

## GetEntitiesByName

### Parameters:

| Name | Type   | Description |
| :--- | :----- | :---------- |
| name | string | Entity name |

### Return value:

| Name | Type           | Description   |
| :--- | :------------- | :------------ |
| ent  | C_BaseEntity\* | Player entity |

```lua
local ents = EntityList.GetEntitiesByName("CCSPlayer")
print("Found " .. tostring(#ents) .. " entities with name CCSPlayer")
```

## GetLocalPlayer

### Return value:

| Name | Type           | Description         |
| :--- | :------------- | :------------------ |
| ent  | C_BasePlayer\* | Local Player entity |

```lua
local player = EntityList.GetLocalPlayer()
```

## GetWeapon

### Parameters:

| Name  | Type | Description         |
| :---- | :--- | :------------------ |
| Index | int  | Weapon Entity index |

### Return value:

| Name | Type                 | Description   |
| :--- | :------------------- | :------------ |
| ent  | C_BaseCombatWeapon\* | Weapon entity |

```lua
local player = EntityList.GetWeapon(100)
```

## GetPlayer

### Parameters:

| Name  | Type | Description  |
| :---- | :--- | :----------- |
| Index | int  | Entity index |

### Return value:

| Name | Type           | Description   |
| :--- | :------------- | :------------ |
| ent  | C_BasePlayer\* | Player entity |

```lua
local player = EntityList.GetPlayer(1)
```

## GetPlayerFromHandle

### Parameters:

| Name   | Type   | Description   |
| :----- | :----- | :------------ |
| handle | handle | Player Handle |

### Return value:

| Name | Type           | Description   |
| :--- | :------------- | :------------ |
| ent  | C_BasePlayer\* | Player entity |

```lua
local player = EntityList.GetPlayerFromHandle(handle)
```

## GetWeaponFromHandle

### Parameters:

| Name   | Type   | Description   |
| :----- | :----- | :------------ |
| handle | handle | Weapon Handle |

### Return value:

| Name | Type                 | Description |
| :--- | :------------------- | :---------- |
| ent  | C_BaseCombatWeapon\* | Weapon      |

```lua
local local_player_ptr = EntityList.GetLocalPlayer()
local active_weapon = local_player_ptr:GetProp("m_hActiveWeapon")
local weapon_from_handle = EntityList.GetWeaponFromHandle(active_weapon)
print(weapon_from_handle)
```

## GetPlayers

### Return value:

| Name    | Type  | Description                         |
| :------ | :---- | :---------------------------------- |
| players | table | Table with players (C_BasePlayer\*) |

```lua
Cheat.RegisterCallback("createmove", function()
    local players = EntityList.GetPlayers()
    local local_player = EntityList.GetLocalPlayer()
    for table_index, player_pointer in pairs(players) do
        if player_pointer == local_player then goto skip end
        local player_name = player_pointer:GetName()
        print("Name:", player_name)
        ::skip::
    end
end)
```

## GetPlayerForUserID

### Return value:

| Name | Type           | Description   |
| :--- | :------------- | :------------ |
| ent  | C_BasePlayer\* | Player entity |

```lua
Cheat.RegisterCallback("events", function(event)
    if event:GetName() == "player_hurt" then
        local target_player = EntityList.GetPlayerForUserID(event:GetInt("userid", 0))
        if not target_player then return end

        local attacker_player = EntityList.GetPlayerForUserID(event:GetInt("attacker", 0))
        if not attacker_player then return end

        print(string.format("%s hurt by %s", target_player:GetName(), attacker_player:GetName()))
    end
end)
```
