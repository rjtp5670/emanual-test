---
layout: popup
---

# Return Delay Time

{{ page.tab_ref.ref1.model }}
{{ page.tab_ref.ref1.product_group }}

{% assign temp_model = include.page.temp_var %}
{{ temp_model }}

{{ page.previous | append : "?" }}

<!-- {% include en/dxl/control_table_return_delay_time.md passed_ref = page.tab_ref.ref1.model %} -->

{{ page.previous }}

<!-- {{ page.url }} -->

<!-- {% assign pages=site.pages | where:"tab_ref", page.tab_ref | sort: 'lang' %}

{% assign pages=site.pages | where:"ref", page.ref | sort: 'lang' %} -->

{% assign temp_model = include.passed_model %}

{{ temp_model }}

{% assign subpage = site.pages | where: 'model', 'xl430-w250' %}
{{ subpage[0].title }}
