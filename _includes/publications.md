<h2 id="publications">Selected Publications</h2>

<p class="publication-note">* Equal contribution · <a href="{{ site.cv_link | relative_url }}">Full publication list in CV</a></p>

<ol class="publication-list">
{% for paper in site.data.publications.main %}
  <li class="pub-row">
    {% if paper.image %}
    <img class="publication-image" src="{{ paper.image | relative_url }}" alt="" loading="lazy">
    {% endif %}
    <div class="publication-detail">
      <h3><a href="{{ paper.pdf }}">{{ paper.title | escape }}</a></h3>
      <p class="publication-authors">{{ paper.authors | remove: ' (*Co-first authors)' }}</p>
      <p class="publication-venue">{{ paper.conference }}</p>
      {% if paper.summary %}
      <p class="publication-summary">{{ paper.summary | escape }}</p>
      {% endif %}
      {% if paper.code or paper.page or paper.bibtex %}
      <p class="publication-links">
        {% if paper.code %}<a href="{{ paper.code }}">Code</a>{% endif %}
        {% if paper.page %}<a href="{{ paper.page }}">Project page</a>{% endif %}
        {% if paper.bibtex %}<a href="{{ paper.bibtex }}">BibTeX</a>{% endif %}
      </p>
      {% endif %}
    </div>
  </li>
{% endfor %}
</ol>
