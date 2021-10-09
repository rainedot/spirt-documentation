# Synced animated clantag changer

> Author: [@es3n1n](https://github.com/es3n1n)
>
> Name: `Synced animated clantag changer`
>
> Description: `Changes your clantag`

```lua
-- @region: engine stuff
local _set_clantag = ffi.cast('int(__fastcall*)(const char*, const char*)', Utils.PatternScan('engine.dll', '53 56 57 8B DA 8B F9 FF 15'))
local _last_clantag = nil
local set_clantag = function(v)
  if v == _last_clantag then return end
  _set_clantag(v, v)
  _last_clantag = v
end
-- @endregion

-- @region: animations stuff
local build_tag = function(tag)
  local ret = { ' ' }

  -- @note: es3n1n: build animations
  -- [0] = B
  -- [1] = Bo
  -- [2] = Bob
  -- etc...
  for i = 1, #tag do
    table.insert(ret, tag:sub(1, i))
  end

  -- @note: es3n1n: reverse ret array so we can get
  -- [0] = B
  -- [1] = Bo
  -- [2] = Bob
  -- [3] = Bo
  -- [4] = B
  for i = #ret - 1, 1, -1 do
    table.insert(ret, ret[i])
  end

  return ret
end

local tag = build_tag('BoberHook')
-- @endregion


-- @note: es3n1n: you can change from draw to whatever you want
local clantag_animation = function()
    if not EngineClient.IsConnected() then return end

    local netchann_info = EngineClient.GetNetChannelInfo()
    if netchann_info == nil then return end

    local latency = netchann_info:GetLatency(0) / GlobalVars.interval_per_tick
    local tickcount_pred = GlobalVars.tickcount + latency
    local iter = math.floor(math.fmod(tickcount_pred / 16, #tag + 1) + 1)

    set_clantag(tag[iter])
end


Cheat.RegisterCallback("draw", clantag_animation)
```
