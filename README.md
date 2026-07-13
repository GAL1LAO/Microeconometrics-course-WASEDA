# AI Tool Usage and Developer Salaries

**Course:** Microeconometrics, WASEDA University (Spring 2026)  
**Topic:** Causal inference using Propensity Score Matching

This project applies PSM methodology from the course to analyze Stack Overflow Developer Survey 2026 data.

## Research Question

Do developers who use AI tools daily earn more than non-users?

## Method

- **Treatment**: Daily AI tool users vs. non-users
- **Outcome**: Annual salary (log-transformed)
- **Approach**: Propensity Score Matching (nearest-neighbor with caliper)
- **Controls**: Work experience, years coding, age, dev type, country, org size, education, remote work, employment status

## Key Findings

- Naive OLS: -26% (biased by selection on experience/seniority)
- OLS with controls: +6.7%
- PSM estimate: +6.7%

Daily AI users earn ~7% more after matching on observables.

## Files

- `stackoverflow_psm_2025.ipynb` - Full analysis workflow
- `so_2025_cleaned.csv` - Cleaned dataset (N=11,760)
- `survey_results_public.csv` - Raw data (not included, download from Stack Overflow)

## Requirements

```
pandas
numpy
statsmodels
matplotlib
seaborn
scikit-learn
```

## Usage

1. Download the dataset from https://survey.stackoverflow.co/
2. Rename it to `survey_results_public.csv`
3. Place it in the project directory
4. Run `stackoverflow_psm_2025.ipynb`

