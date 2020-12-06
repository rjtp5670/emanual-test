{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}

Use the Goal Velocity(104) to set a desired velocity when the [Operating Mode(11)](#operating-mode-{{ passed_model }}){: .popup2} is **Velocity Control Mode**.

Be aware that the Goal Velocity(104) is not to limit moving velocity.

|   Unit    |                 Value Range                  |
|:---------:|:--------------------------------------------:|
| 0.229 rpm | -Velocity Limit(44) ~ Velocity Limit(44) |

**NOTE**: This value cannot exceed [Velocity Limit(44)](#velocity-limit-{{ passed_model }}){: .popup2}.
{: .notice}

**NOTE** : The maximum velocity and maximum torque of DYNAMIXEL is affected by supplying voltage.
Therefore, if supplying voltage changes, so does the maximum velocity. This manual complies with recommended supply voltage(12[V]).
{: .notice}

**NOTE** : If [Profile Acceleration(108)](#profile-acceleration-{{ passed_model }}){: .popup2} and Goal Velocity(104) are modified simultaneously, modified Profile Acceleration(108) will be used to process Goal Velocity(104).
{: .notice}
