
{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}

The Moving(122) indicates whether DYNAMIXEL is in motion or not.
If absolute value of [Present Velocity(128)](#present-velocity-{{ passed_model }}){: .popup2} is greater than [Moving Threshold(24)](#moving-threshold-{{ passed_model }}){: .popup2}, Moving(122) is set to '1'.
Otherwise, it will be cleared to '0'.
However,the Moving(122) will always be set to '1' regardless of Present Velocity(128) while Profile is in progress with [Goal Position(116)](#goal-position-{{ passed_model }}){: .popup2} instruction.

| Value | Description     |
| :------------- | :------------- |
| 0 | Movement is not detected |
| 1 | Movement is detected, or Profile is in progress(Goal Position(116) instruction is being processed) |
