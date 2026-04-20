---
title: Essays
layout: base
header-title: Essays
---

# Essays

This template includes three sample essays on Southwest food history — nachos, chiles, and tamales — written with AI assistance as placeholder content. They're here to demonstrate what student essays can look like: how to use images, pull quotes, scrolling backgrounds, and other Xanthan components in a longer piece of writing.

Browse them to get a feel for the format. When you're ready to build your own project, you'll replace these with your students' essays — same structure, your topic.

{% assign cards = "" | split: "" %}
{% for p in site.pages %}
  {% if p.path contains 'essays/' and p.path != 'essays/index.md' and p.name == 'index.md' %}
    {% assign segments = p.path | split: '/' %}
    {% if segments.size == 3 %}
      {% assign cards = cards | push: p %}
    {% endif %}
  {% endif %}
{% endfor %}

{% include nav/card-grid.html cards=cards %}