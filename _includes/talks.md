<h2 id="talks" class="section-heading">Selected Talks and Posters</h2>

<div class="publications">
<ol class="bibliography">
{% for link in site.data.talks.main %}
<li>
  <div class="pub-row modern-card">
    <div class="col-sm-3 abbr pub-media">
      {% if link.conference_short %}<abbr class="badge">{{ link.conference_short }}</abbr>{% endif %}
    </div>
    <div class="col-sm-9 pub-content">
      <div class="title">{% if link.pdf %}<a href="{{ link.pdf }}" target="_blank" rel="noopener">{{ link.title }}</a>{% else %}{{ link.title }}{% endif %}</div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em></div>
      <div class="links">
        {% if link.pdf %}<a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">PDF</a>{% endif %}
        {% if link.page %}<a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">Link</a>{% endif %}
        {% if link.notes %}<span class="inline-note">{{ link.notes }}</span>{% endif %}
      </div>
    </div>
  </div>
</li>
{% endfor %}
</ol>
</div>
