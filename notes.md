---
layout: default
title: Notes
---
{% for notes in site.notes %}
  <div id="post-short">
    <a href="{{site.url}}{{site.baseurl}}{{post.url}}">
      <h3>{{notes.title}}</h3>
    </a>
    <i>posted on {{ post.date | date: "%-d %b %Y" }}</i>
    <p>
      {% if notes.excerpt %}
        {{ notes.excerpt }}
      {% else %}
        {{ notes.content }}
      {% endif %}
    </p>
  </div>
{% endfor %}
