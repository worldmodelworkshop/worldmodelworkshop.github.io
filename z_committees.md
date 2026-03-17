---
title: Committees
nav: true
---

## Organizers

<div class="people-grid-container">
  {% for person in site.data.organizers %}
    <div class="person">
      <div class="circle-crop-wrapper">
        <img src="{{ person.image | relative_url }}" alt="{{ person.name }}"
          {% if person.position %}
            style="object-position: {{ person.position }};"
          {% endif %}>
      </div>
      <h3>{{ person.name }}</h3>
      <p>{{ person.role }}</p>
      <p>{{ person.affiliation }}</p>
    </div>
  {% endfor %}
</div>

## Advisory Board
<div class="people-grid-container">
  {% for person in site.data.advisory_board %}
    <div class="person">
      <div class="circle-crop-wrapper">
        <img src="{{ person.image | relative_url }}" alt="{{ person.name }}"
          {% if person.position %}
            style="object-position: {{ person.position }};"
          {% endif %}>
      </div>
      <h3>{{ person.name }}</h3>
      <p>{{ person.role }}</p>
      <p>{{ person.affiliation }}</p>
    </div>
  {% endfor %}
</div>