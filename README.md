# Data Cleaning & Exploratory Data Analysis (Titanic Dataset)
This notebook dives deep into data preprocessing and exploratory analysis using the Titanic dataset to extract key insights and visualize patterns related to passenger survival.

### 🧼 1. Data Cleaning Process
We began by checking for missing values using df.isnull().sum(). This revealed:
- 177 missing entries in the Age column.
- 687 missing values in Cabin.
- 2 missing values in Embarked.
### Cleaning Steps:
- Dropped the Cabin column due to its high proportion of missing values (> 75%).
- Imputed missing Age values using the median, ensuring skewed distributions wouldn’t distort the data.
- Filled missing Embarked values with the mode ('S'), as it appeared most frequently.
- Verified that all missing data was handled, resulting in a clean dataset ready for analysis.

### 📊 2. Descriptive Statistics
Using df.describe(), we explored basic statistics:
- Average Age was ~29 years with a wide distribution (ranging from <1 to 80).
- Fare distribution showed a large range, indicating different socioeconomic backgrounds.
- Pclass had a mean of ~2.31, suggesting more passengers in the lower classes.

### 📈 3. Visual Explorations & Insights
#### 🔹 Age Distribution
- A histogram with KDE curve displayed the distribution of passengers by age.
- Most passengers were between 20 and 40 years old.
- The dataset includes infants and elderly passengers, showing a wide demographic.
#### 🔹 Survival Rate by Gender
- Bar plots revealed higher survival rates for females than males.
- Aligns with the “women and children first” rescue principle during the sinking.
#### 🔹 Correlation Heatmap
- Heatmap of numerical features like Age, Fare, SibSp, Parch, Pclass, and Survived.
- Fare and Pclass had a moderate correlation—higher fare often meant higher class.
- Survived showed mild negative correlation with Pclass (lower class, lower survival odds).
- Family-related features like SibSp and Parch showed weaker correlations but potential for feature engineering.

### 💡 Key Takeaways
- Passengers in higher classes (Pclass = 1) had better survival chances.
- Gender had a strong influence on survival: females were significantly more likely to survive.
- Fare and Age provided additional insight into socioeconomic and demographic effects on survival.
- Data was significantly improved through smart imputation and column pruning.

