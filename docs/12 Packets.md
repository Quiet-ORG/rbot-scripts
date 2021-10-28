Packets
======
#### Sending to Server
Packets can be sent from the client to the server easily through `ScriptInterface#SendPacket`. For example, to send the rest packet, you can use:

```csharp
bot.SendPacket("%xt%zm%restRequest%1%%");
```

#### Simulating Server Packets
You can also simulate packets being sent from the server to the client. You can simulate the 3 types of packets used by the game:
- `json` - JSON packets.
- `xml` - XML packets.
- `str` - String packets, ones that contain %s.

These can be sent to the client as follows:

```csharp
bot.SendClientPacket("packet", "type");
```

## Misc packets