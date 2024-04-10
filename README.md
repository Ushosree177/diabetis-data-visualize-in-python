import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
data = pd.read_csv("diabetes.csv")
sns.pairplot(data, hue='Outcome', diag_kind='kde')
plt.show()
plt.figure(figsize=(10, 8))
sns.heatmap(data.corr(), annot=True, cmap='coolwarm', fmt=".2f", linewidths=0.5)
plt.title('Correlation Matrix Heatmap')
plt.show()
plt.figure(figsize=(8, 6))
sns.histplot(data['Age'], kde=True)
plt.title('Distribution of Age')
plt.xlabel('Age')
plt.ylabel('Count')
plt.show()
plt.figure(figsize=(8, 6))
sns.boxplot(x='Outcome', y='Glucose', data=data)
plt.title('Glucose Levels by Outcome')
plt.xlabel('Outcome')
plt.ylabel('Glucose')
plt.show()

