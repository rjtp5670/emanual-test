{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}

The Present Position(132) indicates present Position. For more details, see the (#goal-position-{{ passed_model }}){: .popup2}.

{% include en/dxl/control_table_opmode_note.md passing_model=include.passing_model passed_ref = include.passed_ref %}
