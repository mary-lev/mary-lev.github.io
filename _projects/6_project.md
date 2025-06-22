---
layout: page
title: EU Export Sanctions Analysis
description: The Missing Trade - Export-Import Data Discrepancies Under Sanctions Against Russia
img: assets/img/sanctions.png
importance: 6
category: work
github: https://github.com/mary-lev/eu-export-sanctions
---

**EU Export Sanctions Analysis** is a comprehensive data analysis platform examining export-import discrepancies under EU sanctions against Russia. This Streamlit-based application provides interactive tools for detecting anomalous trade patterns and potential sanctions circumvention through intermediary countries.

## 🎯 Research Context

Since Russia's invasion of Ukraine in February 2022, the European Union implemented extensive sanctions to suppress the Russian economy and limit its ability to finance aggressive actions. However, questions about sanctions effectiveness have emerged as Russia appears to circumvent measures through neighboring countries and trade rerouting.

This project provides empirical analysis to verify claims of growing intermediary trade and quantify the scale of potential sanctions circumvention using official statistical data.

## 💡 Research Inspiration

The project was inspired by **Robin Brooks'** observations highlighting unusual export growth from EU countries to regions such as Kyrgyzstan and Armenia. Brooks' insights raised critical questions about:

- **Significant growth patterns** in import/export activities with intermediary countries
- **Data alignment** between EU sources (Eurostat) and local statistical agencies
- **Statistical significance** of trade changes post-February 2022

## 🔍 Research Questions

### Primary Objectives
1. **Trend Analysis**: What changes occurred in EU imports/exports since February 2022, particularly through intermediary countries?
2. **Statistical Significance**: Are observed changes statistically significant and linked to sanctions timeline?
3. **Data Verification**: How well does EU data match with open data from Kyrgyzstan and Russia?
4. **Circumvention Detection**: What discrepancies exist that could indicate sanctions evasion?

### Analytical Goals
- **Historical Baseline Detection**: Establish pre-sanctions trade patterns
- **Anomaly Identification**: Detect unusual post-2022 trade behaviors
- **Trade Redirection Quantification**: Measure extent of trade rerouting
- **Intermediary Role Analysis**: Assess specific countries' involvement in trade redirection

## 📊 Key Findings

### Anomalous Export Growth (EU to Intermediary Countries)

| Country | Growth Rate | Geopolitical Context |
|---------|-------------|---------------------|
| **Kyrgyzstan** | **+344.8%** | EAEU member, close Russia ties |
| **Armenia** | **+148.9%** | EAEU member, regional hub |
| **Trinidad and Tobago** | **+122.6%** | Caribbean trade gateway |
| **Kazakhstan** | **+88.6%** | Major Central Asian economy |
| **Uzbekistan** | **+63.8%** | Regional economic partner |

### Statistical Significance
- **Timeline Correlation**: Trade surges align precisely with sanctions implementation
- **Magnitude Assessment**: Growth rates far exceed historical variations
- **Geopolitical Patterns**: Countries with strong Russia ties show highest increases
- **Economic Logic**: Trade volumes inconsistent with domestic consumption capacity

## 🛠️ Technical Implementation

### Streamlit Application Architecture
- **Interactive Dashboard**: Real-time data exploration and visualization
- **Multi-source Integration**: Eurostat, national statistical agencies
- **Statistical Analysis**: Trend detection, anomaly identification
- **Comparative Analytics**: Cross-country and temporal comparisons

### Data Sources
- **Eurostat**: Primary EU trade statistics
- **National Agencies**: Kyrgyzstan, Armenia, Russia statistical data
- **Time Series Analysis**: Pre- and post-sanctions comparison
- **Cross-validation**: Multiple source verification

### Key Features
- **Historical Baseline Analysis**: Pre-2022 trade pattern establishment
- **Anomaly Detection**: Statistical identification of unusual patterns
- **Interactive Visualization**: Dynamic charts and geographic mapping
- **Export Controls Tracking**: Specific commodity analysis

## 🔬 Analytical Methodology

### Statistical Approaches
- **Time Series Analysis**: Seasonal decomposition and trend extraction
- **Change Point Detection**: Identifying structural breaks in trade data
- **Comparative Analysis**: Year-over-year and baseline comparisons
- **Correlation Studies**: Sanctions timeline vs. trade pattern changes

### Data Validation
- **Cross-source Verification**: Multiple data source comparison
- **Consistency Checking**: Bilateral trade flow matching
- **Quality Assessment**: Data completeness and reliability evaluation
- **Outlier Analysis**: Extreme value identification and investigation

### Geographic Analysis
- **Trade Route Mapping**: Visualization of redirection patterns
- **Proximity Analysis**: Geographic and economic distance factors
- **Hub Identification**: Key intermediary country roles
- **Network Analysis**: Trade relationship complexity

## 📈 Interactive Dashboard Features

### Core Analytical Tools
- **Trade Flow Visualization**: Interactive charts showing export/import trends
- **Country Comparison**: Side-by-side analysis of multiple countries
- **Timeline Analysis**: Sanctions implementation impact visualization
- **Growth Rate Calculators**: Percentage change and statistical significance

### Data Exploration
- **Filtering Capabilities**: Time period, country, commodity selection
- **Drill-down Analysis**: Detailed investigation of specific patterns
- **Export Controls**: Focus on sanctioned goods and technologies
- **Correlation Matrices**: Relationship identification between variables

### Reporting Features
- **Automated Insights**: Key findings and trend summaries
- **Statistical Reports**: Significance testing and confidence intervals
- **Comparative Dashboards**: Multi-country performance analysis
- **Data Export**: Results and visualizations for further analysis

## 🌍 Geopolitical Implications

### Sanctions Effectiveness
- **Circumvention Evidence**: Statistical indicators of trade rerouting
- **Economic Impact Assessment**: Actual vs. intended sanctions effects
- **Policy Recommendations**: Data-driven insights for sanctions improvement
- **Monitoring Framework**: Ongoing surveillance methodology

### Regional Trade Dynamics
- **EAEU Integration**: Eurasian Economic Union role in trade redirection
- **Central Asian Hub**: Regional countries as intermediary bridges
- **Supply Chain Adaptation**: Russian economy's resilience mechanisms
- **Economic Geography**: Changing trade route preferences

## 🎓 Academic and Policy Impact

### Research Contributions
- **Empirical Evidence**: Quantitative analysis of sanctions circumvention
- **Methodological Innovation**: Multi-source data integration approaches
- **Policy Analysis**: Evidence-based sanctions effectiveness assessment
- **Economic Geography**: Trade redirection pattern documentation

### Practical Applications
- **Policy Making**: Informed sanctions design and implementation
- **Compliance Monitoring**: Automated detection of suspicious patterns
- **Economic Analysis**: Trade relationship evolution tracking
- **Academic Research**: Sanctions effectiveness literature contribution

## 💻 Technical Stack

### Data Processing
- **Python**: Core analytical programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Statistical computing and numerical analysis
- **Streamlit**: Interactive web application framework

### Visualization
- **Plotly**: Interactive charts and geographic mapping
- **Matplotlib/Seaborn**: Statistical visualization
- **Folium**: Geographic mapping and spatial analysis
- **Altair**: Declarative statistical visualization

### Deployment
- **Streamlit Cloud**: Web application hosting
- **GitHub Integration**: Version control and automated deployment
- **Data Pipeline**: Automated data updates and processing
- **Performance Optimization**: Efficient large dataset handling

## 🚀 Getting Started

### Installation Process
```bash
# Clone repository
git clone https://github.com/mary-lev/eu-export-sanctions.git

# Create virtual environment
python -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Launch application
streamlit run Home.py
```

### Application Access
- **Local Development**: http://localhost:8501
- **Web Interface**: Automatic browser launch
- **Interactive Features**: Real-time data exploration
- **Export Capabilities**: Download results and visualizations

## 📚 Academic Citation

```bibtex
@software{lev2024sanctions,
  author = {Maria Levchenko},
  title = {The Missing Trade: Export-Import Data Discrepancies Under Sanctions Against Russia},
  year = {2024},
  url = {https://github.com/mary-lev/eu-export-sanctions},
  note = {Streamlit application for sanctions circumvention analysis}
}
```

## 🌟 Innovation Highlights

- **First comprehensive platform** for systematic EU sanctions circumvention analysis
- **Multi-source data integration** providing robust verification methodology
- **Interactive analytics** enabling real-time exploration of trade anomalies
- **Statistical rigor** with significance testing and confidence intervals
- **Policy relevance** providing actionable insights for sanctions improvement
- **Open source approach** enabling reproducible research and community contribution

This project makes a significant contribution to economic sanctions research by providing empirical tools for detecting and quantifying trade redirection patterns, with particular focus on EU-Russia sanctions effectiveness and intermediary country roles in circumvention strategies.

## 🙏 Acknowledgments

- **Robin Brooks**: Initial inspiration through insightful trade pattern observations
- **Data Sources**: Eurostat, National statistical agencies of Kyrgyzstan, Armenia, and Russia
- **License**: Creative Commons Attribution 4.0 International License