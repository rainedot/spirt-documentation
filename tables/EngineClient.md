# EngineClient

## Functions

## ExecuteClientCmd

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | string | Command |

```lua
EngineClient.ExecuteClientCmd("say spirthack.me")
```

## GetLevelName

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | string | Name of the current map |

```lua
local mapname = EngineClient.GetLevelName()
print(mapname)
```

## GetLevelNameShort

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | string | Short name of the current map |

```lua
local mapname_short = EngineClient.GetLevelNameShort()
print(mapname_short)
```

## GetMapGroupName

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | string | Map group name |

```lua
local mapgroup = EngineClient.GetMapGroupName()
print(mapgroup)
```

## GetLocalPlayer

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | int | Local player index |

```lua
local localplayer = EngineClient.GetLocalPlayer()
print(localplayer)
```

## GetMaxClients

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | int | Max amount of clients |

```lua
local max_players = EngineClient.GetMaxClients()
print(max_players)
```

## GetNetChannelInfo

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | INetChannelInfo\* | INetChannelInfo pointer |

```lua
local net_chann = EngineClient.GetNetChannelInfo()
print(net_chann)
```

## GetScreenSize

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | Vector2 | Size of game window |

```lua
local screen_size = EngineClient.GetScreenSize()
print(screen_size.x, screen_size.y)
```

## GetViewAngles

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | QAngle | View angles |

```lua
local view_angles = EngineClient.GetViewAngles()
print(view_angles.pitch, view_angles.yaw, view_angles.roll)
```

## IsConnected

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is player connected to any server |

```lua
local IsConnected = EngineClient.IsConnected()
print(IsConnected)
```

## IsInGame

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is player ingame |

```lua
local in_game = EngineClient.IsInGame()
print(in_game)
```

## SetViewAngles

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | QAngle | New angles |

```lua
EngineClient.SetViewAngles(QAngle.new(20, 20, 0))
```