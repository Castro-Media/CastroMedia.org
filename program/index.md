---
layout: default
title: Programs
---

## Programs:

<div markdown="0">

{% assign sorted_pages = site.pages | sort: "order" %}

{% for page in sorted_pages %}
  {% if page.path contains "program/" and page.path != "program/index.md" %}
    <hr>
    {% if page.thumbnail %}
      <img src="{{ page.thumbnail }}" alt="{{ page.title }} image" style="max-width: 100%; height: auto; border-radius: 8px; margin-bottom: 1rem;">
    {% endif %}
    <h2><a href="{{ page.url }}">{{ page.title }}</a></h2>
    {% if page.status %}<p><em>Status:</em> {{ page.status }}</p>{% endif %}
    {% if page.blurb %}<p>{{ page.blurb }}</p>{% endif %}
    {% if page.donate_link %}
      <p><a class="btn btn-primary" href="{{ page.donate_link }}">Donate Now</a></p>
    {% endif %}
  {% endif %}
{% endfor %}

</div>

[← Back to Home](/)
