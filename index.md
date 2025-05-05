---
layout: nocontainer
title: Home
---

<div class="container">
  <div class="row">
    <div class="col">

      <h1><a href="https://castromedia.org">CastroMedia.org</a></h1>

      <h2>Uniting Voices To Amplify Change</h2>
      <p><i>We are a flat anarcho-syndicalist organization where every member has the same power to contribute, vote on decisions, and review content before it goes out. We are working towards having monthly public meetings whose agenda and minutes will be posted on Substack.</i></p>
      
      <img src="/assets/images/banner.jpg" class="image">

      <h2>Mission</h2>
      
      <p>Our mission is to highlight local events and news by bringing together thought leaders and content creators to build a shared brand, enabling those with larger platforms to uplift worthy rising voices.</p>
    </div>
  </div>
  
  <hr>

  <div markdown="0" class="row">

  <h2><a href="/program">Programs:</a></h2>

  {% assign sorted_pages = site.pages | sort: "order" %}
  {% assign counter = 0 %}
  {% for page in sorted_pages %}
    {% if page.path contains "program/" and page.path != "program/index.md" %}
      <div class="col-md-4">
        <h3><a href="{{ page.url }}">{{ page.title }}</a></h3>
        {% if page.thumbnail %}
          <img src="{{ page.thumbnail }}" alt="{{ page.title }} image" class="photo">
        {% endif %}
        {% if page.status %}<p><b>Status:</b> {{ page.status }}</p>{% endif %}
        {% if page.blurb %}<p>{{ page.blurb }}</p>{% endif %}
        {% if page.donate_link %}
          <p><a class="btn btn-primary" href="{{ page.donate_link }}">Donate Now</a></p>
        {% endif %}
      </div><!--/col-md-4-->
    {% endif %}
  {% endfor %}
  <p class="text-right"><a href="/program/">View all programs →</a></p>

  </div><!--/row-->

      
  <hr>

  <div markdown="0" class="row">

  <h2><a href="/updates">Updates:</a></h2>

  {% assign sorted_pages = site.pages | sort: "date" | reverse %}
  {% assign counter = 0 %}
  {% for page in sorted_pages %}
    {% if page.path contains "updates/" and page.path != "updates/index.md" %}
      <p>
        <a href="{{ page.url }}">{{ page.title }}</a><br>
        <small><b>{{ page.date | date: "%B %d, %Y" }}</b></small>
      </p>
    {% endif %}
  {% endfor %}
  <p class="text-right"><a href="/updates/">View all updates →</a></p>

  </div><!--/row-->