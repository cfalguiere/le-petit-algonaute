---
permalink: /posters/
title: "Posters"
layout: splash
classes: wide
assets_folder: assets/posters/
---

{% for poster in site.data.posters %}

  <div style:'float:left'>
      <p><b></b>{{ poster.category }}</b></p>
      <a href="{{site.baseurl}}{{page.assets_folder}}{{poster.image}}" target="_blank" class=".btn .btn--success .btn--large">
        <img src="{{site.baseurl}}{{page.assets_folder}}{{poster.thumbnail}}" alt="{{poster.description}}">
      </a>
    <!-- w300 A4 -->
  </div>


{% endfor %}
