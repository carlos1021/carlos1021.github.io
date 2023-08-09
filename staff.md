---
layout: page
title: Directors
description: A listing of all the course staff members.
---

# Staff



{% assign ed_directors = site.staffers | where: 'role', 'Education Director' %}
{% assign df_directors = site.staffers | where: 'role', 'Data Foundations Director' %}

### Education Directors
{% for staffer in ed_directors %}
{{ staffer }}
{% endfor %}

### Data Foundations Directors
{% for staffer in df_directors %}
{{ staffer }}
{% endfor %}



<!-- {% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}
## Teaching Assistants

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %} -->
