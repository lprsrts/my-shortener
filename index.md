---
layout: default   # you can drop this if you have no layout
title: All Short Links
---

# 🔗 All Short Links

<ul>
{% for page in site.pages %}
  {% if page.redirect_to %}
    <li>
      <a href="{{ page.url | relative_url }}">
        {{ page.title | default: page.url | replace: "/", "" }}
      </a>
      &rarr;
      <small>{{ page.redirect_to }}</small>
    </li>
  {% endif %}
{% endfor %}
</ul>