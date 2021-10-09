# GlobalVars

## Fields:

| Name | Type | Description |
| :--- | :--- | :--- |
| realtime | float | Absolute Time |
| framecount | int | Absolute frame counter - continues to increase even if game is paused |
| absoluteframetime | float | Non-paused frametime |
| curtime | float | Current time |
| frametime | float | Time spent on last server or client frame |
| maxClients | int | Current maxplayers setting |
| tickcount | int | Simluation ticks - doesn't increase when game is paused |
| interval_per_tick | float | Simulation tick interval. tickrate = 1/interval_per_tick |
| interpolation_amount | float | Interpolation amount based on fraction of next tick |
| simTicksThisFrame | int | Simulation ticks this frame |
| network_protocol | int | Current saverestore data |
| pSaveData | void\* | Current saverestore data |
| m_bClient | bool | Set to true in client code |
| m_bRemoteClient | bool | True if we are a remote client |
