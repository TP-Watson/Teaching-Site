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
    [Link]({{ p.url | relative_url }})
  </li>
{% endfor %}
</ul>
{% endfor %}