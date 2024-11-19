---
title: Mi Galería de Fotos
layout: default
---

<div class="gallery">
  {% for image in site.static_files %}
    {% if image.path contains '/images/' %}
      <img src="{{ image.path }}" alt="{{ image.name }}">
    {% endif %}
  {% endfor %}
</div>

<style>
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); 
  grid-gap: 10px;
}

.gallery img {
  max-width: 100%;
  height: auto;
}
</style>