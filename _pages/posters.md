---
permalink: /posters/
title: "Posters"
layout: default
classes: wide
assets_folder: assets/posters/
---

{% for poster in site.data.posters %}

  {{ poster.category }}


  <figure>
    <a href="{{site.baseurl}}{{page.assets_folder}}{{poster.image}}" target="_blank" class=".btn .btn--success .btn--large">
      <img src="{{site.baseurl}}{{page.assets_folder}}{{poster.thumbnail}}" alt="{{poster.description}}">
    </a>
  </figure>
  <!-- w300 A4 -->


{% endfor %}
