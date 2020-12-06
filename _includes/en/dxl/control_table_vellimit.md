{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}

Velocity Limit(44) indicates the maximum value of [Goal Velocity(104)](#goal-velocity-{{ passed_model }}){: .popup2}. For more details, see [Goal Velocity(104)](#goal-velocity-{{ passed_model }}){: .popup2}

|   Unit   | Value Range |
|:--------:|:-----------:|
| 0.229rpm |  0 ~ 1,023  |

{% if passed_product_group !='xl330' %}
**NOTE**: The default value of Velocity Limit(44) has been decreased since Firmware V42.
{: .notice}
{% endif %}
