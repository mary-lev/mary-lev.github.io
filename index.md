---
title: Home
layout: page
---
# Home of Concordances

Просто какой-то текст

## Еще заголовок

И снова текст

### Check for deployment

One check

<ul>
  {% for post in site.posts reversed %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>
