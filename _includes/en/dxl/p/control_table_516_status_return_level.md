This value decides how to return Status Packet when the device receives an Instruction Packet.

| Value |        Responding Instructions         |              Description              |
|:-----:|:--------------------------------------:|:-------------------------------------:|
|   0   |            PING Instruction            |     Returns PING Instuction only      |
|   1   | PING Instruction<br />READ Instruction | Returns PING and READ Instuctions only |
|   2   |            All Instructions            |       Returns all Instructions        |

**NOTE** : If the Instruction Packet ID is set to the Broadcast ID(0xFE), Status Packet will not be returned for READ and WRITE Instructions regardless of Status Return Level. For more details, please refer to the [Status Packet] section of [Protocol 2.0].
{: .notice}

**WARNING** : Modebus-RTU dose not support Status Return Level(516).    
{: .notice--warning}

[Status Packet]: /docs/en/dxl/protocol2/#status-packet
[Protocol 2.0]: /docs/en/dxl/protocol2/
