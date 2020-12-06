{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}

The Status Return Level(68) decides how to return Status Packet when DYNAMIXEL receives an Instruction Packet.

| Value |        Responding Instructions         |              Description               |
|:-----:|:--------------------------------------:|:--------------------------------------:|
|   0   |            PING Instruction            |      Returns PING Instuction only      |
|   1   | PING Instruction<br />READ Instruction | Returns PING and READ Instuctions only |
|   2   |            All Instructions            |        Returns all Instructions        |

{% if passed_product_group=='xl330' %}

**NOTE** : If the [Instruction Packet ID](/docs/en/dxl/protocol2/) is set to the [Broad Cast ID(0xFE)](/docs/en/dxl/protocol2/#packet-id), Status Packet will not be returned for READ and WRITE Instructions regardless of Status Return Level. For more details, please refer to the `Status Packet` section for [Protocol 2.0].
{: .notice}

{% else %}

**NOTE** : If the Instruction Packet ID is set to the Broadcast ID(0xFE), Status Packet will not be returned for READ and WRITE Instructions regardless of Status Return Level. For more details, please refer to the `Status Packet` section for [Protocol 1.0] or [Protocol 2.0].
{: .notice}

`1` Packet ID is the field that indicates an ID of the device that should receive the Instruction Packet and process it.

{% endif %}

[Protocol 1.0]: /docs/en/dxl/protocol1/#status-packet
[Protocol 2.0]: /docs/en/dxl/protocol2/#status-packet
