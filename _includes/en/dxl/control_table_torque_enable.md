{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}


{% assign torque_enable= "64" %}
{% assign present_position="132" %}
{% assign homing_offset="20" %}

{% if passed_product_group=='dxl_p' or passed_product_group=='dxl_pro_a' or passed_product_group=='rh_p12_rna' %}
{% assign torque_enable= "512" %}
{% assign present_position="580" %}
{% elsif passed_product_group=='dxl_pro' or passed_product_group=='rh_p12_rn' %}
{% assign torque_enable= "562" %}
{% assign present_position="611" %}
{% assign homing_offset="13" %}
{% elsif passed_product_group=='dxl_xl320'' %}
{% assign torque_enable= "24" %}
{% assign present_position="37" %}
{% endif %}

{% if passed_product_group=='dxl_ax' or passed_product_group=='dxl_dx' or passed_product_group=='dxl_ex' or passed_product_group=='dxl_mx' or passed_product_group=='dxl_rx' %}
{% else %}
Torque Enable(64) determines Torque ON/OFF. Writing ‘1’ to Toque Enable's address will turn on the Torque and all Data in the EEPROM area will be locked.
{% endif %}

|   Value    | Description                             |
| :--------: | :-------------------------------------- |
| 0(Default) | Turn off the torque                     |
|     1      | Turn on the torque and lock EEPROM area |

{% if passed_product_group=='dxl_ax' or passed_product_group=='dxl_dx' or passed_product_group=='dxl_ex' or passed_product_group=='dxl_mx' or passed_product_group=='dxl_rx' or passed_product_group=='dxl_xl320' %}
{% else %}
**NOTE** : [Present Position({{ present_position }})](#present-position-{{ passed_model }}){: .popup2} can be reset when [Operating Mode(11)](#operating-mode-{{ passed_model }}){: .popup2} and Torque Enable({{ torque_enable }}) are updated. For more details, please refer to the [Homing Offset({{ homing_offset }})](#homing-offset-{{ passed_model }}){: .popup2} and Present Position
{: .notice}
{% endif %}
