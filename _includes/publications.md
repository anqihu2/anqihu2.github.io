<h2 id="publications" class="section-heading">Journal Publications</h2>

<div class="publications">
<ol class="bibliography">
{% for link in site.data.publications.main %}
<li>
  <div class="pub-row modern-card">
    {% if link.image %}
    <div class="col-sm-3 abbr pub-media">
      <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" alt="{{ link.title }}">
      {% if link.conference_short %}<abbr class="badge">{{ link.conference_short }}</abbr>{% endif %}
    </div>
    <div class="col-sm-9 pub-content">
    {% else %}
    <div class="col-sm-2 abbr pub-media no-image">
      {% if link.conference_short %}<abbr class="badge">{{ link.conference_short }}</abbr>{% endif %}
    </div>
    <div class="col-sm-10 pub-content">
    {% endif %}
      <div class="title">{% if link.pdf %}<a href="{{ link.pdf }}" target="_blank" rel="noopener">{{ link.title }}</a>{% else %}{{ link.title }}{% endif %}</div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em></div>
      <div class="links">
        {% if link.pdf %}<a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">Paper</a>{% endif %}
        {% if link.code %}<a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">Code</a>{% endif %}
        {% if link.page %}<a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">Project</a>{% endif %}
        {% if link.notes %}<span class="inline-note">{{ link.notes }}</span>{% endif %}
      </div>
    </div>
  </div>
</li>
{% endfor %}
</ol>
</div>
