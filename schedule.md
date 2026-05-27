---
title: Schedule
nav: true
---
<h2> Workshop Timeline </h2>
<div class="schedule-timeline">
  {% for event in site.data.schedule_timeline %}
    <div class="timeline-item">
      
      <div class="timeline-time">
        <span class="time-start">{{ event.start_time }}</span>
        <span class="time-end">{{ event.end_time }}</span>
      </div>

      <div class="timeline-marker">
        <div class="marker-circle class-{{ event.category_type }}"></div>
        <div class="marker-line"></div>
      </div>

      <div class="timeline-content">
        <div class="content-meta">
          {% for cat in event.categories %}
            <span class="category-pill pill-{{ cat.category_type }}">
              {{ cat.category }}
            </span>
          {% endfor %}
          {% if event.duration %}
            <span class="duration">{{ event.duration }}</span>
          {% endif %}
        </div>
        
        <h4 class="event-title">{{ event.title }}</h4>
        
        {% if event.speaker %}
          <p class="event-speaker">
            <strong>{{ event.speaker }}</strong>
            {% if event.affiliation %}
              <span class="affiliation">&middot; {{ event.affiliation }}</span>
            {% endif %}
          </p>
        {% endif %}

        {% if event.subevents %}
          <div class="subevents-container">
            {% for sub in event.subevents %}
              <div class="subevent-item">
                <span class="subevent-time">{{ sub.time }}</span>
                <span class="subevent-title">{{ sub.title }}</span>
              </div>
            {% endfor %}
          </div>
        {% endif %}
        
      </div>
      
    </div>
  {% endfor %}
</div>
