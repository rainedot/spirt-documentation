# Keybind Indicators

> Author: [@elleqt](https://github.com/elleqt)
>
> Name: `Indicators`
>
> Description: `Bind indicator`

```lua
-- Define a few things we're going to be using
local color_active      = Color.new(0, 1, 0, 1) -- The color we use for rendering if the keybind is active
local color_inactive    = Color.new(1, 0, 0, 1) -- The color we use for rendering if the keybind is inactive
local render_position   = Vector2.new(25, 550)  -- The position our indicators will be rendered at

local on_draw = function()
    local local_player_index    = EngineClient.GetLocalPlayer()                   -- Get our local player index
    local local_player          = EntityList.GetClientEntity(local_player_index)  -- Get the entity object for our local player

    if not local_player then
        return -- No real point rendering keybinds if the local player is invalid
    end

    local render_offset     = 0                     --  An offset for our render positions so strings don't render on top of each other

    local render_keybind    = function(bind)        -- Define a helper function that will actually render our keybinds
        if not bind:IsActive() then
            return -- No point rendering a keybind that's not active
        end

        local bind_name             = bind:GetName()        -- Whatever our keybind's name is
        local bind_value            = bind:GetValue()       -- The value our keybind has when toggled

        local render_string         = string.format("%s - %s", bind_name, bind_value)   -- Format the values into a string

        local new_render_position   = Vector2.new(render_position.x, render_position.y + render_offset)

        local render_color

        if bind_value == "off" or bind_value == "Disabled" or bind_value == "0" then    --  If the bind is inactive...
            render_color = color_inactive   --  The color we render our binds with will be whatever we have as the inactive color
        else                                                                            --  Otherwise,
            render_color = color_active     --  The bind is active and we will be using the active color
        end

        Render.Text(render_string, new_render_position, render_color, 24, true)       --  Actually render our string

        render_offset = render_offset + 20  --  Offset our render position a bit
    end

    local binds = Cheat.GetBinds()
    for i = 1, #binds do --  Iterate over our binds...
        render_keybind(binds[i])   --  And handle them using our render_keybind function
    end
end

Cheat.RegisterCallback("draw", on_draw) --  Set a callback on the "draw" event, now our function will be executed every time it's called
```
