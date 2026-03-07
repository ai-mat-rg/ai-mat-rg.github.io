---
layout: page
title: About us
permalink: /about
---
We are a group of students, postdocs, professors and research scientists at Mila passionate about the intersection of artificial intelligence and materials science. Our goal is to educate ourselves and the broader community on topics such as machine learning for materials discovery, interatomic potentials, generative models of crystals, and active learning for scientific applications.

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
