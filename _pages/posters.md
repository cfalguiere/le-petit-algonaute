---
permalink: /posters/
title: "Posters"
layout: splash
classes: wide
assets_folder: assets/posters/
---

{% for poster in site.data.posters %}

  <div style="float:left;margin: 5px">
    <div>
      <b>{{ poster.category }}</b></br>
      <a href="{{site.baseurl}}{{page.assets_folder}}{{poster.image}}" target="_blank" class=".btn .btn--success .btn--large">
        <img src="{{site.baseurl}}{{page.assets_folder}}{{poster.thumbnail}}" alt="{{poster.description}}">
      </a>
    <!-- w300 A4 -->
    </div>
  </div>


{% endfor %}
