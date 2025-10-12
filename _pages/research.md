---
title: "Lucas Palazzolo - Research"
layout: gridlay
excerpt: ""
sitemap: false
permalink: /research/
---


# Publications

## Preprints

## Published articles

<div class="publications">
{% for publi in site.data.publist %}
  <p id="pub-{{ publi.number }}">
    [{{ publi.number }}] {{ publi.title }} <br>
    {{ publi.authors }} 
     {% if publi.link2 %}
      — <a href="{{ publi.link1.url }}">{{ publi.link1.display }}</a> • <a href="{{ publi.link2.url }}">{{ publi.link2.display }}</a>
    {% else %}
      — <a href="{{ publi.link1.url }}">{{ publi.link1.display }}</a>
    {% endif %}
  </p>
{% endfor %}
</div>



# Comunications



