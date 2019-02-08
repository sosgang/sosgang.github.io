---
layout: default
title: Publications
---

## Articles

{% for pub in site.data.publications %}
<p>
    {{ pub.authors }} 
    ({{ pub.year }}). 
    <a href="{{ pub.oa }}">{{ pub.title }}</a>.
    {% if pub.venue %}<em>{{ pub.venue }}</em>{% if pub.volume %}, {{ pub.volume }}{% if pub.issue %} ({{ pub.issue }}){% endif %}{% endif %}{% if pub.pages %}: {{pub.pages}}{% endif %}.{% endif %}
    {% if pub.doi %}doi:<a href="https://doi.org/{{ pub.doi }}">{{ pub.doi }}</a>{% endif %}
    {% if pub.arxiv %}(arXiv:<a href="https://arxiv.org/abs/{{ pub.arxiv }}">{{ pub.arxiv }}</a>){% endif %}
</p>
{% endfor %}

## Datasets

{% for pub in site.data.datasets %}
<p>
    {{ pub.authors }} 
    ({{ pub.year }}). 
    <a href="{{ pub.oa }}">{{ pub.title }}</a>.
    {% if pub.venue %}<em>{{ pub.venue }}</em>.{% endif %}
    {% if pub.doi %}doi:<a href="https://doi.org/{{ pub.doi }}">{{ pub.doi }}</a>{% endif %}
</p>
{% endfor %}