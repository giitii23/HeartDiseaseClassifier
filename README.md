# HeartDiseaseClassifier
Knowledge Discovery in Databases (KDD) project for heart disease classification using Machine Learning.
# Heart Disease Classification via Knowledge Discovery in Databases (KDD)
![Electrocardiogram Animation](assets/ecg.gif)

## Project Overview
This repository contains a structured data science project that applies the complete Knowledge Discovery in Databases (KDD) process to clinical data. The objective is to develop a predictive model capable of classifying patients into healthy or high-risk heart disease categories, serving as a framework for a Clinical Decision Support System (DSS).

The system implements a regularized Random Forest Classifier to extract patterns from non-invasive clinical measurements (such as age, blood pressure, cholesterol, and maximum heart rate), prioritizing diagnostic reliability and interpretability.

## The KDD Process Workflow
The project architecture strictly follows the standard KDD methodology:

1. **Data Selection:** Targeting and extracting the required clinical attributes from the UCI Heart Disease repository to define the baseline dataset.
2. **Data Pre-processing:** Assessment of data quality, checking for missing values, and conducting exploratory distribution analysis to remove anomalies.
3. **Data Transformation:** Data preparation via One-Hot Encoding for nominal categorical variables, dataset partitioning into training (80%) and testing (20%) subsets, and Z-score standardization for continuous variables.
4. **Data Mining:** Algorithmic extraction of clinical patterns using an ensemble Random Forest Classifier with controlled tree depth to mitigate overfitting.
5. **Evaluation and Interpretation:** Performance evaluation prioritizing the Recall (Sensitivity) metric over global accuracy to minimize critical False Negatives. Interpretation is conducted via Feature Importance ranking.
6. **Use of Discovered Knowledge:** Operational deployment simulated through a script that includes a Data Validation Layer to intercept out-of-distribution inputs before executing the predictive pipeline.

## Repository Structure
* `main.ipynb`: The primary Jupyter Notebook containing the segmented KDD phases and executable Python code.
* `heart.csv`: The targeted clinical dataset containing patient records.
* `requirements.txt`: The list of required Python libraries and dependencies.
* `README.md`: Project documentation.

## Dataset Attributes
The model processes the following features extracted from the clinical dataset:
* `age`: Patient age in years.
* `sex`: Biological sex (1 = male; 0 = female).
* `cp`: Chest pain type (0 to 3 representing typical angina, atypical angina, non-anginal pain, or asymptomatic).
* `trestbps`: Resting blood pressure in mm Hg upon hospital admission.
* `chol`: Serum cholesterol in mg/dl.
* `fbs`: Fasting blood sugar > 120 mg/dl (1 = true; 0 = false).
* `restecg`: Resting electrocardiographic results (0 = normal, 1 = ST-T wave abnormality, 2 = left ventricular hypertrophy).
* `thalach`: Maximum heart rate achieved during exercise stress testing.
* `exang`: Exercise-induced angina (1 = yes; 0 = no).
* `oldpeak`: ST depression induced by exercise relative to rest.
* `slope`: The slope of the peak exercise ST segment.
* `ca`: Number of major vessels (0-3) colored by fluoroscopy.
* `thal`: Thallium stress test results (representing normal, fixed defect, or reversible defect conditions).
* `target`: Diagnosis of heart disease status (0 = healthy; 1 = presence of heart disease).

## Installation and Setup

### Prerequisites
Ensure you have Python 3.8 or a later version installed on your operating system.

### Environment Configuration
To prevent dependency conflicts, it is recommended to deploy the project within an isolated virtual environment.

1. Clone or download this repository to your local machine.
2. Open the terminal or command prompt inside the project directory and execute:

```bash
# Create a virtual environment named 'kdd_env'
python -m venv kdd_env

# Activate the environment (Windows Command Prompt)
kdd_env\Scripts\activate

# Activate the environment (macOS / Linux)
source kdd_env/bin/activate
