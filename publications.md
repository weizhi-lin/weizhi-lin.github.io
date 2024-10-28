---
layout: default
title: Publications
permalink: /publications/
---

{% assign publications = site.data.publications %}
{% for publication in publications %}
<div class="publication">
  <h3>{{ publication.title }}</h3>
  {% if publication.image %}
  <img src="{{ publication.image | relative_url }}" alt="{{ publication.title }}" style="max-width: 100%; height: auto;">
  {% endif %}
  <p>{{ publication.description }}</p>
</div>
{% endfor %}
