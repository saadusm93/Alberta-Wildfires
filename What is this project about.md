# Alberta-Wildfires
This is a combination of an exploratory data analysis and machine learning classification model of the historical dataset of wildfire occurences in Alberta.

The study attempts to answer the questions of Why, Where, and When wildfires occur across Alberta using historical datasets.

## Step 1: Data wrangling and cleaning
- Clean data of missing and null values across various columns
- Find and replace incorrect values in columns like dates
- Remove some unnecessary columns

## Step 2: Feature engineering
- Engineer new columns like fire duration using existing columns
- Scale features
- Fix dtypes on columns and extract new columns from datetime

## Step 3: Address outliers and anomalies
- Create function to find quartile ranges
- Find and replace outliers in columns like fire duration and fire size

## Step 4: Run EDA
- Compare correlations between columns to find relationships
- Check distribution type for features (normal, skewed)
- Utilize scatter plots to find relationships between fire size and and temperature and other weather related features
- Explore data via bar charts and histograms

## Step 5.1: Export DataFrame to Power BI
- Import and reaffirm data integrity on BI
- Design normalized data model
- Create DAX functions and measures for further analysis
- Design multiple dahsboards to attempt to answer objective questions

## Step 5.2: Encode features and run Random Forest Classification model to find the general causes of fires that were 'under investigation, unclassified, NaN':
- Select relevant features and identify target variable (general_cause)
- Encode labeled features as numbers
- Split data into 2 dataframes: One with causes classified, another without.
- Fit train and test data to model
- Tune parameters and run iterations
- Check model accuracy using classification report (Scikit-learn)
- Run same model on second DataFrame to fill unclassified values
