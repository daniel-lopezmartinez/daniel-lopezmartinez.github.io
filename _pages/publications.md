---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">For a full list of my publications please see: <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}
- [Selected Publications](#selected-publications)
- [Patents](#patents)

{% include base_path %}

## Selected Publications
{% for post in site.publications reversed %}
  {% if post.category == 'patents' %}
    {% continue %}
  {% endif %}
  {% include archive-single.html %}
{% endfor %}

## Patents
{% for post in site.publications reversed %}
  {% if post.category != 'patents' %}
    {% continue %}
  {% endif %}
  {% include archive-single.html %}
{% endfor %}
