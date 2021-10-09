# QAngle

## Functions

## new

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| instance | QAngle | New instance of a QAngle |

```lua
local my_qangle = QAngle.new()
```

## new

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| pitch | float | - |
| yaw | float | - |
| roll | float | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| instance | QAngle | New instance of a QAngle |

```lua
local my_angle = QAngle.new(1.0, 2.0, 3.0)
```

## Normalize

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| instance | QAngle | Current instance of a QAngle |

```lua
local my_angle = QAngle.new(1.0, 2.0, 3.0)
my_angle:Normalize()
```

## Arithmetics:

### add

#### Usage:

```lua
local angle = QAngle.new(1, 1, 1) + QAngle.new(2, 2, 2)
assert angle.pitch == 3 and angle.yaw == 3 and angle.roll == 3
```

### sub

#### Usage:

```lua
local angle = QAngle.new(1, 1, 1) - QAngle.new(2, 2, 2)
assert angle.pitch == -1 and angle.yaw == -1 and angle.roll == -1
```

### mul

#### Usage:

```lua
local angle = QAngle.new(1, 1, 1) * QAngle.new(2, 2, 2)
assert angle.pitch == 2 and angle.yaw == 2 and angle.roll == 2
```

### div

#### Usage:

```lua
local angle1 = QAngle.new(1.0, 2.0, 3.0)
local angle2 = QAngle.new(1.0, 2.0, 3.0)
local angle3 = angle1 / angle2
```

### len

#### Usage:

```lua
local angle = QAngle.new(1, 1, 1)
assert #angle == 1.7320508076
```

## Fields:

| Name | Type | Description |
| :--- | :--- | :--- |
| pitch | float | - |
| yaw | float | - |
| roll | float | - |

```lua
local my_qangle = QAngle.new(1.0, 2.0, 3.0)
local pitch = my_qangle.pitch --1.0
local yaw = my_qangle.yaw --2.0
local roll = my_qangle.roll --3.0
```
