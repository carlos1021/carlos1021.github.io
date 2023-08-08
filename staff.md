---
layout: page
title: Staff
description: A listing of all the course staff members.
---

# Staff

Staff information is stored in the `_staffers` directory and rendered according to the layout file, `_layouts/staffer.html`.


{% assign directors = site.staffers | where: 'role', 'Director' %}

### Directors

{% for staffer in directors %}
{{ staffer }}
{% endfor %}

<!-- [Schedule an appointment](#){: .btn .btn-outline } -->

<!-- {% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}
## Teaching Assistants

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %} -->
