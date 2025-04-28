# Dataanlytics_Task5
Titanic Survival Analysis
Project Overview
This repository contains an analysis of the Titanic dataset, focusing on understanding the key factors influencing passenger survival rates. The Titanic dataset is a well-known dataset that includes information about passengers on the RMS Titanic, such as age, sex, class, and whether they survived or not.

The analysis uses Python, pandas, seaborn, and matplotlib for data manipulation and visualization. The key goal of this project is to uncover trends and patterns in the data that can provide insights into the likelihood of survival for different passenger groups.
Data Exploration
The dataset used in this analysis consists of the following columns:

PassengerId: Unique ID of each passenger.

Survived: Whether the passenger survived (1) or not (0).

Pclass: Passenger class (1st, 2nd, or 3rd).

Name: Name of the passenger.

Sex: Gender of the passenger.

Age: Age of the passenger.

SibSp: Number of siblings/spouses aboard the Titanic.

Parch: Number of parents/children aboard the Titanic.

Ticket: Ticket number.

Fare: Fare paid by the passenger.

Cabin: Cabin number.

Embarked: Port of embarkation (C = Cherbourg; Q = Queenstown; S = Southampton).

Data Preprocessing
Handling missing values for columns such as Age, Cabin, and Embarked.

Feature extraction (e.g., extracting Title from the Name column).

Data type conversions (e.g., Sex to categorical, Age to numeric).

Exploratory Data Analysis (EDA)
The following analyses were performed:

Survival Rate by Passenger Class:

Visualizing the survival rate across different passenger classes.

Survival Rate by Gender:

Understanding how gender influenced survival chances.

Age vs Survival:

Investigating survival rates across different age groups.

Family Size and Survival:

Analyzing how the number of family members aboard impacted survival chances.

Embarked and Survival:

Examining the relationship between port of embarkation and survival.

Fare and Survival:

Analyzing survival rates based on fare paid.

Visualizations
Pairplot: Visualizing relationships between numerical variables like Age, Fare, and Pclass.

Heatmap: Correlation heatmap for numerical features.

Barplot: Survival rates by Pclass, Sex, and Embarked.

Boxplot/Histograms: Distribution of Fare and Age.

Example Code for Visualizations
python
Copy
Edit
import seaborn as sns
import matplotlib.pyplot as plt

# Pairplot to visualize relationships between numerical variables
sns.pairplot(titanic, hue='Survived', vars=['Age', 'Fare', 'Pclass'])
plt.show()

# Heatmap to check correlations between features
sns.heatmap(titanic.corr(), annot=True, cmap='coolwarm')
plt.show()

# Barplot to visualize survival rate by Pclass
sns.barplot(x='Pclass', y='Survived', data=titanic)
plt.title('Survival Rate by Pclass')
plt.show()
Key Insights
Passenger Class (Pclass): Passengers in 1st class had a significantly higher chance of survival compared to those in 3rd class.

Gender: Female passengers had a higher survival rate compared to male passengers.

Age: Children had a higher chance of survival than adults.

Family Size: Passengers traveling alone had a lower survival rate compared to those traveling with family.

Embarked Port: Passengers who boarded in Cherbourg had the highest survival rate.

Fare: Higher fares were associated with a higher chance of survival, possibly reflecting higher-class passengers.

Technologies Used
Python: Programming language used for data analysis and visualization.

pandas: Data manipulation and analysis.

seaborn: Data visualization library for statistical plots.

matplotlib: Plotting library for creating static, animated, and interactive visualizations.

Jupyter Notebook: Used for interactive analysis and documentation.

