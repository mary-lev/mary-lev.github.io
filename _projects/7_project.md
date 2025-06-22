---
layout: page
title: BertAlign API
description: Multilingual Sentence Alignment Service for DiScEPT Project
img: assets/img/discept.png
importance: 7
category: work
github: https://github.com/mary-lev/bertalign-api
---

**BertAlign API** is a FastAPI-based web service for multilingual sentence alignment developed as part of the **DiScEPT** (Digital Scholarly Editions Platform and aligned Translations) project at the Istituto Italiano di Studi Germanici. The service uses sentence-transformers (LaBSE model) to support both plain text and TEI XML document alignment, deployed on Google Cloud Run with Docker containerization.

## 🎯 DiScEPT Project Context

This service is a key component of the **DiScEPT** project, which aims to develop a sustainable digital environment for producing and publishing Digital Scholarly Editions (DSE). DiScEPT is designed to create multilingual scholarly editions by integrating digital publishing tools with services that can align various versions of texts or entire corpora across multiple languages.

### Project Coordination
- **Coordinator**: Hansmichael Hohenegger (IISG)
- **Partners**: Fabio Ciotti (Tor Vergata), Tiziana Mancinelli (IISG), Federico Boschetti (ILC), Angelo Mario Del Grosso (ILC)
- **Collaborating Institutions**: 
  - Istituto di Linguistica Computazionale "A. Zampolli" – CNR (ILC)
  - Istituto per il Lessico Intellettuale Europeo e Storia delle Idee – CNR (ILIESI)
  - Università Tor Vergata
  - Università della Tuscia

## 🚀 Key Features

- **Multilingual Support**: Align sentences across 25 languages including English, French, German, Russian, Chinese, and more
- **Semantic Alignment**: Uses LaBSE (Language-agnostic BERT Sentence Embeddings) for high-quality alignments
- **Flexible Alignment**: Support for 1-1, 1-many, many-1, and many-many alignment patterns
- **TEI XML Support**: Specialized endpoint for aligning TEI documents with standOff annotations
- **FastAPI Backend**: Auto-generated OpenAPI documentation and request validation
- **Cloud Ready**: Dockerized for easy deployment on Google Cloud Run
- **Fast Processing**: Optimized response times ranging from 0.2-3 seconds

## 🌍 Supported Languages

The service supports alignment across 25 languages: Catalan, Chinese, Czech, Danish, Dutch, English, Finnish, French, German, Greek, Hungarian, Icelandic, Italian, Lithuanian, Latvian, Norwegian, Polish, Portuguese, Romanian, Russian, Slovak, Slovenian, Spanish, Swedish, and Turkish.

## 🔧 Technical Implementation

### Core Technology Stack
- **FastAPI**: Modern Python web framework for building APIs
- **sentence-transformers**: LaBSE model for multilingual sentence embeddings
- **Docker**: Containerization for consistent deployment
- **Google Cloud Run**: Serverless deployment platform

### API Endpoints

#### 1. Basic Text Alignment
```bash
POST /align
```
Aligns plain text inputs between source and target languages with configurable similarity thresholds.

#### 2. TEI XML Document Alignment
```bash
POST /align/tei
```
Specialized endpoint for aligning TEI-encoded documents, preserving XML structure and generating standOff annotations.

### Example Response Format
```json
{
  "alignments": [
    {
      "source_sentences": ["Hello world."],
      "target_sentences": ["Bonjour le monde."],
      "alignment_score": 0.89,
      "source_indices": [0],
      "target_indices": [0]
    }
  ],
  "processing_time": 0.23,
  "total_source_sentences": 2,
  "total_target_sentences": 2
}
```

## 🎯 Use Cases

### Digital Humanities Applications
- **Multilingual Digital Editions**: Aligning source texts with their translations
- **Comparative Literature**: Analyzing translation patterns across languages
- **TEI Document Processing**: Creating aligned multilingual corpora with proper markup

### Translation Studies
- **Translation Quality Assessment**: Comparing alignment patterns between different translations
- **Corpus Linguistics**: Building parallel corpora for linguistic analysis
- **Educational Tools**: Supporting language learning through aligned text pairs

## 🏗️ Architecture

The service is built with a microservices architecture:

1. **API Layer**: FastAPI handles HTTP requests and response validation
2. **Processing Engine**: sentence-transformers provides semantic embeddings
3. **Alignment Algorithm**: Custom logic for flexible many-to-many alignments
4. **TEI Handler**: Specialized XML processing for digital humanities workflows

## 📈 Performance

- **Response Time**: 0.2-3 seconds depending on text length
- **Scalability**: Horizontal scaling via Google Cloud Run
- **Memory Efficient**: Optimized for cloud deployment constraints
- **Model Loading**: Cached LaBSE model for fast inference

## 🔗 Integration within DiScEPT

The BertAlign API serves as a core infrastructure component within the DiScEPT ecosystem, specifically designed to support:

### Digital Scholarly Editions
- **Multilingual text alignment** for scholarly editions across language barriers
- **TEI-compliant processing** maintaining XML structure and scholarly markup standards
- **Translation quality assessment** for scholarly publication workflows

### DiScEPT Platform Integration
- **Microservice architecture** allowing seamless integration with other DiScEPT tools
- **API-first design** enabling flexible integration with editorial workflows
- **Open access compatibility** supporting both research and commercial publishing pathways

### Research and Innovation Goals
- **Social innovation**: Supporting interaction between academic research and publishing industry
- **Educational applications**: Enabling use in secondary education and university teaching
- **International collaboration**: Facilitating multilingual scholarly communication

This service represents a crucial component in DiScEPT's vision of creating a sustainable platform that bridges research, education, and publishing, providing reliable sentence alignment capabilities that support the production of high-quality multilingual digital scholarly editions while maintaining open access principles for the digital humanities community.