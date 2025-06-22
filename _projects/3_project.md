---
layout: page
title: ALTO-to-TEI Converter
description: Document Processing Toolkit for eScriptorium Output
img: assets/img/publication_preview/publishing.webp
importance: 3
category: work
github: https://github.com/mary-lev/alto2tei
---

**ALTO-to-TEI Converter** is a comprehensive Python toolkit for converting eScriptorium ALTO XML files to TEI (Text Encoding Initiative) format, with full support for the Segmonto ontology for document structure classification. This tool bridges the gap between OCR/HTR output and structured scholarly markup.

## 🎯 Two Conversion Modes

### 📄 Page-Level Converter (alto2tei.py)
- **Individual file processing**: Converts ALTO files to corresponding TEI files
- **Structure preservation**: Maintains original document layout and line breaks
- **Small collections**: Ideal for analyzing individual pages or focused document sets

### 📚 Book-Level Converter (alto2teibook.py)
- **Complete book conversion**: Uses METS.xml for proper page ordering
- **Advanced text processing**: Cross-page paragraph merging with hyphenation handling
- **Unified output**: Generates single TEI document with optional facsimile zones
- **Machine-readable texts**: Perfect for computational analysis and digital editions

## 🏗️ Core Architecture Principles

### 1. Segmonto Ontology Compliance
The converter implements the **Segmonto ontology** - a controlled vocabulary for semantic annotation of historical document layouts:

- **Zone Classification**: Standardized zone types (`MainZone`, `MarginZone:note`, `GraphicZone`)
- **Hierarchical Names**: Colon-separated classification system for precise semantic markup
- **Semantic Consistency**: Maintains relationships between document regions across manuscripts

### 2. YAML-Driven Configuration
All transformation rules are externalized in YAML files, enabling:

- **Maintainability**: Updates without code changes
- **Flexibility**: Support for different document types and ontologies
- **Transparency**: Clear, readable transformation rules
- **Extensibility**: Simple addition of new zone and line types

### 3. TEI Best Practices
Generates standards-compliant TEI XML with:

- **Semantic Markup**: Meaningful element names reflecting content structure
- **Metadata Preservation**: Page numbers, image references, document hierarchy
- **Poetry Handling**: Proper `<lg>` and `<l>` element grouping
- **Footnote Management**: Structured annotation with automatic symbol recognition

## 🔧 Document Processing Pipeline

```
ALTO XML → Parse Tags → Classify Zones → Process Lines → Generate TEI
    ↓           ↓           ↓             ↓            ↓
eScriptorium  Segmonto   YAML Rules   Line Types   TEI XML
```

## 📊 Zone Classification System

| Zone Type | Segmonto Category | Processing | TEI Output |
|-----------|------------------|------------|------------|
| `MainZone` | Primary text content | Process all lines | `<p>`, `<lg>`, `<head>` |
| `MarginTextZone:note` | Footnote annotations | Extract as footnotes | `<note type="footnote">` |
| `MarginTextZone:outer` | Outer margin content | Process lines | `<p>` or specialized elements |
| `NumberingZone` | Page numbering | Extract page numbers | `<pb n="..." facs="...">` |
| `RunningTitleZone` | Running headers/titles | Process lines | `<p>` with context |
| `QuireMarksZone` | Quire markings | Process lines | `<p>` with context |

## 🔤 Line Type Processing

| Line Type | Purpose | TEI Element | Container |
|-----------|---------|-------------|-----------|
| `HeadingLine` | Section headings | `<head>` | Standalone |
| `CustomLine:paragraph_start` | Begin paragraph | `<p>` | Auto-closed |
| `CustomLine:verse` | Poetry lines | `<l>` | `<lg type="verse">` |
| `CustomLine:speaker` | Speaker names | `<speaker>` | Standalone |
| `CustomLine:catchword` | Page catchwords | `<fw type="catchword">` | Standalone |
| `CustomLine:signature` | Technical marks | `<fw type="signature">` | Standalone |
| `DefaultLine` | Regular text | Add to `<p>` | Current paragraph |

## ⚙️ Configuration Example

```yaml
block_types:
  MainZone:
    description: "Main text content blocks"
    process_lines: true
    skip_content: false
  
  "MarginTextZone:note":  # Segmonto hierarchical naming
    description: "Footnote blocks"
    process_lines: false
    extract_footnote: true
    tei_element: "note"
    attributes:
      type: "footnote"

line_types:
  "CustomLine:paragraph_start":
    description: "Beginning of paragraph"
    action: "start_paragraph"
    tei_element: "p"
    closes:
      - "poetry"
  
  "CustomLine:verse":
    description: "Poetry lines"
    tei_element: "l"
    container: "lg"
    container_attributes:
      type: "verse"
```

## 🚀 Usage Examples

### Page-Level Conversion
```bash
# Convert all ALTO files in 'alto' folder to 'tei' folder
python alto2tei.py

# Specify input and output folders
python alto2tei.py manuscripts output_tei

# Use custom configuration
python alto2tei.py --config custom_mapping.yaml
```

### Book-Level Conversion
```bash
# Convert entire book using METS.xml for page ordering
python alto2teibook.py alto_book/

# Enable cross-page paragraph merging with facsimile zones
python alto2teibook.py alto_book/ --merge-lines True --facsimile True

# Process without facsimile for pure text output
python alto2teibook.py alto_book/ --merge-lines True --facsimile False
```

## 📈 Real-World Performance

Based on processing historical manuscript collections:

### Block Types (6 actively used):
- **MainZone**: 100 files (102 instances) - Primary content
- **NumberingZone**: 89 files (91 instances) - Page numbers
- **GraphicZone**: 32 files (35 instances) - Graphics/decorations
- **MarginTextZone:outer**: 6 files (8 instances) - Margin content
- **RunningTitleZone**: 5 files (5 instances) - Running headers
- **MarginTextZone:note**: 4 files (4 instances) - Footnotes

### Line Types (6 actively used):
- **DefaultLine**: 100 files (2,775 instances) - Regular text
- **CustomLine:catchword**: 75 files (75 instances) - Page catchwords
- **CustomLine:verse**: 2 files (50 instances) - Poetry lines
- **CustomLine:paragraph_start**: 7 files (30 instances) - Paragraph starts
- **HeadingLine**: 3 files (13 instances) - Section headers
- **CustomLine:signature**: 7 files (7 instances) - Signatures

## 🌟 Key Features

- **Segmonto Ontology Integration**: Full support for hierarchical document structure classification
- **Flexible Configuration**: YAML-driven rules for different manuscript types
- **Cross-Page Processing**: Advanced paragraph merging across page boundaries
- **Hyphenation Handling**: Intelligent word reconstruction across page breaks
- **TEI Compliance**: Standards-compliant output with proper semantic markup
- **Extensible Architecture**: Easy addition of new document types and processing rules

This toolkit serves as essential infrastructure for digital humanities projects working with historical documents, providing a robust bridge between automated transcription tools and scholarly digital editions.