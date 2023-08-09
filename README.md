---
layout: home
title: SAAS Fall 2023
nav_exclude: true
permalink: /:path/
seo:
  type: Course
  name: Data Foundation
---

# Data Foundations

- [announcements](announcements.md),
- a [course calendar](calendar.md),
- a [staff](staff.md) page,
- and a weekly [schedule](schedule.md).



---
layout: page
title: Calendar
description: Listing of course modules and topics.
---

# Calendar

{% for module in site.modules %}
{{ module }}
{% endfor %}