---
layout: page
title: "Gallery"
permalink: /gallery/
---

<p style="text-align: center;">
Here is a collection of photos from my fieldwork, research travels, and talks.
</p>

<div class="photo-gallery">
  {% for image in site.static_files %}
    {% if image.path contains 'files/photos/' %}
      <div class="photo-item">
        <img src="{{ image.path }}" alt="{{ image.name }}">
      </div>
    {% endif %}
  {% endfor %}
</div>
