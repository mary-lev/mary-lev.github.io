---
layout: page
title: NER Models Evaluation
description: Russian Cultural Texts Analysis with Traditional and LLM-based Approaches
img: assets/img/ner_performance_heatmap.png
importance: 5
category: work
github: https://github.com/mary-lev/NER
---

**NER Models Evaluation** provides comprehensive evaluation and modular implementation of Named Entity Recognition (NER) models for Russian cultural texts, comparing traditional NER approaches with modern LLM-based methods on a substantial cultural dataset spanning two decades.

## 🎯 Research Context

This project addresses the critical need for effective Named Entity Recognition in Russian cultural domain texts, providing both live model inference capabilities and comprehensive evaluation frameworks. The research compares traditional machine learning approaches with state-of-the-art Large Language Models on real-world cultural event data.

## 📊 Dataset: SPbLitGuide Cultural Events

### Dataset Overview
- **15,012 total records** from Saint Petersburg Literary Guide project
- **Time Period**: 1999-2019 (two decades of cultural events)
- **Content**: Electronic newsletters detailing upcoming cultural events
- **Geographic Scope**: Saint Petersburg cultural landscape
- **Annotations**: 1,000 manually annotated records using Doccano framework

### Data Structure
- **Event ID**: Unique identifier for each cultural event
- **Event Description**: Detailed text describing the cultural activity
- **Date/Time**: Temporal information for event scheduling
- **Location**: Venue names and cultural institutions
- **Address**: Geographic location data
- **Coordinates**: Latitude/longitude for spatial analysis

### Cultural Significance
- **Literary Landscape**: Comprehensive coverage of St. Petersburg's literary scene
- **Genre Diversity**: Fiction, poetry, drama, academic events, exhibitions
- **Historical Evolution**: Two-decade perspective on cultural trends
- **Person Recognition**: Focus on identifying cultural figures, authors, performers

## 🔧 Technical Architecture

### 🚀 Quick Start Options

#### Interactive Development
- **📔 NER_Models_Demo.ipynb**: Interactive demonstration of modular NER system
- **📊 Evaluation_Analysis.ipynb**: Comprehensive model comparison and analysis

#### Production Deployment
- **🐍 model_comparison.py**: Command-line evaluation script for batch processing

### 🤖 Modular NER System (`utils/ner_models/`)

#### Traditional NER Models
- **spaCy Russian Models**: `ru_core_news_sm`, `ru_spacy_ru_updated`
- **DeepPavlov BERT**: `ner_collection3_bert`, `ner_ontonotes_bert_mult`
- **RoBERTa Large**: Advanced transformer-based recognition
- **Custom Russian Models**: Domain-specific trained models

#### LLM-based Approaches
- **OpenAI Family**: GPT-4.1, GPT-4o, GPT-4, GPT-3.5-turbo
- **Mistral**: European multilingual capabilities
- **JSON-structured Output**: Structured entity extraction
- **API Integration**: Seamless cloud model access

## 📈 Performance Analysis

### Comprehensive Model Evaluation

| Model | Precision | Recall | F1 Score | Use Case |
|-------|-----------|--------|----------|----------|
| **gpt-4.1-2025-04-14** | 0.94 | 0.93 | **0.94** | Best overall performance |
| **gpt4o (json)** | 0.96 | 0.90 | 0.93 | Structured output |
| **gpt-4o** | 0.96 | 0.86 | 0.91 | Balanced accuracy |
| **roberta_large** | 0.92 | 0.77 | 0.84 | Traditional ML efficiency |
| **spacy** | 0.84 | 0.81 | 0.83 | Production reliability |
| **mult_model** | 0.94 | 0.71 | 0.81 | High precision |
| **gpt-3.5** | 0.95 | 0.71 | 0.81 | Cost-effective option |
| **rus_ner_model** | 0.96 | 0.65 | 0.78 | Russian-specific |

### Key Performance Insights

#### LLM Advantages
- **GPT-4.1** achieved highest F1 score (0.94) with balanced precision-recall
- **JSON-structured outputs** improved entity extraction consistency
- **Latest generation models** show 10-15% improvement over traditional approaches

#### Traditional Model Strengths
- **RoBERTa Large** provides best traditional performance (0.84 F1)
- **spaCy models** offer reliable production-ready performance
- **Lower computational cost** for high-volume processing

#### Tokenization Impact
- **Model-specific tokenizers** create different token counts for same samples
- **Tokenization differences** significantly affect performance comparison
- **Standardized evaluation** accounts for tokenization variations

## 🔬 Statistical Validation

### Significance Testing (GPT-4o vs GPT-4.1)
- **Precision**: Mean difference = -0.0180, 95% CI = [-0.0272, -0.0099], p < 0.001
- **Recall**: Mean difference = 0.0702, 95% CI = [0.0438, 0.0971], p < 0.001
- **F1 Score**: Mean difference = 0.0289, 95% CI = [0.0138, 0.0440], p < 0.001

### Performance Visualization
- **Model Performance Heatmap**: Visual comparison across all metrics
- **Precision-Recall Curves**: Detailed performance analysis
- **Statistical Confidence Intervals**: Robust evaluation methodology

## 💻 Implementation Features

### Unified Model Interface
- **Consistent API**: Single interface for all model types
- **Error Handling**: Robust exception management
- **Performance Monitoring**: Real-time evaluation metrics
- **Batch Processing**: Efficient large-scale analysis

### Evaluation Framework
- **Cross-validation**: Statistically sound evaluation
- **Metric Standardization**: Comparable results across models
- **Confidence Intervals**: Statistical significance testing
- **Performance Profiling**: Speed and accuracy trade-offs

### Production Readiness
- **Command-line Interface**: Easy integration into workflows
- **Configuration Management**: Flexible model selection
- **API Integration**: Cloud model support
- **Scalable Architecture**: Handle large document collections

## 🎓 Research Applications

### Digital Humanities Research
- **Cultural Network Analysis**: Identify key figures in cultural events
- **Historical Trend Analysis**: Track cultural figure prominence over time
- **Geographic Cultural Mapping**: Spatial analysis of cultural activities
- **Literary Community Studies**: Social network extraction from event data

### NLP Methodology
- **Model Comparison**: Systematic evaluation of NER approaches
- **Domain Adaptation**: Cultural text-specific model training
- **Multilingual Analysis**: Russian language processing challenges
- **Evaluation Standardization**: Reproducible assessment methods

### Practical Applications
- **Cultural Event Processing**: Automated entity extraction from announcements
- **Archive Digitization**: Historical document processing
- **Information Retrieval**: Enhanced search capabilities
- **Knowledge Graph Construction**: Automated relationship extraction

## 📚 Academic Citation

```bibtex
@misc{lev2024ner,
  author = {Maria Levchenko},
  title = {Evaluation of Named Entity Recognition Models for Russian News Texts in the Cultural Domain},
  year = {2024},
  howpublished = {\url{https://github.com/mary-lev/NER}},
  note = {Accessed: 2024-06-01}
}
```

## 🌟 Innovation Highlights

- **First comprehensive comparison** of traditional vs. LLM-based NER on Russian cultural texts
- **Two-decade cultural dataset** providing substantial evaluation corpus
- **Modular architecture** enabling easy model integration and comparison
- **Statistical significance testing** ensuring robust evaluation methodology
- **Production-ready implementation** with unified interface for all model types
- **Cultural domain specialization** addressing specific challenges in humanities text processing

This project significantly contributes to digital humanities methodology by providing tools and evaluation frameworks for systematic analysis of Named Entity Recognition performance on cultural texts, with particular emphasis on Russian language processing and cultural event analysis.