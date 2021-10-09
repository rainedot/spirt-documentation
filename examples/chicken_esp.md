# Chicken ESP

> Author: [@elleqt](https://github.com/elleqt)
>
> Name: `Chicken esp`
>
> Description: `Render circle around chickens`

```lua
Cheat.RegisterCallback("draw", function()
    local entity = EntityList.GetEntitiesByName("CChicken")
    for i = 1, #entity do
        local position = entity[i]:GetProp("m_vecOrigin")
        Render.Circle3D(position, 58, 10.0, Color.new(1.0, 1.0, 1.0))
    end
end)
```
