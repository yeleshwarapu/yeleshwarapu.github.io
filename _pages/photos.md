---
permalink: /photos/
title: "photos"
layout: single
---

{% assign cloud_name = "db5cyuuxy" %}
{% assign base_url = "https://yeleshwarapu.github.io" %}

{% for file in site.static_files %}
  {% if file.path contains 'assets/photos/' %}
    <img src="https://res.cloudinary.com/{{ cloud_name }}/image/fetch/w_1000,c_limit,q_auto,f_auto/{{ base_url }}{{ file.path }}" alt="{{ file.name }}" loading="lazy" />
  {% endif %}
{% endfor %}
