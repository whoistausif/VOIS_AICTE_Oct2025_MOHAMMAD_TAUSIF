

# **Project Report: Detailed Analysis of the Airbnb Hotel Booking**

**Author:** Mohmmad Tausif  

**Internship ID:** INTERNSHIP\_17546440516895be537820f

-----

### **1. Project Introduction & Setup**

#### **Description**

This project provides a comprehensive analysis of the Airbnb open dataset for New York City. The goal is to uncover insights into pricing, availability, and popular neighborhoods. We begin by importing the necessary Python libraries for data manipulation (`pandas`, `numpy`) and visualization (`matplotlib`, `seaborn`).

#### **Code**

```python
# Import necessary libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Set the style for our plots
sns.set(style="whitegrid")
print("Libraries imported successfully!")
```

-----

### **2. Data Loading & Initial Inspection**

#### **Description**

The dataset, `Airbnb_Open_Data.csv`, is loaded into a pandas DataFrame. We then display the first five rows using `.head()` to get an initial understanding of the data's structure, columns, and content.

#### **Code**

```python
df = pd.read_csv('1730285881-Airbnb_Open_Data (1).xlsx - in.csv', low_memory=False)
print("Dataset loaded successfully!")
print("First 5 rows of the dataset:")
display(df.head())
```

-----

### **3. Data Cleaning and Preprocessing**

#### **Description**

This crucial step ensures the quality of our analysis. We handle missing values by filling them where appropriate (e.g., `reviews per month`) and drop irrelevant columns. We then correct the data types for `price` and `service fee`, converting them from text strings (e.g., "$966") to numerical values that can be used in calculations. Finally, we remove any duplicate rows.

#### **Code**

```python
df['reviews per month'].fillna(0, inplace=True)
df['review rate number'].fillna(0, inplace=True)
df.drop(['license', 'country', 'country code'], axis=1, inplace=True)

df['price'] = df['price'].replace({'\$': ''}, regex=True).astype(float)
df['service fee'] = df['service fee'].replace({'\$': ''}, regex=True).astype(float)

df.drop_duplicates(inplace=True)
print("Data cleaning and preprocessing complete.")
```

-----

### **4. Analysis of Listings by Borough**

#### **Description**

To understand the geographical distribution of listings, we create a count plot showing the number of Airbnb properties in each of New York City's five boroughs. This visualization quickly tells us which boroughs are the most popular for Airbnb rentals.

#### **Code**

```python
plt.figure(figsize=(10, 6))
sns.countplot(y='neighbourhood group', data=df, order = df['neighbourhood group'].value_counts().index, palette='plasma')
plt.title('Number of Listings by Neighbourhood Group')
plt.xlabel('Number of Listings')
plt.ylabel('Neighbourhood Group')
plt.show()
```

#### **Visualization**
![Analysis of Listings by Borough](https://github.com/whoistausif/VOIS_AICTE_Oct2025_MOHAMMAD_TAUSIF/blob/main/Analysis%20of%20Listings%20by%20Borough.png)
-----

### **5. Analysis of Room Type Distribution**

#### **Description**

A pie chart is used to show the proportion of different room types available on the platform. This helps us understand what kind of accommodation is most common—whether it's entire apartments, private rooms, or shared spaces.

#### **Code**

```python
plt.figure(figsize=(8, 8))
df['room type'].value_counts().plot.pie(autopct='%1.1f%%', startangle=90, colors=sns.color_palette('pastel'))
plt.title('Distribution of Room Types')
plt.ylabel('') # Hides the y-axis label
plt.show()
```

#### **Visualization**
![Analysis of Room Type Distribution](https://github.com/whoistausif/VOIS_AICTE_Oct2025_MOHAMMAD_TAUSIF/blob/main/Analysis%20of%20Room%20Type%20Distribution.png)
-----

### **6. Price Distribution Analysis**

#### **Description**

We plot a histogram to visualize the distribution of listing prices. To make the chart more readable, we filter out extreme outliers (prices above $500) to focus on the most common price range. This shows us the typical cost of an Airbnb in NYC.

#### **Code**

```python
plt.figure(figsize=(10, 6))
sns.histplot(df[df['price'] < 500]['price'], bins=50, kde=True)
plt.title('Price Distribution for Listings under $500')
plt.xlabel('Price ($)')
plt.ylabel('Number of Listings')
plt.show()
```

#### **Visualization**
![Price Distribution Analysis](https://github.com/whoistausif/VOIS_AICTE_Oct2025_MOHAMMAD_TAUSIF/blob/main/Price%20Distribution%20Analysis.png)
-----

### **7. Correlation Analysis of Features**

#### **Description**

A correlation heatmap is a powerful tool to visualize the relationships between different numerical variables in the dataset. The color intensity indicates the strength of the correlation (positive or negative) between variables like price, number of reviews, and availability.

#### **Code**

```python

numerical_cols = ['price', 'service fee', 'minimum nights', 'number of reviews', 'review rate number', 'availability 365']
corr_matrix = df[numerical_cols].corr()

plt.figure(figsize=(12, 9))
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm', fmt=".2f")
plt.title('Correlation Matrix of Numerical Features')
plt.show()
```

#### **Visualization**
![Correlation Analysis of Features](https://github.com/whoistausif/VOIS_AICTE_Oct2025_MOHAMMAD_TAUSIF/blob/main/Correlation%20Analysis%20of%20Features.png)
-----

### **8. Analysis of Most Expensive Neighborhoods**

#### **Description**

To identify the most premium locations, we calculate the average price per neighborhood and plot the top 20 most expensive ones. This provides a clear ranking and is valuable for travelers looking for luxury stays or hosts evaluating their pricing strategy.

#### **Code**

```python

avg_price_by_neighborhood = df.groupby('neighbourhood')['price'].mean().sort_values(ascending=False).head(20)

plt.figure(figsize=(12, 8))
sns.barplot(x=avg_price_by_neighborhood.values, y=avg_price_by_neighborhood.index, palette='viridis')
plt.title('Top 20 Most Expensive Neighborhoods')
plt.xlabel('Average Price ($)')
plt.ylabel('Neighborhood')
plt.show()
```

#### **Visualization**
![Analysis of Most Expensive Neighborhoods](https://github.com/whoistausif/VOIS_AICTE_Oct2025_MOHAMMAD_TAUSIF/blob/main/Analysis%20of%20Most%20Expensive%20Neighborhoods.png)
