---
layout: home
title: Courses
permalink: /courses/
---

# My Fall 2026 Courses

Here are all of my courses for this semester. Click on a course below to learn more about the class and the professor teaching it.

{% assign courses = site.courses | sort: "course_number" %}

{% for course in courses %}
## [{{ course.course_code }} — {{ course.course_title }}]({{ course.url | relative_url }})

{{ course.instructor_name }}{% if course.meeting_time %} · {{ course.meeting_time }}{% endif %}

{% endfor %}
