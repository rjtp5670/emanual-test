{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}

The Current Limit(38) indicates maximum current(torque) output limit. The [Goal Current(102)] can’t be configured with any values exceeding the Current Limit(38). The Current Limit(38) is used in Torque Control Mode and Current-based Position Control Mode, therefore decreasing the Current Limit(38) will result in decreasing torque of DYNAMIXEL. For more details, please refer to the [Position PID Gain(80 ~ 84)](#position-pid-gain80-82-84).
