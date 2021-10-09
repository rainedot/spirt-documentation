# PlayerInfo

{% hint style="info" %}
You can access `PlayerInfo` instance through `GetPlayerInfo` [function](../tables/EngineClient.md)
{% endhint %}

## Fields

| Name            | Type          | Description                                |
| :-------------- | :------------ | :----------------------------------------- |
| fakeplayer      | bool          | Is fake player (e.g. Bot)                  |
| filesdownloaded | unsigned char | Amount of files downloaded from the server |
| ishltv          | bool          | Is HLTV                                    |
| iSteamID        | unsigned long | User's steam id                            |
| steamID64       | int           | User's steam id 64                         |
| userId          | int           | User id                                    |
