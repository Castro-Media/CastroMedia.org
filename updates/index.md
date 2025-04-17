---
layout: default
title: Updates
---

## Updates

<div markdown="0">

{% assign update_pages = site.pages | sort: "date" | reverse %}

{% for page in update_pages %}
  {% if page.path contains "updates/" and page.path != "updates/index.md" %}
    <p>
      <a href="{{ page.url }}">{{ page.title }}</a><br>
      <small><em>{{ page.date | date: "%B %d, %Y" }}</em></small>
    </p>
  {% endif %}
{% endfor %}

</div>
