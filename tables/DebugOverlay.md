# DebugOverlay

## Functions

## AddBoxOverlay

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| origin | Vector |  |
| mins | Vector |  |
| max | Vector |  |
| value | QAngle |  |
| r | int |  |
| g | int |  |
| b | int |  |
| a | int |  |
| duration | float |  |

```lua
DebugOverlay.AddBoxOverlay(Vector.new(1, 2, 3), Vector.new(4, 5, 6), Vector.new(6, 7, 8), QAngle.new(9, 10, 11), 255, 255, 255, 255, false, 1.0)
```

## AddSphereOverlay

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vOrigin | Vector |  |
| flRadius | float |  |
| nTheta | int |  |
| nPhi | int |  |
| r | int |  |
| g | int |  |
| b | int |  |
| a | int |  |
| flDuration | float |  |

```lua
DebugOverlay.AddSphereOverlay(Vector.new(1, 2, 3), 1.0, 10, 10, 255, 255, 255, 255, false, 1.0)
```

## AddTriangleOverlay

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| p1 | Vector |  |
| p2 | Vector |  |
| p3 | Vector |  |
| r | int |  |
| g | int |  |
| b | int |  |
| a | int |  |
| noDepthTest | bool |  |
| duration | float |  |

```lua
DebugOverlay.AddTriangleOverlay(Vector.new(1, 2, 3), Vector.new(4, 5, 6), Vector.new(7, 8, 9), 255, 255, 255, 255, false, 1.0)
```

## AddLineOverlay

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| origin | Vector |  |
| dest | Vector |  |
| r | int |  |
| g | int |  |
| b | int |  |
| noDepthTest | bool |  |
| duration | float |  |

```lua
DebugOverlay.AddLineOverlay(Vector.new(1, 2, 3), Vector.new(4, 5, 6), 255, 255, 255, false, 1.0)
```

## AddCapsuleOverlay

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| origin | Vector |  |
| dest | Vector |  |
| pillradius | float |  |
| r | int |  |
| g | int |  |
| b | int |  |
| a | int |  |
| duration | float |  |

```lua
DebugOverlay.AddCapsuleOverlay(Vector.new(1, 2, 3), Vector.new(4, 5, 6), 15.0, 255, 255, 255, 255, 1.0)
```
