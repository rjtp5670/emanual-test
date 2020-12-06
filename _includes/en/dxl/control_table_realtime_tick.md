{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}

The Realtime Tick(120) indicates DYNAMIXEL's time.

| Unit | Value Range |                  Description                   |
|:----:|:-----------:|:----------------------------------------------:|
| 1 ms | 0 ~ 32,767  | The value resets to '0' when it exceeds 32,767 |
