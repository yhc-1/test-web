---
layout: page
permalink: /students/
title: Students
description: 
nav: true
nav_order: 2
---

## Graduate Students
<div class="student-section">
  {% for student in site.data.grad_students %}
  <div class="student-row">
    <div class="student-image">
      <img src="../assets/images/students/{{ student.image }}" alt="{{ student.name }}">
    </div>
    <div class="student-info">
      {% if student.linkedin %}
      <a href="{{ student.linkedin }}" target="_blank" class="student-name-link">
        <strong class="student-full-name">{{ student.name }}</strong>
      </a>
      {% else %}
      <strong class="student-full-name">{{ student.name }}</strong>
      {% endif %}
      <div class="student-details">{{ student.program }}</div>
      {% if student.cosupervisor %}
      <div class="student-details">Co-sup. with {{ student.cosupervisor }}</div>
      {% endif %}
    </div>
  </div>
  {% endfor %}
</div>

## Research Assistants
<div class="student-section">
  {% for student in site.data.research_assistants %}
  <div class="student-row">
    <div class="student-info">
      {% if student.linkedin %}
      <a href="{{ student.linkedin }}" target="_blank" class="student-name-link">
        <strong class="student-full-name">{{ student.name }}</strong>
      </a>
      {% else %}
      <strong class="student-full-name">{{ student.name }}</strong>
      {% endif %}
      <div class="student-details">Research Assistant</div>
    </div>
  </div>
  {% endfor %}
</div>

## Undergraduate Students
<div class="student-section">
  {% for student in site.data.undergrads %}
  <div class="student-row">
    {% if student.image %}
    <div class="student-image">
      <img src="../assets/images/students/{{ student.image }}" alt="{{ student.name }}">
    </div>
    {% endif %}
    <div class="student-info">
      {% if student.linkedin %}
      <a href="{{ student.linkedin }}" target="_blank" class="student-name-link">
        <strong class="student-full-name">{{ student.name }}</strong>
      </a>
      {% else %}
      <strong class="student-full-name">{{ student.name }}</strong>
      {% endif %}
      <div class="student-details">{{ student.type }} ({{ student.major }}) • {{ student.terms }}</div>
      <div class="student-details research-field">{{ student.research }}</div>
      {% if student.paper %}
      <div class="student-details">
        <a href="{{ student.paper }}" target="_blank" class="paper-link">
          <i class="fas fa-file-alt"></i> Publication
        </a>
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
    align-items: flex-start;
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

.student-name-link {
    text-decoration: none;
    color: inherit;
}

.student-name-link:hover {
    text-decoration: underline;
}

.student-details {
    color: #666;
    margin: 0.3em 0;
    font-size: 0.95em;
}

.research-field {
    font-style: italic;
}

.paper-link {
    color: #0366d6;
    text-decoration: none;
}

.paper-link:hover {
    text-decoration: underline;
}

.paper-link i {
    margin-right: 0.3em;
}
</style>

<!-- Font Awesome for paper icon -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css"> 