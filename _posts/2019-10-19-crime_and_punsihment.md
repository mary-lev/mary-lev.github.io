---
layout: post
title: Talks and Sounds in "Crime and Punishment"
date: 2019-10-19 17:39:00
tags: ipynb, NLP, charts, Dostoevsky
featured: true
description: text analysys and visualisation with Python
---

{::nomarkdown}
{% assign jupyter_path = "assets/jupyter/dostoevsky.ipynb" | relative_url %}
{% capture notebook_exists %}{% file_exists assets/jupyter/dostoevsky.ipynb %}{% endcapture %}
{% if notebook_exists == "true" %}
{% jupyter_notebook jupyter_path %}
{% else %}

<p>Sorry, the notebook you are looking for does not exist.</p>
{% endif %}
{:/nomarkdown}