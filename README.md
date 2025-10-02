# Analysis of the New York City Airbnb Market 🗽

### A Data-Driven Exploration using Python

**Author:** Mohmmad Tausif  
**Internship ID:** INTERNSHIP_17546440516895be537820f

---

## ► Project Overview

This project presents a comprehensive analysis of the Airbnb open dataset for New York City. The goal is to explore the data to uncover key trends and insights into the NYC short-term rental market. By leveraging Python and data science libraries, we analyze factors like pricing, availability, neighborhood popularity, and host activity to paint a clear picture of the Airbnb landscape in one of the world's most dynamic cities.

---

## ► Key Analyses & Features

-   **Data Cleaning:** Processed raw data to handle missing values, correct data types, and remove duplicates.
-   **Geospatial Analysis:** Investigated the distribution of listings across different boroughs and neighborhoods.
-   **Price Analysis:** Analyzed price distribution, price by room type, and identified the most expensive neighborhoods.
-   **Host Analysis:** Identified top hosts based on the number of listings.
-   **Correlation Study:** Examined the relationships between numerical features like price, reviews, and availability.
-   **Visualization:** Presented findings through a variety of plots including bar charts, pie charts, histograms, and heatmaps.

---

## ► Dataset

The dataset used for this analysis is the **NYC Airbnb Open Data**, which contains detailed information on listings, hosts, locations, prices, and reviews.

-   **Source:** Publicly available Airbnb data.
-   **File Name:** `Airbnb_Open_Data.csv`

---

## ► Technologies Used

-   **Language:** Python 3.x
-   **Libraries:**
    -   **Pandas:** For data manipulation and analysis.
    -   **NumPy:** For numerical operations.
    -   **Matplotlib & Seaborn:** For data visualization.
-   **Environment:** Jupyter Notebook / Google Colab

---

## ► Key Visualizations & Insights

Here are some of the key findings from the analysis, represented through visualizations.

### 📊 Listings by Borough
Manhattan and Brooklyn dominate the NYC Airbnb market, hosting the vast majority of listings.

![Listings by Borough](images/listings_by_borough.png)

### 🏡 Distribution of Room Types
The most common type of listing is an 'Entire home/apt', followed closely by 'Private room'.

![Room Types](images/room_types.png)

### 💰 Price Distribution
The price of listings is right-skewed, with a majority of properties priced under $250 per night.

![Price Distribution](images/price_distribution.png)

### 🗺️ Most Expensive Neighborhoods
The analysis reveals the top 20 most expensive neighborhoods, providing valuable insights for travelers on a budget and hosts setting their prices.

![Top 20 Most Expensive Neighborhoods](images/top_20_neighborhoods.png)

### 🔥 Correlation Heatmap
The heatmap shows the relationships between key numerical variables. As expected, `price` and `service fee` have a strong positive correlation.

![Correlation Heatmap](images/correlation_heatmap.png)

---

## ► How to Run This Project

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    ```
2.  **Navigate to the project directory:**
    ```bash
    cd your-repository-name
    ```
3.  **Install the required libraries:**
    ```bash
    pip install pandas numpy matplotlib seaborn
    ```
4.  **Run the Jupyter Notebook:**
    ```bash
    jupyter notebook Airbnb_Analysis.ipynb
    ```

---
