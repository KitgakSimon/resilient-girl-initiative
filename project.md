---
layout: project
title: "Project Gallery"
---

<div class="image-grid">
  {% for img in site.static_files %}
    {% if img.path contains '/assets/img/project/' %}
      <div class="image-item">
        <img src="{{ img.path | relative_url }}" alt="Project Image" onclick="openLightbox('{{ img.path | relative_url }}')">
      </div>
    {% endif %}
  {% endfor %}
</div>

<div id="lightbox" class="lightbox">
  <span class="close" onclick="closeLightbox()">&times;</span>
  <img class="lightbox-content" id="lightbox-img">
</div>
