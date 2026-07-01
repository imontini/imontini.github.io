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
    {% if image.path contains 'files/photos/' and image.extname != '.DS_Store' %}
      {% assign ext = image.extname | downcase %}
      {% if ext == '.jpg' or ext == '.jpeg' or ext == '.png' or ext == '.gif' or ext == '.webp' %}
        <div class="photo-item">
          <img src="{{ image.path | relative_url }}" alt="{{ image.name }}">
        </div>
      {% endif %}
    {% endif %}
  {% endfor %}
</div>
