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

I have won <a href="https://www.kaggle.com/competitions/news-scraping-competition/overview">my first Kaggle competition</a>. This fairly simple news classification competition was run by the Faculty of Computer Science (FCS) at the Higher School of Economics (HSE) as part of their bootcamp. What made this win special was how I achieved it: through a simple yet effective approach.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/19.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The Leaderboard.
</div>

## The Challenge
The task was to predict news topics without any training data. Our goal was to classify news into categories such as 'Society/Russia', 'Science and Technology' and more. The unique aspect was that we obtained our training data by scraping news sites. To tackle this, I first carefully explored the test data. This exploration was crucial in deciding which specific data to analyse. As a result, I collected data from Lenta.Ru for four years and Fontanka.Ru for three years.

## Complexity or Simplicity?
Initially I dabbled with complex models such as CatBoost and XGBoost, and even tried advanced transformers, but these didn't produce the desired results. This led me to a pivotal moment where I decided to embrace simplicity. Using basic techniques such as CountVectorizer and TfidfVectorizer, along with Logistic Regression, I developed a model that was not only efficient, but surprisingly more effective than the complex alternatives.

## The Results: A Clear Victory for Simplicity

The approach was successful, achieving accuracy scores of 0.92 with CountVectorizer and 0.93 with TfidfVectorizer. The competition's final scores were particularly impressive, with a public accuracy of 0.98548 and a private score of 0.98756. These figures demonstrate the effectiveness of a well-considered, simple approach over more complex ones.

In the spirit of community and collaboration, I've uploaded <a href="https://www.kaggle.com/marialevchenko/datasets">both datasets used in this competition to Kaggle</a>. I hope that these resources will help future explorers in their data science pursuits. 

## Exploring Further: Topic Modeling in Russian News

The competition inspired me to explore topic modeling within Russian news texts. I was motivated by my work on news classification. I hope to uncover how subjects and lexicon in Russian news have evolved over the last three years. The purpose of this journey into topic modeling is to gain deeper insights into the shifts in societal and cultural narratives as reflected in the media. This project is ongoing, and I'll keep you updated with my findings as they unfold. This project has sparked a new avenue of research and discovery in the ever-evolving world of data science.

{::nomarkdown}
{% assign jupyter_path = "assets/jupyter/news-classification.ipynb" | relative_url %}
{% capture notebook_exists %}{% file_exists assets/jupyter/dostoevsky.ipynb %}{% endcapture %}
{% if notebook_exists == "true" %}
{% jupyter_notebook jupyter_path %}
{% else %}

<p>Sorry, the notebook you are looking for does not exist.</p>
{% endif %}
{:/nomarkdown}