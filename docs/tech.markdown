---
layout: page
title: Tech Blog
categories: tech
---

{% if site.posts.size > 0 %}
  <ul class="post-list">
  {% for post in site.posts %}
  {%- if post.big_category == "tech" -%}
  <li>
    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
    <span class="post-meta">
      {{ post.date | date: date_format }}
    </span>
    <br/>
    <span class="post-meta">
      {% if post.author %}
        {{ post.author }}
      {% else %}
        Ananymous
      {% endif %}
    </span>
    <h3>
      <a class="post-link" href="{{ post.url | relative_url }}">
        {{ post.title | escape }}
      </a>
    </h3>
    {%- if site.show_excerpts -%}
      {{ post.excerpt }}
    {%- endif -%}
  </li>
  {% endif %}
  {%- endfor -%}
  </ul>
{% endif %}
