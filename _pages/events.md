---
layout: page
title: Events and sessions
permalink: /events
---
{% assign today = 'now' | date: "%Y-%m-%d" %}
{% assign future_events = "" | split: "," %}
{% assign past_events = "" | split: "," %}

{% for event in site.data.events %}
  {% assign event_date = event.date | date: "%Y-%m-%d" %}
  {% if event_date >= today %}
      {% assign future_events = future_events | push: event %}
  {% else %}
      {% assign past_events = past_events | push: event %}
  {% endif %}
{% endfor %}

Sessions of the AI Mat Reading Group take place every other Wednesday at 2:00 PM at Mila, in person and online.

By attending the sessions of the reading group, participants are requested to follow the [Berlin Code of Conduct](https://berlincodeofconduct.org/en).

## Coming up
{% assign events = future_events | sort: 'date' %}
{% if events.size == 0 %}
There are not currently any planned events. Stay tuned!
{% else %}
  {% for event in events %}
  {% include event.html %}
  {% endfor %}
{% endif %}

## Past sessions
{% assign events = past_events | sort: 'date' | reverse %}
{% for event in events %}
  {% include event.html %}
{% endfor %}
