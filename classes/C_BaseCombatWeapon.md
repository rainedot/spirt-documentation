# C_BaseCombatWeapon

{% hint style="warn" %}
C_BaseCombatWeapon class is derived from C_BaseEntity, so
every method you can find in C_BaseEntity can be called from the C_BaseCombatWeapon instance

In all examples below, `weap` is a C_BaseCombatWeapon instance

```lua
-- @summary: Get active weapon
local me = EntityList.GetClientEntity(EngineClient.GetLocalPlayer()):GetPlayer()
local weap = me:GetActiveWeapon()
```

{% endhint %}

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
-- @summary: Detect when grenade is throwing

if not weap:IsGrenade() then
    return -- filter out the entities which is not a grenade
end

local m_bPinPulled = weap:GetProp("m_bPinPulled") -- is grenade's pin is pulled on or not
local m_fThrowTime = weap:GetProp("m_fThrowTime") -- get grenade throw time

if m_bPinPulled then
    return
end

if m_fThrowTime > 0 then
    print("Throwing a grenade!")
end
```

## SetProp

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| name | string | Netvar name |
| value | Netvar dependant | Netvar value |
| array index | int | Index in array |

```lua
weap:SetProp("m_bPinPulled", true)
```

## GetClassId

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| id | int | Class id |

```lua
-- @summary: Detects when active weapon is AK-47 by weapon class id

local ClassId_CAK47 = 1 -- https://github.com/spirthack/CSGOSimple/blob/master/CSGOSimple/valve_sdk/misc/Enums.hpp#L164

local weapon_classid = weap:GetClassId()
if weapon_classid == ClassId_CAK47 then
    print("Active weapon is AK-47")
end
```

## IsGrenade

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is weapon granade |

```lua
weap:IsGrenade()
```

## IsKnife

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is weapon knife |

```lua
weap:IsKnife()
```

## IsRifle

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is weapon rifle |

```lua
weap:IsRifle()
```

## IsPistol

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is weapon pistol |

```lua
weap:IsPistol()
```

## IsSniper

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is weapon sniper |

```lua
weap:IsSniper()
```

## IsGun

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is weapon gun |

```lua
weap:IsGun()
```

## IsReloading

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is weapon being reloaded |

```lua
weap:IsReloading()
```

## GetInaccuracy

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| weapon | C_BaseCombatWeapon | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | float | Weapon inaccuarcy |

```lua
local weapon_inaccuracy = weap:GetInaccuracy(weap)
```

## GetSpread

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| weapon | C_BaseCombatWeapon | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | float | Weapon inaccuarcy |

```lua
local weapon_spread = weap:GetSpread(weap)
```

## GetFireRate

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | float | Weapon fire rate |

```lua
weap:GetFireRate()
```

## GetMaxSpeed

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | float | Max weapon speed |

```lua
weap:GetMaxSpeed()
```

## GetMaxClip

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | int | Max weapon clip count|

```lua
-- @summary: Prints the amount of bullets in clip and max bullets in clip available

local clip = weap:GetProp("DT_BaseCombatWeapon", "m_iClip1")
local max_clip = weap:GetmaxClip()

print("Bullets in clip: "..tostring(clip).."/"..tostring(max_clip))
```

## GetWeaponDamage

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | int | Weapon damage |

```lua
weap:GetWeaponDamage()
```

## GetWeaponRange

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | int | Weapon range |

```lua
weap:GetWeaponRange()
```

## GetWeaponID

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | int | Weapon id |

```lua
-- @summary: Detects when active weapon is AK-47 by weapon id

local WEAPON_AK47 = 7 -- https://github.com/spirthack/CSGOSimple/blob/master/CSGOSimple/valve_sdk/misc/Enums.hpp#L80
local weapon_id = weap:GetWeaponID()

if weapon_id == WEAPON_AK47 then
    print("Your active weapon is AK-47")
end
```
