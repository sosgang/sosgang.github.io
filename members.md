---
layout: default
title: Members
---

{% for member in site.data.members %}
<div id="{{member.orcid}}" class="mem">
    <img src="{{ member.pic }}" />
    <p><strong>{{ member.name }}</strong></p>
    <p><span>ORCID:</span> <a href="https://orcid.org/{{ member.orcid }}">{{ member.orcid }}</a></p>
    <p><span>Email:</span> <a href="mailto:{{ member.email }}">{{ member.email }}</a></p>
    <p><span>GitHub:</span> <a href="https://github.com/{{ member.github }}">{{ member.github }}</a></p>
    {% if member.twitter %}<p><span>Twitter:</span> <a href="https://twitter.com/{{ member.twitter }}">@{{ member.twitter }}</a></p>{% endif %}
    <p><span>Affiliation:</span> <a href="{{ member.affiliation_url }}">{{ member.affiliation }}</a></p>
    <p><span>Short bio:</span> {{ member.bio }}</p>
</div>
{% endfor %}

## Collaborators
<div id="collaborators" class="mem">
{% for collaborator in site.data.collaborators %}
<p><strong>{{ collaborator.name }}</strong>{% if collaborator.affiliation %}, {{ collaborator.affiliation }}{% endif %}</p>
{% endfor %}
</div>
