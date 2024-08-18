---
layout: home
title: Home
nav_exclude: true
---

<div class="d-flex">
	<div>
		<img src="assets/images/morgan-state-logo.jpg" width="100" alt="Morgan State Logo" />
	</div>
	<div>
		<h1 class="mb-1">{{ site.tagline }}</h1>
		<p class="fs-6 fw-300">{{ site.description }}</p>
	</div>
</div>

<!--{% if site.announcements %}
{{ site.announcements.last }}
[Announcements](announcements.md){: .btn .btn-outline .fs-3 }
{% endif %}-->

Welcome to COSC 111! This is the first class in the computer science sequence and doesn’t require any prior programming knowledge. As such, we'll be focusing on foundational knowledge as well as developing skills that will help you succeed in future courses.

This site is the one-stop resource for sections H02 and 004.

See the [syllabus](/syllabus) for more details on course policies and logistics and the [calendar](/calendar) for office hours, due dates, and class times. 

## Course Materials
{% for module in site.modules %}
{{ module }}
{% endfor %}