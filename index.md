---
layout: default
title: Home
---




<img src="/assets/images/smi.gif" class="photo">

---

## Here are the stories we're covering:

<div markdown="0">

{% assign update_pages = site.pages | sort: "date" | reverse %}

{% for page in update_pages %}
  {% assign path_parts = page.path | split: "/" %}
  {% if page.path contains "posts/" and path_parts.size == 3 % and page.path != "posts/index.md" %}
    <p>
      <a href="{{ page.url }}">{{ page.title }}</a><br>
      <small><em>{{ page.date | date: "%B %d, %Y" }}</em></small>
      {% if page.blurb %}<p>{{ page.blurb }}</p>{% endif %}
    </p>
  {% endif %}
{% endfor %}

</div>