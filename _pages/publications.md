---
title: Publications
permalink: /publications/
layout: single
---

{% assign pubs = site.publications | sort: 'year' | reverse %}
{% assign grouped = pubs | group_by: 'year' %}
{% for y in grouped %}
## {{ y.name }}
<ul>
{% for p in y.items %}
  <li>
    {{ p.authors }} ({{ p.year }}). <em>{{ p.title }}</em>. {{ p.venue }}.
    {% if p.doi %} [DOI](https://doi.org/{{ p.doi }}){% endif %}
    {% if p.url %} [Link]({{ p.url }}){% endif %}
    {% if p.pdf %} [PDF]({{ p.pdf | relative_url }}){% endif %}
    {% if p.code %} [Code]({{ p.code }}){% endif %}
  </li>
{% endfor %}
</ul>
{% endfor %}