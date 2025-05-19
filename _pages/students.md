---
layout: page
permalink: /students/
title: Students
description: 
nav: true
nav_order: 2
---

# Students and Researchers

## Graduate Students
<div class="student-section">
  {% for student in site.data.grad_students %}
  <div class="student-row">
    <div class="student-image">
      <img src="../assets/images/students/{{ student.image }}" alt="{{ student.name }}">
    </div>
    <div class="student-info">
      <strong>{{ student.first_name }}</strong> <strong class="student-full-name">{{ student.name }}</strong>
      <div class="student-details">{{ student.program }}</div>
      {% if student.cosupervisor %}
      <div class="student-details">Co-sup. with {{ student.cosupervisor }}</div>
      {% endif %}
      {% if student.linkedin %}
      <div class="student-links">
        <a href="{{ student.linkedin }}" target="_blank">Profile</a>
      </div>
      {% endif %}
    </div>
  </div>
  {% endfor %}
</div>

## Research Assistants
<div class="student-section">
  {% for student in site.data.research_assistants %}
  <div class="student-row">
    <div class="student-image">
      <img src="../assets/images/students/{{ student.image }}" alt="{{ student.name }}">
    </div>
    <div class="student-info">
      <strong>{{ student.first_name }}</strong> <strong class="student-full-name">{{ student.name }}</strong>
      <div class="student-details">Research Assistant</div>
      {% if student.linkedin %}
      <div class="student-links">
        <a href="{{ student.linkedin }}" target="_blank">Profile</a>
      </div>
      {% endif %}
    </div>
  </div>
  {% endfor %}
</div>

<style>
.student-section {
    margin-bottom: 2em;
}

.student-row {
    display: flex;
    align-items: center;
    margin-bottom: 1.5em;
    padding-bottom: 1em;
    border-bottom: 1px solid #eee;
}

.student-image {
    width: 100px;
    height: 100px;
    margin-right: 1.5em;
    flex-shrink: 0;
}

.student-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 50%;
}

.student-info {
    flex-grow: 1;
}

.student-full-name {
    margin-left: 0.5em;
}

.student-details {
    color: #666;
    margin: 0.3em 0;
    font-size: 0.95em;
}

.student-links a {
    color: #0366d6;
    text-decoration: none;
}

.student-links a:hover {
    text-decoration: underline;
}
</style> 