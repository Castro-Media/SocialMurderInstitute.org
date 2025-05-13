---
layout: default
title: Home
---

# SocialMurderInstitute.org
Researching and publishing data and analysis attributing harms in society to the organizations and policies directly responsible for them.


<div markdown="0">

{% assign update_pages = site.pages | sort: "date" | reverse %}

{% for page in update_pages %}
  {% if page.path contains "posts/" and page.path != "posts/index.md" %}
    <p>
      <a href="{{ page.url }}">{{ page.title }}</a><br>
      <small><em>{{ page.date | date: "%B %d, %Y" }}</em></small>
    </p>
  {% endif %}
{% endfor %}

</div>
