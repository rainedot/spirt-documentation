# C_BaseEntity

## Functions

## GetClassID

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| id | int | Class id |

```lua
local localplayer = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local classid = localplayer:GetClassID()
print(classid)
```

## GetClassName

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| name | char | Class name |

```lua
local localplayer = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local classname = localplayer:GetClassName()
print(classname)
```

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

## IsPlayer

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is entity a player |

```lua
local localplayer = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local isPlayer = localplayer:IsPlayer()
print(isPlayer)
```

## GetPlayer

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | C_BasePlayer\* | Pointer to player |

```lua
local localplayer = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local getplayer = localplayer:GetPlayer()
```

## IsWeapon

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is entity a weapon |

```lua
local localplayer = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local weapon = EntityList.GetClientEntity(localplayer:GetWeapon():EntIndex())
local isWeapon = weapon:IsWeapon()
print(isWeapon)
```

## GetWeapon

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | C_BaseWeapon\* | Pointer to weapon |

```lua
local weapon = entity:GetWeapon()
```

## GetRenderBounds

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| min | Vector | - |
| max | Vector | - |

```lua
-- @summary: Render boxes on every player
Cheat.RegisterCallback("draw", function()
    local ents = EntityList.GetEntitiesByName("CCSPlayer")

    for i = 1, #ents do
        local origin = ents[i]:GetRenderOrigin()
        local min = Vector.new()
        local max = Vector.new()
        local bounds = ents[i]:GetRenderBounds(min, max)

        -- upper bounds
        Render.CircleFilled(Render.ScreenPosition(origin + Vector.new(min.x, max.y, max.z)), 10.0, 30, Color.new(1.0, 1.0, 1.0, 1.0))
        Render.CircleFilled(Render.ScreenPosition(origin + Vector.new(max.x, min.y, max.z)), 10.0, 30, Color.new(1.0, 1.0, 1.0, 1.0))
        Render.CircleFilled(Render.ScreenPosition(origin + Vector.new(min.x, min.y, max.z)), 10.0, 30, Color.new(1.0, 1.0, 1.0, 1.0))
        Render.CircleFilled(Render.ScreenPosition(origin + max), 10.0, 30, Color.new(1.0, 1.0, 1.0, 1.0))

        -- bottom bounds
        Render.CircleFilled(Render.ScreenPosition(origin + Vector.new(max.x, min.y, min.z)), 10.0, 30, Color.new(1.0, 1.0, 1.0, 1.0))
        Render.CircleFilled(Render.ScreenPosition(origin + Vector.new(min.x, max.y, min.z)), 10.0, 30, Color.new(1.0, 1.0, 1.0, 1.0))
        Render.CircleFilled(Render.ScreenPosition(origin + Vector.new(max.x, max.y, min.z)), 10.0, 30, Color.new(1.0, 1.0, 1.0, 1.0))
        Render.CircleFilled(Render.ScreenPosition(origin + min), 10.0, 30, Color.new(1.0, 1.0, 1.0, 1.0))

    end
end)
```

## GetRenderOrigin

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| vec | Vector | Render origin |

```lua
local localplayer = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local origin = localplayer:GetRenderOrigin()
print(origin.x, origin.y, origin.z)
```

## GetRenderAngles

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| angle | QAngle | Render angles |

```lua
local localplayer = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local render_angles = localplayer:GetRenderAngles()
print(render_angles.pitch, render_angles.yaw, render_angles.roll)
```

## EntIndex

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | int | Entity index |

```lua
local localplayer = EntityList.GetClientEntity(EngineClient.GetLocalPlayer())
local ent_id = localplayer:EntIndex()
print(ent_id)
```

## SetModelIndex

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| index | int | Model index |

```lua
--soonTM
```
