# University Ranking Analysis (2014-2024)

## Project Overview
This project provides an in-depth analysis of global university rankings over a decade, from 2014 to 2024. Using data from the Center for World University Rankings (CWUR), this analysis aims to identify patterns, trends, and key factors influencing the rankings of universities worldwide. Through this project, we explore the factors contributing to the stability or changes in rankings and investigate the growth of universities in developing countries.

## Data Source
- **Center for World University Rankings (CWUR)** dataset covering the years 2014 to 2024.
- The dataset includes metrics for each university:
  - **World Rank**: Global position of each university.
  - **National Rank**: Position within the university’s country.
  - **Research Rank**: Score based on research output and impact.
  - **Education Rank**: Score based on teaching quality.
  - **Employability Rank**: Score reflecting graduate employment rates.
  - **Faculty Rank**: Score based on faculty qualifications and achievements.
  - **Score**: An overall score metric was included but not used in this study due to inconsistencies over the years.

## Hypotheses
The project tests three main hypotheses:
1. **Research and employability ranks** are primary elements of global university rankings.
2. **Top university rankings** exhibit relative stability over time, with minimal changes in the highest ranks.
3. **Universities in developing countries** are showing an upward trend in global rankings, in contrast to those in developed countries.

## Data Cleaning
The CWUR data had several inconsistencies and missing values that required extensive data cleaning. Each year’s dataset presented unique challenges:
- **Missing Values**: Missing data was represented by `'-'` in some years, which was replaced with `NaN` to enable analysis.
- **Threshold Values**: For values over 200, the dataset used symbols like `'>200'` or `'200+'`, which needed conversion to numeric values such as `201`.
- **Data Types**: All rank values were initially in string format and were converted to numeric format for statistical analysis.
- **Score Exclusion**: The "Score" metric was excluded from the analysis due to significant variability across years. Scores ranged from a minimum of around 44 (2014-2017) to around 75 (2018-2024), making it unreliable for comparative analysis.

To handle these issues, each year’s dataset was cleaned individually in separate Jupyter Notebooks. After cleaning, all datasets were merged into a single comprehensive dataset for analysis.

## Methodology
1. **Exploratory Data Analysis (EDA)**: Used histograms, violin plots, and line graphs to understand the distribution of rankings and identify trends over time.
2. **Visualization**: Created spider plots, trend lines, and distribution graphs to illustrate:
   - Stability in top university rankings.
   - Regional growth trends, particularly among universities in developing countries.
   - Ranking shifts across different categories such as Research, Faculty, and Employability.
3. **Statistical Analysis**: Calculated correlations among ranking metrics (World Rank, Research Rank, Faculty Rank, etc.) to identify primary factors contributing to high global rankings.
4. **Hypothesis Testing**: Verified hypotheses through observed trends, statistical correlations, and comparative analysis.

## Key Findings
1. **Top University Stability**: The top 5 universities showed minimal ranking changes over the 10-year period, highlighting stability among elite institutions.
2. **Influence of Research and Faculty**: Research Rank and Faculty Rank emerged as the strongest predictors of World Rank, supporting the hypothesis that research and faculty quality are crucial in determining global rank.
3. **Growth in Developing Countries**: Developing countries, particularly China, Malaysia, and Iran, showed significant upward trends in rankings, reflecting increased investment in higher education.
4. **National Rank Impact**: The National Rank metric showed weak correlations with global ranking factors, indicating that a university’s standing within its country does not significantly influence its global position.

## Project Structure
The repository contains the following files:
- `University_ranking.ipynb`: The main analysis notebook, where the cleaned datasets are merged, analyzed, and visualized.
- **Data Cleaning Notebooks**: Separate Jupyter Notebooks for each year (2014-2024) where unique cleaning methods were applied based on specific issues in each dataset.
- `presentation.pptx`: The presentation summarizing key findings, trends, and future directions.
- `memory.pdf`: A detailed document describing the project methodology, challenges, insights, and data sources.

## Usage Instructions
1. **Clone the repository**:
   ```bash
   git clone [repository_url]
   ```
2. **Install required libraries**:
   Make sure you have the following Python libraries installed:
   ```bash
   pip install Numpy pandas matplotlib seaborn jupyter
   ```
3. **Run the data cleaning notebooks**:
   Execute each Jupyter Notebook for data cleaning from 2014 to 2024 to generate cleaned datasets for each year.
4. **Run the main analysis notebook**:
   Open and execute `University_ranking.ipynb` to perform the analysis on the merged dataset and visualize findings.

## Requirements
- Python 3.x
- Jupyter Notebook
- Libraries: Numpy and Pandas (for data manipulation), Matplotlib and Seaborn (for visualization)

## Future Directions
Based on the findings, further analysis could focus on:
1. **Comparing Multiple Ranking Systems**: Analyzing data from other ranking systems like THE, QS, and ARWU to identify differences and gain a comprehensive view of university rankings.
2. **Economic and Institutional Factors**: Investigating the impact of GDP, education spending, and institutional types (public vs. private) on university rankings.
3. **Influence of University Types**: Analyzing the performance of different university types (e.g., research-focused vs. teaching-focused) to understand their strengths in global rankings.
4. **Regional and Cultural Factors**: Examining how regional factors like language, historical context, and cultural priorities affect rankings, which could reveal biases or advantages.

## Limitations
- **Score Metric Exclusion**: The CWUR “Score” metric was excluded from the study due to inconsistencies across the years, limiting some aspects of cross-year comparisons.
- **Correlation vs. Causation**: While strong correlations were observed between certain metrics, establishing causation requires further in-depth analysis, particularly for external factors like funding or policy changes.
- **Single Ranking Source**: This study used data exclusively from CWUR, and conclusions might vary with data from other ranking bodies.

## Author
Arman Ghaziaskari Naeini  
November 2024
