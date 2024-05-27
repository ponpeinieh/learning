---
layout: default
title: 工作室剪影
---
<div class="gallery-container">
  <h2>工作室剪影</h2>
  <div class="gallery-row">
    {% for photo in site.data.gallery.photos %}
      <div class="gallery-column">
        <img src="{{ site.baseurl }}/assets/images/{{ photo.src }}" alt="{{ photo.alt }}">
        <h3>{{ photo.title }}</h3>
        <p>{{ photo.description }}</p>
      </div>
      {% if forloop.index0 | modulo: 2 == 1 and forloop.index0 != forloop.length - 1 %}
        </div><div class="gallery-row">
      {% endif %}
    {% endfor %}
  </div>
</div>