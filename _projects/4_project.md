---
layout: page
title: Historical OCR Analysis
description: LLM Performance Visualization Platform for 18th Century Russian Documents
img: assets/img/ocr.png
importance: 4
category: work
github: https://github.com/mary-lev/historical-ocr-analysis
---

**Historical OCR Analysis** is a comprehensive web application for analyzing and visualizing OCR model performance on 18th century Russian Civil Font documents. This tool provides detailed insights into how modern Large Language Models handle historical text recognition challenges.

## 🎯 Research Context

This application supports the research paper **"Why and Where LLMs Still Go Wrong: Gaps in Historical Linguistic Competence"** by providing an interactive platform to explore OCR errors and model performance across a dataset of 1,029 historical Russian documents from 1752-1801.

## 📊 Dataset Overview

### Scale and Scope
- **1,029 images** from **428 books** 
- **Time Period**: 1752-1801 (18th century Russian Civil Font)
- **Content Coverage**: 28,662 text lines, 933K characters
- **Subject Distribution**: Fiction, science, religion, history, geography, drama, education, poetry
- **Difficulty Range**: Easy to hard, with majority classified as medium difficulty

### Historical Significance
- **Peak Coverage**: 1780s-1790s representing golden age of Russian literature
- **Civil Font**: Transition period from Church Slavonic to modern Russian typography
- **Literary Genres**: Comprehensive coverage of 18th century Russian literary production

## 🔧 Key Features

### Analysis View (Dataset-Wide Insights)
- **Comprehensive Statistics**: Overview of 428 books and temporal distribution
- **Performance Metrics**: Model comparison with top-3 highlighting across evaluation metrics
- **Error Analysis**: Detailed breakdown of character substitutions and foreign character insertions
- **Subject Analysis**: Performance patterns across different literary genres

### Document View (Individual Analysis)
- **Interactive Image Viewer**: Zoom, pan, click-to-select with ALTO XML overlay
- **Line-by-Line Comparison**: Ground truth vs. model outputs
- **Smart Model Comparison**: 3-column layout with intelligent line matching
- **Real-Time Metrics**: Character preservation, case sensitivity, word accuracy

## 🤖 Models Evaluated

The platform analyzes performance across **12 state-of-the-art language models**:

### OpenAI Family
- GPT-4.1, GPT-4o, O3, O4-mini

### Google Family  
- Gemini 2.5 Pro, Gemini 2.5 Flash, Gemini 2.0 Flash

### Anthropic Family
- Claude 3.5 Sonnet, Claude 3.7 Sonnet

### Meta Family
- Llama 4 Maverick, Llama 4 Scout

### Alibaba
- Qwen 2.5 VL

## 🔍 Key Research Findings

### Historical Character Preservation
- **Gemini models** demonstrate superior preservation of historical Russian characters (ѣ, і, ъ)
- **Character-specific challenges**: Old orthography poses consistent difficulties across model families

### Performance Hierarchy
- **Latest generation models** show 5-15% accuracy improvements over earlier versions
- **Model family differences**: Distinct strengths in different aspects of historical text processing

### Error Pattern Analysis
- **Case sensitivity** remains a primary challenge across all models
- **Foreign character insertion** shows systematic patterns
- **Dataset complexity**: 880 medium difficulty and 146 hard documents provide substantial OCR challenges

## 💻 Technology Stack

### Frontend Architecture
- **React 18** with Vite for modern development experience
- **Tailwind CSS** for responsive and maintainable styling
- **Recharts** for interactive data visualization

### Image Processing
- **Canvas API** for ALTO XML overlays and annotations
- **Smart line matching algorithms** for accurate model comparison
- **Interactive zoom/pan** for detailed document inspection

### Deployment
- **GitHub Pages** with automated CI/CD pipeline
- **Optimized builds** for fast loading and performance

## 📈 Visualization Capabilities

### Statistical Dashboards
- **Performance metrics** with comparative analysis
- **Error distribution** across different document types
- **Temporal analysis** showing historical period coverage
- **Model comparison** with highlighting of top performers

### Interactive Document Analysis
- **ALTO XML overlay** showing recognition boundaries
- **Side-by-side comparison** of multiple model outputs
- **Character-level accuracy** visualization
- **Error highlighting** with detailed explanations

## 🎓 Academic Impact

This platform enables:

### Research Applications
- **Systematic evaluation** of LLM performance on historical texts
- **Error pattern analysis** for improving OCR accuracy
- **Dataset insights** for historical corpus development
- **Model comparison** for selecting optimal tools

### Educational Use
- **Interactive exploration** of OCR challenges
- **Visual demonstration** of technological limitations
- **Historical linguistics** teaching resource
- **Digital humanities** methodology showcase

## 🌟 Innovation Highlights

- **First comprehensive platform** for LLM OCR analysis on historical Russian texts
- **Interactive visualization** of complex model performance data
- **Real-time analysis** with immediate visual feedback
- **Scalable architecture** for additional historical corpora
- **Open source approach** enabling community contribution

This platform represents a significant contribution to digital humanities research by providing tools for systematic analysis of how modern AI handles historical text recognition challenges, with particular focus on preserving cultural and linguistic heritage through accurate digitization.