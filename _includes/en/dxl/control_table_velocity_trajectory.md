{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}


The Velocity Trajectory(136) is a desired velocity trajectory created by Profile. Operating method can be changed based on its [Operating Mode(11)]. For more details, see the [What is the Profile].
1. **Velocity Control Mode** : When Profile reaches to the endpoint, The Velocity Trajectory(136) becomes equal to the [Goal Velocity(104)].
2. **Position Control Mode, Extended Position Control Mode{% if passed_product_group=='dxl_xl430' %}{% else %}, Current-based Position Control Mode{% endif %}** : Velocity Trajectory is used to create Position Trajectory(140). When Profile reaches to an endpoint, Velocity Trajectory(136) is cleared to '0'.
