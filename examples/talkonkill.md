# Talk on kill

> Author: [@elleqt](https://github.com/elleqt) / [@es3n1n](https://github.com/es3n1n/)
>
> Name: `Talk on kill`
>
> Description: `Talk in chat on kill`

```lua

local phrases = {
    "1 sit nn dog",
    "owned"
}

local function get_phrase()
    return phrases[Utils.RandomInt(1, #phrases)]:gsub('\"', '')
end

Cheat.RegisterCallback("events", function(event)
    if event:GetName() ~= "player_death" then return end

    local me = EntityList.GetLocalPlayer()
    local victim = EntityList.GetPlayerForUserID(event:GetInt("userid"))
    local attacker = EntityList.GetPlayerForUserID(event:GetInt("attacker"))

    if victim == attacker or attacker ~= me then return end

    EngineClient.ExecuteClientCmd('say "' .. get_phrase() .. '"')
end)

```
