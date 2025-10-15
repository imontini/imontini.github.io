---
layout: page
title: "Gallery"
permalink: /gallery/
---

#  Gallery

A collection of photos from my fieldwork, research travels, and talks.

<div class="photo-gallery">
  {% for image in site.static_files %}
    {% if image.path contains 'files/photos/' %}
      <div class="photo-item">
        <img src="{{ image.path }}" alt="{{ image.name }}">
      </div>
    {% endif %}
  {% endfor %}
</div>