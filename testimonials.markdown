---
layout: default
title: 推薦語
permalink: /testimonials/
---
<div class="feedback-container">
  <h2>課程教學評語與推薦</h2>
  {% for feedback in site.data.feedbacks %}
    <div class="feedback-entry">
      <div class="photo-and-details">
        {% if feedback.photo %}
          <div class="feedback-photo">
           <img src="{{ site.baseurl }}/assets/images/{{ feedback.photo }}" alt="上傳相片">
          </div>
        {% endif %}
        <div class="feedback-details">
          <h2>{{ feedback.name }}</h2>
          <p><strong>Email:</strong> <a href="mailto:{{ feedback.email }}">{{ feedback.email }}</a></p>
          <p><strong>參加的語言課程:</strong> {{ feedback.courses }}</p>
          <p><strong>整體評價:</strong> 
            {% for i in (1..5) %}
              {% if i <= feedback.rating %}
                <span class="stars">★</span>
              {% else %}
                <span class="stars">☆</span>
              {% endif %}
            {% endfor %}
          </p>
          <p><strong>評語:</strong> {{ feedback.comment }}</p>
        </div>
      </div>
    </div>
    <hr>
  {% endfor %}
</div>