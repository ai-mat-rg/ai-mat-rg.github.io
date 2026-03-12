---
layout: page
title: About us
permalink: /about
---
We are a group of students, postdocs, professors and research scientists at Mila united by a shared enthusiasm for applying AI to accelerate materials discovery and design. We believe that machine learning has the potential to transform how we find and develop new materials: from next-generation semiconductors and battery technologies to catalysts for carbon capture and materials for climate change mitigation. Through regular discussions, paper presentations and invited talks, we aim to build expertise at the intersection of machine learning and the physical sciences.

These are some of the folks co-organising the reading group, in random order:

<div id="team-cards">
{% for person in site.data.team %}
  {% include team-card.html %}
{% endfor %}
</div>

<script>
  const container = document.getElementById('team-cards');
  const cards = Array.from(container.children);
  cards.sort(() => Math.random() - 0.5);
  cards.forEach(card => container.appendChild(card));
</script>
