# IGameEvent

{% hint style="info" %}
Instance of `IGameEvent` is passed to `events` [callback](../tables/callbacks.md)
{% endhint %}

{% hint style="info" %}
Events are networked to connected clients and invoked there to.
Therefore you have to specify all data fields and there data types
in an public resource file which is parsed by server and broadcasted
to it's clients.
A typical game event is defined like this:

```text
    "game_start"                // a new game starts
    {
        "roundslimit"    "long"        // max round
        "timelimit"        "long"        // time limit
        "fraglimit"        "long"        // frag limit
        "objective"        "string"    // round objective
    }
```

All events must have unique names (case sensitive) and may have
a list of data fields.

Each data field must specify a data type, so the engine knows
how to serialize/unserialize that event for network transmission.
Valid data types are string, float, long, short, byte & bool.

{% endhint %}

{% hint style="warning" %}
In examples below all `event` is `IGameEvent` instance
{% endhint %}

## Functions

## GetName

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | string | Event name |

```lua
local event_name = event:GetName()
```

## GetBool

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| name | string | Field name |
| def_val | bool | Default value |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Event's bool value |

```lua
local is_headshot = event:GetBool("headshot", false)
```

## GetInt

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| name | string | Field name |
| def_val | int | Default value |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | int | Event's int value |

```lua
local user_id = event:GetInt("userid", -1)
```

## GetFloat

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| name | string | Field name |
| def_val | float | Default value |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | float | Event's float value |

```lua
local x_axis = event:GetFloat("x", -1.0)
```

## GetString

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| name | string | Field name |
| def_val | string | Default value |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | string | Event's string value |

```lua
local weapon_name = event:GetString("weapon", "unknown")
```
