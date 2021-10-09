# RenderBeams

## Functions

## CreateBeamPoints

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| BeamInfo_t | BeamInfo_t | - |

```lua
local beam_info = BeamInfo_t.new()
beam_info.m_vecStart = Vector.new(-1500, -1800, -200)
beam_info.m_vecEnd = beam_info.m_vecStart + 100
beam_info.m_nSegments = 2
beam_info.m_nType = 0
beam_info.m_bRenderable = true
beam_info.m_nFlags = 0
beam_info.m_pszModelName = "sprites/purplelaser1.vmt"
beam_info.m_flHaloScale = 0.0
beam_info.m_flLife = 4.0
beam_info.m_flWidth = 2.0
beam_info.m_flEndWidth = 2.0
beam_info.m_flFadeLength = 0.0
beam_info.m_flAmplitude = 0.0
beam_info.m_flSpeed = 0.0
beam_info.m_flFrameRate = 0.0
beam_info.m_nHaloIndex = 0
beam_info.m_nStartFrame = 0
beam_info.m_flBrightness = 255.0
beam_info.m_flRed = 255.0
beam_info.m_flGreen = 55.0
beam_info.m_flBlue = 5.0

RenderBeams.CreateBeamPoints(beam_info)
```

## DrawBeam

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| BeamInfo_t | BeamInfo_t | - |

## CreateBeamRing

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| BeamInfo_t | BeamInfo_t | - |

## CreateBeamRingPoint

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| BeamInfo_t | BeamInfo_t | - |

## CreateBeamCirclePoints

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| BeamInfo_t | BeamInfo_t | - |
