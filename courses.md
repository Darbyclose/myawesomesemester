---
layout: default
title: Courses
permalink: /courses/
---
<div class="course-sparkles">
  <span>✦</span>
  <span>✧</span>
  <span>✦</span>
  <span>✧</span>
  <span>✦</span>
  <span>✧</span>
  <span>✦</span>
  <span>✧</span>
</div>

# My Fall 2026 Courses

Here are all of my courses for this semester. Click on a course below to learn more about the class and the professor teaching it.

<div class="course-directory">
  <ol class="course-list">
    {% assign courses = site.courses | sort: "course_number" %}
    {% for course in courses %}
      <li class="course-list__item">
        <a class="course-list__link" href="{{ course.url | relative_url }}">
          <span class="course-list__code">{{ course.course_code }}</span>
          <span class="course-list__title">{{ course.course_title }}</span>
        </a>

        <p class="course-list__meta">
          {{ course.instructor_name }}{% if course.meeting_time %} · {{ course.meeting_time }}{% endif %}{% if course.location %} · {{ course.location }}{% endif %}
        </p>
      </li>
    {% endfor %}
  </ol>
</div>
