{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}

{% capture present_pos_notice_01 %}
**NOTE** : {% if passed_product_group=='dxl_pro_a' or passed_product_group=='dxl_p' %} [Present Position(580)](#present-position-{{ passed_model }}){: .popup2} {% elsif passed_product_group=='dxl_pro' %} [Present Position(611)](#present-position-{{ passed_model }}){: .popup2} {% else %} [Present Position(132)](#present-position-{{ passed_model }}){: .popup2} {% endif %} represents 4 byte continuous range from -2,147,483,648 to 2,147,483,647 when Torque is turned off regardless of Operating Mode(11).
However, {% if passed_product_group=='dxl_pro_a' or passed_product_group=='dxl_p' %} Present Position(580) {% elsif passed_product_group=='dxl_pro' %} Present Position(611) {% else %} Present Position(132) {% endif %} will be reset to an absolute position value within one full rotation in following cases:
1. When Operating Mode(11) switches to **Position Control Mode**, {% if passed_product_group=='dxl_pro_a' or passed_product_group=='dxl_p' %} Present Position(580) {% elsif passed_product_group=='dxl_pro' %} Present Position(611) {% else %} Present Position(132) {% endif %} will be reset to an absolute position value within a full rotation.
2. When torque is turned on in **Position Control Mode**, {% if passed_product_group=='dxl_pro_a' or passed_product_group=='dxl_p' %} Present Position(580) {% elsif passed_product_group=='dxl_pro' %} Present Position(611) {% else %} Present Position(132) {% endif %} will be reset to an absolute position value within one full rotation.
3. Turning on the power supply or using [Reboot Instruction](/docs/en/dxl/protocol2/#reboot).

Notice that {% if passed_product_group=='dxl_pro_a' or passed_product_group=='dxl_p' %} Present Position(580) {% elsif passed_product_group=='dxl_pro' %} Present Position(611) {% else %} Present Position(132) {% endif %} value can be affected by {% if passed_product_group=='dxl_pro' %} [Homing Offset(13)](#homing-offset-{{ passed_model }}){: .popup2} {% else %} [Homing Offset(20)](#homing-offset-{{ passed_model }}){: .popup2} {% endif %}.
{% endcapture %}
<div class="notice">{{ present_pos_notice_01 | markdownify }}</div>
