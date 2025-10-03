# Smart-Watch_Data-Manipulation
hey there,
Here i have been successfull in Collecting, Cleaning and Maintaing the Data Qaulity of Smart Watches. The Data is been collected from smart watches, regarding the Health-Lifestyle of Consumers.
Project Overview
This project demonstrates end-to-end data cleaning of unstructured health data from smartwatches, addressing common data quality issues and creating meaningful health assessment metrics for user analytics.

🎯 Business Problem
Smartwatch health data often contains:

Missing values from sensor disconnections

Spelling inconsistencies in categorical data

Physiologically impossible measurements

Mixed data types and formatting errors

Goal: Clean the dataset to enable reliable health analytics and user segmentation.

📁 Dataset
Source: Simulated smartwatch health monitoring data

Records: 10,000 user entries

Features: 7 original columns + 2 engineered features

Size: ~547 KB

Original Features:
User ID - Unique user identifier

Heart Rate (BPM) - Beats per minute

Blood Oxygen Level (%) - Blood oxygen saturation

Step Count - Daily step count

Sleep Duration (hours) - Total sleep time

Activity Level - User activity categorization

Stress Level - Perceived stress score (1-10)

🛠️ Data Cleaning Pipeline
1. Data Quality Assessment
Identified 2-4% missing values across columns

Detected mixed data types (object/float64)

Found spelling variations in categorical data

2. Spelling Correction
python
# Standardized activity levels
"Seddentary" → "Sedentary"
"Highly_Active" → "Highly Active" 
"Actve" → "Active"
3. Missing Value Treatment
Used median imputation for numerical features

Type conversion for sleep duration and stress levels

Maintained 100% data completeness

4. Outlier Management
Applied medical reality checks

Capped physiologically impossible values

Preserved data integrity while ensuring realism

5. Data Standardization
Rounded numerical values to appropriate precision

Ensured consistent formatting

Prepared data for analysis and visualization

🚀 Feature Engineering
Stress Ratings
python
Conditions:
- Excellent: Stress Level 1-5
- Satisfactory: Stress Level 6-7  
- Bad: Stress Level 8-10
User Health Ratings
Multi-criteria health assessment based on:

Blood Oxygen (94-100%)

Heart Rate (50-80 BPM)

Step Count (4,000-15,000 steps)

Sleep Duration (6-8 hours)

Categories: Healthy, Mid-Healthy, Borderline, Unhealthy

📈 Results
Data Quality Improvements:
Null Values: 2-4% → 0%

Spelling Errors: 6 variations → 3 standardized categories

Data Types: Mixed → Consistent formatting

Outliers: Medically impossible values treated

User Health Distribution:
text
Borderline     38.1%
Mid-Healthy    32.8%
Unhealthy      19.8%
Healthy         9.3%
Stress Level Distribution:
text
Excellent      51.5%
Bad            28.5%
Satisfactory   20.1%
🛠️ Technical Stack
Python 3.8+

Pandas - Data manipulation and cleaning

NumPy - Numerical operations and conditional logic

Jupyter Notebook - Interactive development environment

📁 Project Structure
text
smartwatch-health-data/
│
├── smart_watches.ipynb          # Main analysis notebook
├── unclean_smartwatch_health_data.csv    # Raw data
├── cleaned_health_data.csv      # Cleaned output
├── README.md                    # Project documentation
└── requirements.txt             # Python dependencies
🚀 Getting Started
Prerequisites
bash
pip install pandas numpy jupyter
Usage
Clone the repository

Open smart_watches.ipynb in Jupyter

Run cells sequentially to reproduce analysis

Export cleaned data using the final cell

💡 Key Insights
Data Quality Matters: 20% of users had inconsistent activity level categorization

Medical Reality: 2.5% of records contained physiologically impossible values

Health Patterns: Only 9.3% of users met all four health criteria

Stress Impact: 51.5% of users reported excellent stress management

🎯 Business Applications
User Segmentation: Identify health behavior patterns

Product Development: Focus features on common health gaps

Marketing: Target users based on health profiles

Clinical Research: Clean dataset for health studies

📝 License
This project is open source and available under the MIT License.

👨‍💻 Author
Name : Zaviyar Ali 
Data Analyst 
LinkedIn | Portfolio

🔗 Connect
Feel free to connect with me for data science collaborations, health tech projects,Supply-Chain projects or just to chat about data!

⭐ If you found this project helpful, please give it a star!




