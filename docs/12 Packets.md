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

### Misc packets
#### Send Whisper
Sends whisper packet to the server

```csharp
bot.SendWhisper("name", "message");
```

### Sending message packet
`SentBy` has a `"SERVER"` option that sends the message without a username

`MessageType` defaults to `"zone"`

There are 7 message types:
- `moderator`
- `warning`
- `server`
- `event`
- `guild`
- `zone`
- `whisper`

These can be sent to client as follows:

```csharp
bot.SendMSGPacket("message", "sentBy", "messageType");
```