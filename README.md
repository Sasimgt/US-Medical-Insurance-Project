# U.S. Medical Insurance Costs Analysis

## Project Overview

This project analyzes a U.S. medical insurance dataset (`insurance.csv`) to explore patterns and insights in healthcare costs. The goal is to investigate how features such as age, BMI, smoking status, gender, and region impact insurance charges. The project also includes basic predictive insights and visualizations.

The dataset is sourced from Kaggle and contains real-world information on insurance costs, enabling practical analysis using Python.

uhfyedfghi

---

## Dataset

The dataset contains the following columns:

- `age`: Age of the insured individual
- `sex`: Gender of the individual (`male` or `female`)
- `bmi`: Body Mass Index
- `children`: Number of children/dependents
- `smoker`: Smoking status (`yes` or `no`)
- `region`: Residential region in the U.S.
- `charges`: Annual medical insurance charges

Example of the first few records:

| age | sex    | bmi   | children | smoker | region    | charges  |
| --- | ------ | ----- | -------- | ------ | --------- | -------- |
| 19  | female | 27.9  | 0        | yes    | southwest | 16884.92 |
| 18  | male   | 33.77 | 1        | no     | southeast | 1725.55  |
| 28  | male   | 33.0  | 3        | no     | southeast | 4449.46  |

---

## Features Implemented

1. **Data Loading**
   - Used `csv` and `pandas` to read and inspect the dataset.
   - Converted numeric fields (`age`, `bmi`, `children`, `charges`) to appropriate data types.

2. **Exploratory Data Analysis (EDA)**
   - Calculated average age and average insurance charges.
   - Filtered data based on smoker status to compare costs.
   - Grouped data by categorical features (`sex`, `region`, `smoker`) for summary statistics.

3. **Custom Analysis Class**
   - `InsuranceAnalysis` class encapsulates methods to:
     - Calculate overall average insurance cost
     - Calculate average cost by smoker status
     - Count records by number of children

4. **Correlation Analysis**
   - Calculated numeric correlations with insurance charges to identify influential factors.

5. **Key Findings**
   - **Most influential feature**: Smoking status
   - **High cost profile**: Smoker, older age, higher BMI
   - **Low cost profile**: Non-smoker, younger age, lower BMI
   - Average charges for smokers are significantly higher than non-smokers
   - Correlation exists between `age`, `bmi`, and `charges`

6. **Visualizations**
   - Scatter plot of `age` vs `charges` to visualize trend in insurance costs by age.

---

## How to Run

1. Ensure Python 3.x is installed along with the following libraries:
   - `pandas`
   - `matplotlib`
2. Place `insurance.csv` in the same directory as the Python script or Jupyter Notebook.
3. Run the main script or notebook to:
   - Load and clean the dataset
   - Perform analyses
   - Generate plots

Example:

```bash
python insurance_analysis.py
# OR run the Jupyter Notebook
jupyter notebook

Sample Output:

Average insurance cost: $13270.42
Average cost by smoker status: (smokers: $32050.23, non-smokers: $8434.27)
Count by number of children: {0: 574, 1: 183, 2: 196, 3: 67, 4: 5}
Numeric correlation with charges:
{"charges": 1.0, "age": 0.299, "bmi": 0.198, "children": 0.067}
Visual plot: Scatter plot of age vs charges

Tools & Libraries:

Python 3.x: Core programming language
CSV Module: For reading CSV data
Pandas: Data analysis and manipulation
Matplotlib: Visualization
Object-Oriented Programming: Encapsulating analyses in a class

Project Insights:

Smoking status is the most influential factor for insurance charges.
Older individuals and those with higher BMI tend to have higher charges.
Non-smokers under 30 with healthy BMI typically have the lowest insurance costs.
Regional variations exist, with the southeast region showing higher average charges.
```
