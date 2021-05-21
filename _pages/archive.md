---
layout: page
permalink: /archive
title: Arşiv
---

**Note:** Bu arsiv sayfasi blogdaki tum yazilari ve notlari icerir.

{% for collection in site.collections %}
{% if collection.label != "pages" %}

  <h2>Entries from {{ collection.label | capitalize }}</h2>
  <ul>
    {% for item in site[collection.label] %}
      <li class="archive-links"><a href="{{ item.url }}">{{ item.title }}</a></li>
    {% endfor %}
  </ul>
  {% endif %}
{% endfor %}
