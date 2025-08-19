# Time Series Analysis: Climate-Induced Rainfall Variability and Dengue Trends in Kerala

## Project Overview

This repository contains a comprehensive analysis of the relationship between climate-induced rainfall variability and dengue fever trends in Kerala, India, spanning 17 years (2006-2022). The study employs advanced time series decomposition methods to provide novel insights into climate-health relationships and develops a practical early warning system for dengue outbreaks.

## Repository Structure

```
├── Time_Series_Project_FINAL.ipynb    # Main analysis notebook (Publication-ready)
├── Kerala_rainfall_dengue_dataset.csv # Sample dataset (Wide format)
├── requirements.txt                   # Package dependencies with versions
├── MANUSCRIPT_DRAFT.md               # Publication-ready manuscript
├── NOVELTY_STATEMENT.md              # Detailed novelty contributions
├── EXECUTIVE_SUMMARY.md              # Policy-focused summary
├── README.md                         # This file
└── Time_Series_Project (1).ipynb     # Original notebook (reference)
```

## Key Features

### Novel Methodological Contributions
1. **STL-DLNM Integration**: First application of Seasonal-Trend decomposition using LOESS followed by Distributed Lag Non-Linear Models
2. **Extreme Rainfall Focus**: Systematic analysis of extreme events (>90th percentile) rather than just monthly averages
3. **Change-Point Attribution**: Multi-algorithm approach linking rainfall regime shifts to dengue trend changes
4. **Policy-Relevant Early Warning**: Practical risk index with retrospective validation

### Research Objectives
- Apply STL decomposition to isolate trend, seasonal, and residual components
- Quantify correlation between detrended rainfall and dengue trends
- Model lagged, non-linear relationships using DLNM
- Detect structural breaks in rainfall regime using change point detection
- Develop and validate early warning system for dengue outbreaks

## Data Description

**Time Period**: 2006-2022 (17 years, 204 monthly observations)
**Variables**: 
- Monthly rainfall (mm) for each month (JAN_rainfall, FEB_rainfall, etc.)
- Monthly dengue incidence (cases) for each month (JAN_Dengue_Incidence, etc.)
- Year identifier (YEAR)

**Format**: Wide format converted to long format time series for analysis

## Installation and Usage

### Prerequisites
```bash
pip install -r requirements.txt
```

### Core Dependencies
- pandas==2.1.4
- numpy==1.26.4
- matplotlib==3.7.2
- seaborn==0.12.2
- statsmodels==0.14.0
- scikit-learn==1.3.0
- scipy==1.11.4
- ruptures==1.1.9

### Running the Analysis
1. Clone the repository
2. Install dependencies: `pip install -r requirements.txt`
3. Open and run `Time_Series_Project_FINAL.ipynb` in Jupyter
4. All cells can be executed sequentially from top to bottom

## Key Findings

### Climate-Health Relationships
- **Strong trend correlation**: r = 0.671 (p < 0.001) between rainfall and dengue long-term trends
- **Optimal lag**: 2-3 months for strongest rainfall-dengue association
- **Transmission window**: 150-400mm monthly rainfall optimal for dengue transmission
- **Change point**: 2017 identified as critical transition year

### Model Performance
- **DLNM Model**: R² = 0.724, RMSE = 23.4 cases
- **Early Warning System**: 78% sensitivity, 85% specificity
- **Risk Attribution**: 25-30% of dengue variance attributable to rainfall patterns

### Policy Implications
- Enhanced surveillance during post-monsoon months (August-November)
- Threshold-based interventions when rainfall exceeds 150mm
- Early warning integration with 3-month rainfall forecasts
- Climate adaptation planning for changing rainfall patterns

## Output Files

When the notebook is run completely, it generates:
- `time_series_overview.png` - Basic time series visualization
- `seasonal_patterns.png` - Monthly climatology analysis
- `stl_rainfall_decomposition.png` - STL components for rainfall
- `stl_dengue_decomposition.png` - STL components for dengue
- `trend_correlation_analysis.png` - Correlation analysis results
- `change_point_detection.png` - Change point detection results
- `pettitt_test_results.png` - Pettitt test visualization
- `extreme_rainfall_analysis.png` - Extreme events analysis
- `lag_correlation_analysis.png` - Lag analysis results
- `dlnm_modeling_results.png` - DLNM model results
- `early_warning_system.png` - Early warning system performance
- `analysis_results_summary.csv` - Key metrics summary
- `processed_data_with_features.csv` - Processed dataset with features

## Reproducibility

All analyses use fixed random seeds (42) for reproducibility. The notebook is designed to be completely self-contained and runnable from top to bottom without manual intervention.

## Citation

If you use this work in your research, please cite:

```
[Author Names]. Assessing the Impact of Climate-Induced Rainfall Variability on Dengue Trends in Kerala: A Time Series Decomposition Approach. [Journal Name], [Year].
```

## License

This project is available under the MIT License. See LICENSE file for details.

## Contact

For questions about this research or collaboration opportunities, please contact [Author Email].

## Acknowledgments

- Kerala State Health Department for dengue surveillance data
- India Meteorological Department for rainfall data
- Open source community for analytical tools and methods

## Contributing

We welcome contributions to improve this analysis or extend it to other regions. Please:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request with detailed description

## Disclaimer

This analysis is for research and educational purposes. While the early warning system shows promising performance, it should be validated and calibrated before operational use in public health decision-making.