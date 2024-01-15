---
layout: page
title: SPbLitGuide 1999–2020
description: Social Network and GeoData Analysis
img: assets/img/15.jpg
importance: 2
category: work
---

<a href="https://spblitguide.streamlit.app/">The project SPbLitGuide 1999–2020</a> focuses on constructing and analyzing a dataset derived from <a href="https://isvoe.ru/spblitgid/">SPbLitGuide, a newsletter initiated by Daria Sukhovey</a> in May 1999. SPbLitGuide is notable for its comprehensive coverage of upcoming literary events in St. Petersburg, providing valuable insights into the city's cultural activities. The dataset encompasses 1,255 issues released up to October 2019, representing a significant aggregation of literary event data.

The project aims to:

- Systematically transform the corpus of newsletters into a structured, accessible dataset.
- Perform preliminary analyses as a foundation for deeper scholarly research into St. Petersburg's literary scene.

## Target Audience
- Academic Researchers: Ideal for scholars in literary studies, cultural analysis, and social sciences, this dataset lays the groundwork for longitudinal research in understanding the literary dynamics of St. Petersburg.
- Cultural Analysts and Historians: The preliminary analysis and structured data offer an entry point for exploring historical shifts in literary venues, themes, and community participation.

## Potential Applications
The cleaned and structured dataset offers valuable insights into the literary landscape of St. Petersburg, facilitating analyses such as trends in literary events, identification of key venues, and community engagement over two decades.

## Additional Data Representations
- Literary Life Map of St. Petersburg: Geographic locations for 862 venues were identified and mapped.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/15.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/17.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
     Literary places map of Saint Petersburg
</div>

- Graph of Persons: A graph depicting individuals who have participated in events over the 20-year span was compiled, using named entity recognition and neural network techniques.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/16.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/18.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
     Literary Network and Communities of Saint Petersburg
</div>

## Tools and Technologies Used
The following tools and technologies were instrumental in the development and analysis of the dataset:

- Data Extraction and Cleaning: Tools such as Python’s Pandas library for data manipulation, Regular Expressions (Regex) for pattern matching and text extraction, and BeautifulSoup for parsing and handling HTML content from the newsletters.
- Named Entity Recognition (NER): The DeepPavlov and Natasha libraries for Russian language processing, utilized for identifying and extracting specific entities like names, dates, and places from the text.
- Data Visualization and Mapping: Geographic Information System (GIS) tools for creating the Literary Life Map of St. Petersburg and network analysis tools for developing the Graph of Characters.
- Text Analysis: Focusing on Natural Language Processing (NLP) techniques and leveraging pre-built NLP models for text analytics.
- Database Management: PostgreSQL for database handling and management of the structured dataset.
- Data Publishing: The cleaned dataset is available on Zenodo in CSV format {% cite levchenko_2023_10086515 %}, and the data processing code <a href ="https://github.com/mary-lev/spblitguide">is hosted on GitHub</a>, ensuring accessibility and reproducibility of the research.

The SPbLitGuide Data Analysis Project employs text analytics and machine learning to create a comprehensive dataset, coupled with preliminary analysis. This serves as a crucial resource for those interested in a detailed study of St. Petersburg's literary landscape.

## References

{% reference levchenko_2023_10086515 %}

{% reference levchenko_inprogress_mapping %}