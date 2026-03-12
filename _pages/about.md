---
layout: page
title: About us
permalink: /about
---
We are a group of students, postdocs, professors and research scientists at Mila united by a shared enthusiasm for applying AI to accelerate materials discovery and design. We believe that machine learning has the potential to transform how we find and develop new materials: from next-generation semiconductors and battery technologies to catalysts for carbon capture and materials for climate change mitigation. Through regular discussions, paper presentations and invited talks, we aim to build expertise at the intersection of machine learning and the physical sciences.

These are some of the folks co-organising the reading group, in random order:

{% assign people = site.data.team | sample: site.data.team.size %}
{% for person in people %}
  {% assign side = forloop.index0 | modulo: 2 %}
    {% if side == 0 %}
      {% include team-card.html %}
    {% else %}
      {% include team-card.html %}
    {% endif %}
{% endfor %}
