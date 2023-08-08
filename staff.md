---
layout: page
title: Staff
description: A listing of all the course staff members.
---

# Staff

Staff information is stored in the `_staffers` directory and rendered according to the layout file, `_layouts/staffer.html`.

{% assign directors = site.staffers | where_exp: "staffer", "staffer.role == 'ED Director' or staffer.role == 'DF Director'" %}
{% assign num_directors = directors | size %}
{% if num_directors != 0 %}
## Director

{% for staffer in directors %}
{{ staffer.name }}
{% if staffer.role %}
### {{ staffer.role }}
{% endif %}
{% if staffer.email %}
Email: {{ staffer.email }}
{% endif %}
{% if staffer.website %}
Website: {{ staffer.website }}
{% endif %}
{% if staffer.photo %}
Photo: {{ staffer.photo }}
{% endif %}
{% if staffer.meta %}
{% for key, value in staffer.meta %}
{{ key }}: {{ value }}
{% endfor %}
{% endif %}
[Schedule an appointment](#){: .btn .btn-outline }
{% endfor %}
{% endif %}



{% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}
## Teaching Assistants

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}
