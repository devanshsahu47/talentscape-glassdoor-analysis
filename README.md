# TalentScape: Data-Driven Insights on Glassdoor Job Postings

## Problem Statement & Business Objective
Companies often struggle to set competitive compensation and target the best recruitment regions. This project addresses that challenge by leveraging a comprehensive Glassdoor Jobs dataset to extract actionable insights. Our objectives are to:
- **Benchmark Salaries:** Understand trends across industries and roles.
- **Optimize Recruitment:** Identify high-potential geographic and industry segments.
- **Enhance Employer Branding:** Improve employee satisfaction by analyzing company ratings.
- **Optimize Resource Allocation:** Inform HR strategies to maximize ROI in talent acquisition.

## Approach & Methodology
The project follows an end-to-end data analysis process:
1. **Data Exploration:**  
   We begin by exploring the dataset with commands like `df.info()`, `df.head()`, and `df.describe(include='all')` to assess its structure and quality.
2. **Data Wrangling & Preprocessing:**  
   - Duplicate records are removed, and missing values are handled.
   - The "Salary Estimate" field is cleaned by stripping extraneous text and parsing it into numeric minimum, maximum, and average salary values.
   - The "Company Name" is sanitized to remove appended ratings.
   - The "Location" field is parsed to extract state information, and the "Size" column is converted into an ordered categorical variable.
   - Derived columns (e.g., `sdesc_len` for job description length and a default `num_comp` if missing) are created to ensure comprehensive analysis.
3. **Visualization & Analysis:**  
   Using 20 diverse visualizations (following the Univariate, Bivariate, and Multivariate framework), we uncover key patterns such as:
   - The overall distribution of salaries.
   - Relationships between company ratings and salary levels.
   - Geographic trends in job postings.
   - Interactions among variables via pair plots, correlation heatmaps, and bubble charts.
These insights directly inform strategies for competitive compensation, targeted recruitment, and improved employer branding.

## Dependencies
This project requires the following Python packages:
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- jupyter

Install all dependencies using:
```bash
pip install -r requirements.txt
