# Snaplines

> Author: [@elleqt](https://github.com/elleqt)
>
> Name: `Snapline esp`
>
> Description: `Render snaplines`

```lua
local screen_size = EngineClient.GetScreenSize()
Cheat.RegisterCallback("draw", function()
    local players = EntityList.GetPlayers()
    local local_player = EntityList.GetLocalPlayer()
    for _, player_ptr in ipairs(players) do
        if player_ptr == local_index or player_ptr:IsTeamMate() then goto skip end
        local position = Render.WorldToScreen(player_ptr:GetProp("m_vecOrigin"))
        Render.Line(position, Vector2.new(screen_size.x / 2, screen_size.y), Color.new(1, 1, 1, 1))
        ::skip::
    end
end)
```
