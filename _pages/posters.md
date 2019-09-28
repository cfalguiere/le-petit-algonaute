---
permalink: /posters/
title: "Posters"
layout: splash
classes: wide
assets_folder: /assets/posters/
---

<div>
  <span style="font-size:2em;font-family: 'Dancing Script', cursive;font-weight: bold;">Les posters</span>

</div>

{% for category in site.data.poster-categories %}
  <div style="float:left;margin: 5px">
    <a href="#{{ category.name }}"><img width="100" height="100" src="{{site.baseurl}}/assets/images/authors/{{ category.image }}" alt="cat. image"></a>
    <br>
    <a href="#{{ category.name }}">{{ category.name }}</a>
  </div>
{% endfor %}

<br>

{% for poster in site.data.posters %}

  <a name="{{ poster.category }}"></a>
  <div style="float:left;margin: 5px">
    <div>
      <span style="font-size:0.7em;font-weight: bold;"><i class="fas fa-fw fa-tags" aria-hidden="true"></i>&nbsp;{{ poster.category }}</span><br>
      <a href="{{site.baseurl}}{{page.assets_folder}}{{poster.image}}" target="_blank" class=".btn .btn--success .btn--large">
        <img src="{{site.baseurl}}{{page.assets_folder}}{{poster.thumbnail}}" alt="{{poster.description}}">
      </a>
    <!-- w300 A4 -->
    </div>
  </div>


{% endfor %}
