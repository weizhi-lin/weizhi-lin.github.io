<h1 id="publications"></h1>

<h2>
  Publications 
  <temp style="font-size:15px;">[</temp>
  <a href="https://scholar.google.com/citations?user=CylLW1kAAAAJ" target="_blank" style="font-size:15px;">Google Scholar</a>
  <temp style="font-size:15px;">]</temp>
</h2>

<!-- Journals Section -->
<h3>Refereed Journals and Transactions</h3>
<div class="publications">
<ol class="bibliography">
{% for link in site.data.publications.journals %}
<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    <img src="{{ link.image | relative_url }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    <abbr class="badge">{{ link.conference_short }}</abbr>
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em></div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf | relative_url }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
    </div>
  </div>
</div>
</li>
<br>
{% endfor %}
</ol>
</div>

<!-- Proceedings Section -->
<h3>Conference Proceedings</h3>
<div class="publications">
<ol class="bibliography">
{% for link in site.data.publications.proceedings %}
<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    <img src="{{ link.image | relative_url }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    <abbr class="badge">{{ link.conference_short }}</abbr>
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em></div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf | relative_url }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.award %}
      <strong> <i style="color:#BF1013; font-weight:600">{{ link.award }}</i></strong>
      {% endif %}
    </div>
  </div>
</div>
</li>
<br>
{% endfor %}
</ol>
</div>
