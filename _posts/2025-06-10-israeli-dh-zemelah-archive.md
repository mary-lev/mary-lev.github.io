---
layout: post
title: "Subject Indexing, Chatbot, and Computational Text Analysis in Zemelah.online: A Digital Archive of Soviet-Era Jewish Egodocuments"
date: 2025-06-10 09:00:00 +0000
categories: conferences digital-archives
description: Israeli International Conference on Digital Humanities and Social Sciences, Ra'anana, Israel
tags: digital-archives jewish-studies topic-modeling LDA sentiment-analysis chatbot
---

I will be presenting my collaborative work with Anastasia Glazanova (The Central Archives for the History of the Jewish People) on the Zemelah.online digital archive at the Israeli International Conference on Digital Humanities and Social Sciences at The Open University of Israel in Ra'anana.

## Project Overview

Zemelah.online is a digital archive preserving and analyzing Soviet-era Jewish egodocuments. Our collection encompasses diverse material types: handwritten manuscripts, typewritten documents, and small-edition publications produced for family and friends. The project reveals diverse experiences that challenge conventional scholarly frameworks — from stories of victimhood to achievement, from acculturation to religious observance.

## Evolution with AI Technology

Beginning in late 2020, the project has evolved significantly alongside rapid developments in Large Language Models since 2023:

### Initial Phase (2020-2023)
- Systematic document processing and qualitative text analysis
- Manual indexing of key entities (locations, persons, organizations)
- Thematic content indexing covering Jewish-specific and universal subjects

### AI Integration Phase (2023-present)
- **Markup editor** with pre-annotation using Claude and fixed tag sets
- **GPT-powered chatbot** enabling thematic queries and text fragment retrieval
- **Computational text analysis** using multiple methodological approaches

## Computational Analysis Methods

### Topic Modeling with LDA
Using Latent Dirichlet Allocation, we identified **8 distinct thematic clusters** in Soviet Jewish narratives:

- **Family/Childhood** (20.96% - most prevalent theme)
- **Personal Correspondence**
- **Soviet Jewish Experience** 
- **Military/Navy Life**
- **War/Holocaust narratives**
- **Professional/Medical narratives**

### Key Finding: Narrative Separation
A statistically significant **negative correlation (-0.32)** between Family/Childhood narratives and Soviet Jewish Experience topics reveals a compelling narrative strategy: authors tend to separate intimate family memories from institutional/political experiences, creating distinct storytelling modes that reflect complex navigation of private and public spheres in Soviet Jewish life.

### Technical Implementation
- **Russian-specific preprocessing**: Modified stopword lists for memoir narratives
- **pymorphy2** for Russian lemmatization
- **Optimal parameters**: 8 topics with document-topic prior (alpha) of 0.1 and topic-word prior (beta) of 0.01
- **Cross-validation** for empirical parameter determination

## Ongoing Research Directions

- **Sentiment analysis** to map emotional patterns across the corpus
- **Word embeddings (word2vec)** to visualize semantic networks
- **Multi-method correlation analysis** examining how themes relate to emotional expression

## Research Impact

This project demonstrates how "ordinary" Soviet Jews documented their experiences, providing computational insights into:
- Narrative strategies in historical ego-documents
- Private vs. public sphere navigation in Soviet Jewish life
- Emotional and semantic patterns in memoir writing
- Digital preservation of cultural heritage materials

## Resources

- **Code Repository**: [GitHub](https://github.com/mary-lev/topic_modeling)
- **Project Website**: Zemelah.online

**Conference dates**: June 10, 2025  
**Location**: Ra'anana, Israel  
**Event**: Israeli International Conference on Digital Humanities and Social Sciences 2025