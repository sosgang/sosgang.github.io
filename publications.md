---
layout: default
title: Publications
---

{% for pub in site.data.publications %}
<p>
    {{ pub.authors }} 
    ({{ pub.year }}). 
    <a href="{{ pub.oa }}">{{ pub.title }}</a>.
    {% if pub.venue %}<em>{{ pub.venue }}</em>{% if pub.volume %}, {{ pub.volume }}{% if pub.issue %} ({{ pub.issue }}){% endif %}{% endif %}{% if pub.pages %}: {{pub.pages}}{% endif %}.{% endif %}
    {% if pub.doi %}DOI: <a href="https://doi.org/{{ pub.doi }}">{{ pub.doi }}</a>{% endif %}
</p>
{% endfor %}