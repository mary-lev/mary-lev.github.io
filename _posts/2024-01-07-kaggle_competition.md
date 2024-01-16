---
layout: post
title: My first Kaggle competition
date: 2024-01-07 09:56:00-0400
description: News classification for Russian 
tags: kaggle, classification, news, Russian
categories: competitions, awards
related_posts: true
toc:
  sidebar: left
---

It was <a href="https://www.kaggle.com/competitions/news-scraping-competition/overview">my first kaggle competition</a>, and I have won it!

This fairly simple news classification competition was run by the Faculty of Computer Science (FCS) at the Higher School of Economics (HSE) as part of their bootcamp. What made this win special was how I achieved it: through a simple yet effective approach.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/19.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The Leaderboard.
</div>

## The Challenge
The task was to predict news topics. We were to categorize news as ‘Society/Russia’, ‘Science and Technology’, and other types. Our unique idea was to accumulate training data by scraping news sites. To solve this problem, I first carefully probed the test data. This exploration was very important to selecting which specific data to analyze. As a result, I collected material for three years from Lenta. Ru and four years from Fontanka. Ru.

## Complexity or Simplicity?
At first, I thought about using a less complex model like CatBoost or XGBoost,even went the route of testing out a bit of advanced transformers. I didn't get what I wanted from any of these That took me to the next phase, one in which I decided to rely on the simple side. Using basic techniques like CountVectorizer and TfidfVectorizer, combined with Logistic Regression, I made not only a model that was efficient but amazingly more effective than complex alternatives.

## The Results: A Clear Victory for Simplicity

The approach was successful, with accuracy scores of 0.92 on CountVectorizer and 0.93 on TfidfVectorizer. The final results of this competition were particularly impressive. The public accuracy was 0.98548 and the private score was 0.98756. These numbers demonstrate that carefully-made simple approaches can surpass more intricate ones in efficiency.

In the spirit of community and collaboration, I've uploaded <a href="https://www.kaggle.com/marialevchenko/datasets">both datasets used in this competition to Kaggle</a>. I hope that these resources will help future explorers in their data science pursuits. 

## Exploring Further: Topic Modeling in Russian News

The competition inspired me to explore topic modeling within Russian news texts. I was motivated by my work on news classification. I hope to uncover how subjects and lexicon in Russian news have evolved over the last three years. The purpose of this journey into topic modeling is to gain deeper insights into the shifts in societal and cultural narratives as reflected in the media. This project is ongoing, and I'll keep you updated with my findings as they unfold. 

{::nomarkdown}
{% assign jupyter_path = "assets/jupyter/news-classification.ipynb" | relative_url %}
{% capture notebook_exists %}{% file_exists assets/jupyter/dostoevsky.ipynb %}{% endcapture %}
{% if notebook_exists == "true" %}
{% jupyter_notebook jupyter_path %}
{% else %}

<p>Sorry, the notebook you are looking for does not exist.</p>
{% endif %}
{:/nomarkdown}