# Airbnb Listings 2024 (NYC) - EDA & Data Visualization 🌆📊

## Project Overview 🚀
This project performs **Exploratory Data Analysis (EDA)** and **Data Visualization** on the Airbnb Listings dataset for New York City in 2024. The objective is to uncover insights into pricing 💰, room types 🏠, neighborhood trends 🌎, and other key metrics using Python libraries such as Pandas, NumPy, Matplotlib, and Seaborn.

## Dataset 📋
The dataset (`airbnb dataset.csv`) contains **20,770 listings** with **22 columns**, including:
- `id`, `host_id`, `host_name`: Unique identifiers for listings and hosts 🆔.
- `neighbourhood_group`, `neighbourhood`: Location details (e.g., Manhattan, Brooklyn) 🗽.
- `latitude`, `longitude`: Geographic coordinates 🌍.
- `room_type`: Type of listing (e.g., Entire home/apt, Private room) 🛏️.
- `price`, `minimum_nights`, `number_of_reviews`, `reviews_per_month`: Pricing and review metrics ⭐.
- `rating`, `bedrooms`, `beds`, `baths`: Property details 🛁.
- `license`, `availability_365`: Licensing and availability information 📅.

## Project Structure 🛠️
1. **Data Loading and Exploration** 🔍:
   - Loaded the dataset using Pandas.
   - Explored the first and last 5 rows, dataset shape (20,770 rows, 22 columns), data types, and statistical summary.
   - Identified missing values (e.g., 34 in `price`, 7 in `neighbourhood`) and duplicates (12 records).

2. **Data Cleaning** 🧹:
   - Handled missing values by dropping rows with `dropna()` (permanent change).
   - Removed 12 duplicate records based on all columns.
   - Final cleaned dataset: **20,724 rows**.

3. **Data Analysis** 📈:
   - **Univariate Analysis**:
     - Analyzed `price` distribution using histograms and boxplots to identify outliers 📊.
     - Filtered listings with `price < $1500` to remove extreme outliers (20,636 rows after filtering).
   - **Feature Engineering**:
     - Created `price_per_bed` by dividing `price` by `beds` to evaluate cost efficiency per bed 💸.
   - **Bivariate Analysis**:
     - Explored price dependency on `neighbourhood_group` and `room_type` using bar plots.
     - Calculated mean `price` and `price_per_bed` by `neighbourhood_group`.

4. **Visualizations** 🎨:
   - **Price Distribution**: Histogram to show the frequency of listing prices 📉.
   - **Outlier Detection**: Boxplots to identify and filter extreme prices 📍.
   - **Price by Neighborhood and Room Type**: Bar plot to visualize average prices across neighborhoods and room types 📊.

## Key Findings 🔑
- **Price Distribution** 💵:
  - Prices are right-skewed, with most listings below $500. Outliers above $1500 were filtered for improved analysis.
- **Neighborhood Insights** 🏙️:
  - **Manhattan**: Highest average price ($204.15) and price per bed ($138.71).
  - **Bronx**: Most affordable, with an average price of $107.99 and price per bed of $74.71.
  - **Brooklyn**: Average price of $155.14 and price per bed of $99.79.
  - **Queens**: Average price of $121.68 and price per bed of $76.34.
  - **Staten Island**: Average price of $118.78 and price per bed of $67.73.
- **Room Type Trends** 🏠:
  - Entire home/apartment listings are generally more expensive than private rooms across all neighborhoods.
- **Data Quality** ✅:
  - Minimal missing data and duplicates were effectively handled to ensure reliable analysis.

