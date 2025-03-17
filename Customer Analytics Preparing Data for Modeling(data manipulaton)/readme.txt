# Customer Analytics: Preparing Data for Modeling

## Overview

This project focuses on **data manipulation and optimization** to improve storage efficiency for predictive modeling. The dataset contains anonymized student information, and the goal is to prepare it for machine learning models that predict whether a student is looking for a new job.

## Dataset

The dataset, `customer_train.csv`, consists of the following columns:

| Column                   | Description                                                                      |
|------------------------- |--------------------------------------------------------------------------------- |
| `student_id`             | A unique ID for each student.                                                    |
| `city`                   | A code for the city the student lives in.                                        |
| `city_development_index` | A scaled development index for the city.                                         |
| `gender`                 | The student's gender.                                                            |
| `relevant_experience`    | An indicator of the student's work relevant experience.                          |
| `enrolled_university`    | The type of university course enrolled in (if any).                              |
| `education_level`        | The student's education level.                                                   |
| `major_discipline`       | The educational discipline of the student.                                       |
| `experience`             | The student's total work experience (in years).                                  |
| `company_size`           | The number of employees at the student's current employer.                       |
| `company_type`           | The type of company employing the student.                                       |
| `last_new_job`           | The number of years between the student's current and previous jobs.             |
| `training_hours`         | The number of hours of training completed.                                       |
| `job_change`             | Whether the student is looking for a new job (`1`) or not (`0`).                 |

## Data Processing Steps

### 1. **Data Loading & Exploration**
- The dataset is loaded using `pandas.read_csv()`.
- The first few rows are displayed to understand the structure.
- The distribution of values in each column is analyzed.

### 2. **Optimizing Data Types**
To reduce memory usage and improve performance:

- **Boolean Conversion:**
  - `relevant_experience` and `job_change` converted to `bool`.
  
- **Integer Optimization:**
  - `student_id` and `training_hours` converted to `int32`.
  
- **Float Optimization:**
  - `city_development_index` converted to `float16`.
  
- **Categorical Encoding:**
  - Nominal categorical columns converted to `category`.
  - Ordinal categorical columns reordered for proper comparison.

### 3. **Filtering Data**
The dataset is filtered to retain only students who:
- Have **10 or more years of experience**.
- Work at companies with **at least 1000 employees**.

### 4. **Memory Usage Comparison**
Memory usage is measured before and after transformation to assess improvements.

## Results
- The dataset is now **more memory-efficient**, enabling faster model training.
- Filtering ensures that only **relevant professionals** are included for recruitment predictions.
- Data types are optimized without loss of information.

## How to Run the Code
### Prerequisites
- Python 3.x
- Pandas (`pip install pandas`)

### Execution
```python
# Import necessary libraries
import pandas as pd

# Load the dataset
ds_jobs = pd.read_csv("customer_train.csv")

# Run the transformations (Refer to the provided script)
```

## Future Improvements
- Handling missing values before conversion.
- Additional feature engineering for better predictive modeling.
- Integration with a machine learning pipeline.


