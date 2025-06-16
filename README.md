# US Traffic Accident Analysis

This project analyzes traffic accident data to identify patterns related to:
- Road conditions
- Weather
- Time of day

## Dataset
[Kaggle US Accident EDA](https://www.kaggle.com/code/harshalbhamare/us-accident-eda)

## Structure
- `data/` - Dataset files.
- `notebooks/` - Jupyter notebooks for EDA.
- `images/` - Task reference images.
- `output/` - Final output files.


# CODE:
# US Traffic Accident EDA
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load dataset
df = pd.read_csv('data/US_Accidents_Dec21_updated.csv')  # replace with actual filename

# Show basic info
print(df.info())
print(df.describe())

# Example plot - Accidents by Weather Condition
plt.figure(figsize=(12, 6))
sns.countplot(data=df, x='Weather_Condition', order=df['Weather_Condition'].value_counts().iloc[:10].index)
plt.xticks(rotation=45)
plt.title("Top 10 Weather Conditions in US Accidents")
plt.tight_layout()
plt.show()
