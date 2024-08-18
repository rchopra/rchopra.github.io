---
layout: page
title: Staff
description: All the people making COSC 111 possible this semester.
---

# Staff

For a quicker response on homework or project help, please ask on
[EdStem](https://edstem.org/us/courses/60560) rather than emailing staff
members individually. On EdStem, all staff members (and students!) can see your
question and answer it.

## Instructor
{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign morgan_tas = site.staffers | where: 'role', 'Morgan TA' %}
{% assign num_morgan_tas = morgan_tas | size %}
{% if num_morgan_tas != 0 %}

## Morgan TAs

{% for staffer in morgan_tas %}
{{ staffer }}
{% endfor %}
{% endif %}

{% assign google_tas = site.staffers | where: 'role', 'Google TA' %}
{% assign num_google_tas = google_tas | size %}
{% if num_google_tas != 0 %}

## Google TAs

{% for staffer in google_tas %}
{{ staffer }}
{% endfor %}
{% endif %}
