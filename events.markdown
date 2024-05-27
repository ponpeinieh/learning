---
layout: default
title: 活動
---

<div class="events-container">
  <h2>活動</h2>
  {% assign sorted_events = site.events | sort: 'date' | reverse %}
  {% for event in sorted_events %}
    <div class="event-item">
      <h2><a href="{{ site.baseurl }}/{{ event.url }}">{{ event.title }}</a></h2>
      <p class="event-date">{{ event.date | date: "%Y年%-m月%-d日" }}</p>
      {% if event.image %}
      <img src="{{ site.baseurl }}/{{ event.image }}" alt="{{ event.title }}" class="event-image">
      {% endif %}
      <p>{{ event.content | strip_html | truncate: 50 }}</p>
      <a href="{{ site.baseurl }}/{{ event.url }}" class="read-more">閱讀更多</a>
    </div>
    <hr>
  {% endfor %}
</div>