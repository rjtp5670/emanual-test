{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}

The Position Trajectory(140) is a desired position trajectory created by the [Profile](#what-is-the-profile).
The Position Trajectory(140) is used only when the [Operating Mode(11)](#operating-mode-{{ passed_model }}){: .popup2} is **the Position Control Mode**, **Extended Position Control Mode**{% if passed_product_group!='dxl_xl430' %} or **Current-based Position Control Mode**{% else %}{% endif %}.
For more details, see [What is the Profile](#what-is-the-profile).
