{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}

{% if passed_product_group=='dxl_mx2' or passed_product_group=='xl330' or passed_product_group=='dxl_x430' or passed_product_group=='dxl_xl430' or passed_product_group=='dxl_xw540' or passed_product_group=='dxl_x540' or passed_product_group=='dxl_pro' or passed_product_group=='dxl_pro_a' or passed_product_group=='dxl_p' or passed_product_group=='rh_p12_rn' or passed_product_group=='rh_p12_rna' %}
{% assign return_delay = "9" %}
{% else %}
{% assign return_delay = "5" %}
{% endif %}

<!-- # Return Delay Time ({{return_delay}}) -->

After the DYNAMIXEL receives an Instruction Packet, it delays transmitting the Status Packet for Return Delay Time({{ return_delay }}).
For instance, if the Return Delay Time({{ return_delay }}) is set to ‘10’, the Status Packet will be returned after 20[μsec] when the Instruction Packet is received.

|Unit| Value Range    | Description     |
| :------------: | :------------: | :------------: |
| 2[μsec] | 0 ~ 254 | Default value ‘250’(500[μsec]), Maximum 508[μsec] |
