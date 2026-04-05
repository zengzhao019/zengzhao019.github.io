---
layout: page
title: Publications
permalink: /publications/
intro: Representative papers across exceptional-point physics, open quantum dynamics, topological systems, and quantum transport.
---

<div class="panel-shell">
  {% assign pubs = site.publications | sort: 'year' | reverse %}
  {% for pub in pubs %}
  <div class="pub-item">
    <div class="pub-title"><a href="{{ pub.url | relative_url }}">{{ pub.title }}</a></div>
    <div class="pub-meta">{{ pub.authors }} · <em>{{ pub.venue }}</em>{% if pub.volume %} {{ pub.volume }}{% endif %}{% if pub.pages %}, {{ pub.pages }}{% endif %} ({{ pub.year }})</div>
    <div class="pub-links">
      {% if pub.paperurl %}<a href="{{ pub.paperurl }}" target="_blank" rel="noreferrer">DOI</a>{% endif %}
      {% if pub.arxiv %}<a href="{{ pub.arxiv }}" target="_blank" rel="noreferrer">arXiv</a>{% endif %}
    </div>
  </div>
  {% endfor %}
</div>
