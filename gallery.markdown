---
layout: default
title: 剪影
permalink: /gallery/
---

<div class="gallery-container">
  <h2>剪影</h2>
  
    {% for photo in site.data.gallery.photos %}
    <div class="row">
      <div class="column">
        <img src="{{ site.baseurl }}/assets/images/{{ photo.src }}" alt="{{ photo.alt }}">
        <h3>{{ photo.title }}</h3>
         {% if photo.description %}
          <p>{{ photo.description }}</p>
        {% endif %}
      </div>
    </div>
    {% endfor %}
  
</div>