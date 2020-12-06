{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}

The LED(65) determines LED On or Off.

|    Bit     | Description      |
|:----------:|:-----------------|
| 0(Default) | Turn OFF the LED |
|     1      | Turn ON the LED  |

{% include en/dxl/led_policy.md %}
