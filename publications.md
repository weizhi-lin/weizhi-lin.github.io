---
layout: default
title: Publications
permalink: /publications/
---

## Publications

{% assign publications = site.data.publications %}
{% if publications %}
  {% for publication in publications %}
    <div class="publication">
      <h3>{{ publication.title }}</h3>
      {% if publication.authors %}
        <p>{{ publication.authors }}</p>
      {% endif %}
      {% if publication.conference %}
        <p><strong>Conference:</strong> {{ publication.conference }}</p>
      {% endif %}
      {% if publication.image %}
        <img src="{{ publication.image | relative_url }}" alt="{{ publication.title }}" style="max-width: 100%; height: auto;">
      {% endif %}
      {% if publication.description %}
        <p>{{ publication.description }}</p>
      {% endif %}
      {% if publication.pdf %}
        <p><a href="{{ publication.pdf | relative_url }}" target="_blank">Download PDF</a></p>
      {% endif %}
    </div>
  {% endfor %}
{% else %}
  <p>No publications found.</p>
{% endif %}
