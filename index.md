---
layout: default
title: Home
---

## Uniting Voices To Amplify Change
 *We are a flat anarcho-syndicalist organization where every member has the same power to contribute, vote on decisions, and review content before it goes out. We are working towards having monthly public meetings whose agenda and minutes will be posted on Substack.*

<img src="/assets/images/banner.jpg" class="image">

## Mission

Our mission is to highlight local events and news by bringing together thought leaders and content creators to build a shared brand, enabling those with larger platforms to uplift worthy rising voices.

## Programs

- **What's Happening Around Town:** We are working on a community-driven system to see all the events going on wherever you are, including information from activists about any active boycotts.
- **Social Murder Institute:** Documenting the way policies and policymakers choose to cause unnecessary harm.
  - **KleptNews.org:** Documenting the way oligarchs steal from the people and the future to enrich themselves.
- **Beneficial Merch:** Contributors will be able to create merchandise whose revenue goes directly to specific, worthy causes.

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
