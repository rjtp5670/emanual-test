{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}

| Value | Description                           |
|:-----:|:--------------------------------------|
|   0   | REG_WRITE instruction is not received |
|   1   | REG_WRITE instruction is received     |

**NOTE** : If ACTION instruction is executed, the value will be changed to 0.
{: .notice}
