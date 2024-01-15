---
layout: page
title: LeggoManzoni
description: Quaranta commenti alla Quarantana
img: assets/img/13.jpg
importance: 1
category: work
related_publications: true
---

["Leggo Manzoni: Quaranta commenti alla Quarantana"](https://projects.dharc.unibo.it/leggomanzoni/) is an innovative project developed in [Bologna University](https://www.unibo.it/) and [the Digital Humanities advanced research center (DH.arc)](https://centri.unibo.it/dharc/en/research/projects-at-dh-arc) by Ersilia Russo, Beatrice Nava, Maria Levchenko and Giulia Menna, aiming to integrate digital technologies into everyday teaching practices. It provides educators with a tool for a more interactive approach to reading an Italian literature classic: Alessandro Manzoni's "The Betrothed" ("I promessi sposi"). 

This web application stands out for its interactive interface, presenting the text of the Quarantana edition of the novel, enriched with 40 critical comments and an illustrative apparatus. The project exemplifies a digital resource for teaching, born from the collaboration between schools and universities. It aims to impart students with cross-disciplinary skills through the use of digital resources. "Leggo Manzoni" not only facilitates an understanding of the novel through various critical perspectives but also encourages deeper analysis, allowing students to actively interact with the text and comments, thereby enhancing their analytical skills.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/13.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The main page of the web application.
</div>

From a more technical point of view, the project involves the storage and processing of two distinct types of texts, both in XML format: the full text of the novel and the commentaries. In the former, carefully structured into chapters, each term is associated with a unique identifier in order to facilitate analysis and structure references to that specific term. Each commentary, on the other hand, provides two distinct features: the first allows for the identification of specific portions of the novel, linking directly to the text via individual word identifiers; the second consists of the textual flow of the actual commentary, enriched by extra-textual markup.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/14.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The "Leggo" (Read) page of the application with text/comments alignment.
</div>

Correlation between the text of the novel and the comments is achieved through an advanced search algorithm, which assigns identifiers to comments based on the XML segmentation of the original text. This process allows the automatic creation of XML files associated with each comment, ensuring a direct link to the relevant sections of the novel. Finally, the project's web platform, thanks to the dynamic conversion of these XML files, allows users to select specific chapters and authors of the comments, facilitating intuitive interaction and smooth navigation. The standard XML format, in addition to supporting the core functionality of the site, ensures effective and easier management of content versions and updates, an aspect that should always be kept in mind when designing a new digital resource {% reference levchenko2024commentare %}.

{% raw %}

```xml
<note xml:id="BadConf_intro-image1" type="comm" target="quarantana/intro.xml#intro_10000">
    <figure rend="bold">
        <figDesc>[intestazione]</figDesc>
    </figure>: l’intestazione dell’introduzione, inizialmente non prevista
        (cfr. <bibl corresp="#letteremanzoni">
        <hi rend="italic">Lettere</hi>, to. 11 p. 161</bibl>), è quella
        del «genietto», che apre anche i <rs>capp. VI, XVII, XXIII e
        XXXVIII</rs>. «Il genietto regge due fiaccole. Una dà fiamme,
        l’altra dà fumo: a indicare accensione di passione, da una parte; e
        spegnimento e ritrosia, dall’altra. L’intestazione è da favola
        boschereccia. E prende a modello, dall'<bibl corresp="#aminta">
        <hi rend="italic">Aminta</hi> del Tasso</bibl>, la disarmonia
        antiidillica introdotta dal Satiro con il suo attentato violento
        contro la vergine Silvia. L’intestazione compendia la violenza che è
        il presupposto del romanzo. E che sulla narrazione tutta incombe come
        minaccia, e come memento antiidillico» (<bibl corresp="#nigrops">Nigro</bibl>).
</note>
```

{% endraw %}
