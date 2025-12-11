---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">For a full list of my publications please see: <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

## Selected Publications
{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}

## Patents
- [Systems for Generation of Prompts for Evaluation of Language Models (Amazon))](https://ppubs.uspto.gov/api/patents/html/20250378274?source=US-PGPUB&requestToken=eyJzdWIiOiI5MTNhN2ZhYS1jNGNmLTQ1NWEtYmYzZS0wMDAwYzAzMTI2ODkiLCJ2ZXIiOiJkYTI4MzgwMy04NTZjLTRiMzgtYTVmMi1jODNkOWM2ZTAzMmYiLCJleHAiOjB9)