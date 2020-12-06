{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}

The PWM Limit(36) indicates maximum PWM output. [Goal PWM(100)](#goal-pwm-{{ passed_model }}){: .popup2} can’t be configured with any values exceeding PWM Limit(36). PWM Limit(36) is commonly used in all operating mode as an output limit, therefore decreasing PWM output will result in decreasing torque and velocity. For more details, please refer to the Gain section of each operating modes.

|         Values          |     Description      |
|:-----------------------:|:--------------------:|
| 0(0 [%]) ~ 885(100 [%]) | 885 = 100 [%] output |
