# Analysis of the New York City Airbnb Market 🗽

A comprehensive data-driven exploration of NYC's short-term rental landscape using Python, pandas, and Seaborn.

**Author:** Mohmmad Tausif | **Internship ID:** INTERNSHIP_17546440516895be537820f

---

## ► Table of Contents
- [Project Overview](#-project-overview)
- [Dataset](#-dataset)
- [Technologies Used](#-technologies-used)
- [Key Visualizations & Insights](#-key-visualizations--insights)
- [Setup & Usage](#-setup--usage)

---

## ► Project Overview

This project provides a deep dive into the New York City Airbnb market. The goal is to analyze the publicly available Airbnb dataset to uncover trends, patterns, and insights related to listing distribution, pricing strategies, and host activity. By cleaning the data and creating compelling visualizations, we can better understand the dynamics of one of the world's most competitive rental markets.

---

## ► Dataset

The analysis is based on the **NYC Airbnb Open Data** file. This dataset includes detailed information on thousands of listings, including location, room type, price, availability, number of reviews, and host details.

---

## ► Technologies Used

-   **Python:** The core programming language for the analysis.
-   **Pandas:** Used for data manipulation, cleaning, and processing.
-   **Matplotlib & Seaborn:** Used for creating informative and visually appealing data visualizations.
-   **Jupyter Notebook / Google Colab:** The interactive environment for running the analysis.

---

## ► Key Visualizations & Insights

### 📊 Listings by Borough
The market is heavily concentrated in **Manhattan and Brooklyn**, which together account for over 85% of all listings. This highlights their status as the primary tourist hubs in NYC.

![Listings by Borough](images/listings_by_borough.png)

### 🏡 Room Type Distribution
**'Entire home/apt' (52.2%)** is the most frequently listed room type, indicating a high demand for private accommodations. 'Private rooms' follow closely, while 'Shared rooms' are rare.

![Room Types](images/room_types.png)

### 💰 Price Distribution
Most listings are priced under **$250 per night**, with a significant concentration between $100-$200. This histogram helps visualize the most common price points for travelers.

![Price Distribution](images/price_distribution.png)

### 🗺️ Most Expensive Neighborhoods
The analysis pinpoints the most premium neighborhoods, with areas in **Manhattan** commanding the highest average nightly rates.

![Top 20 Most Expensive Neighborhoods](images/top_20_neighborhoods.png)

### 🔥 Feature Correlation Heatmap
This heatmap reveals the relationships between numerical features. A strong positive correlation is observed between **`price` and `service fee`**, which is expected. Other correlations are weaker, suggesting pricing is influenced by complex factors.

![Correlation Heatmap](images/correlation_heatmap.png)

---

## ► Setup & Usage

To replicate this analysis, please follow these steps:

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    ```
2.  **Navigate to the Directory**
    ```bash
    cd your-repository-name
    ```
3.  **Install Dependencies**
    ```bash
    pip install pandas matplotlib seaborn notebook
    ```
4.  **Launch the Notebook**
    ```bash
    jupyter notebook Your_Notebook_Name.ipynb
    ```

---
