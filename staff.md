---
layout: page
title: Staff
description: A listing of all the course staff members.
---

# Staff

Staff information is stored in the `_staffers` directory and rendered according to the layout file, `_layouts/staffer.html`.


{% assign ed_directors = site.staffers | where: 'role', 'ED Director' %}
{% assign df_directors = site.staffers | where: 'role', 'DF Director' %}

### ED Directors
{% for staffer in ed_directors %}
{{ staffer }}
{% endfor %}

### DF Directors
{% for staffer in df_directors %}
{{ staffer }}
{% endfor %}


{% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}
## Teaching Assistants

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}
