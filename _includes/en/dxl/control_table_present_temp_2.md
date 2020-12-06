{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}

The Present Temperature(146) indicates internal temperature of DYNAMIXEL. For more details, see the [Temperature Limit(31)]#temperature-limit-{{ passed_model }}{: .popup2}.
