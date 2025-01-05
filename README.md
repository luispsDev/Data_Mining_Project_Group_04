# Data_Mining_Project_Group_04
# Comprehensive Customer Segmentation Strategy for ABCDEats, Inc.

## Developed By:
- **Beatriz Monteiro**
- **Luís Semedo**
- **Pedro Santos**
- **Rodrigo Miranda**

---

## Table of Contents
- [Abstract](#abstract)
- [Introduction](#introduction)
- [Repository Structure](#repository-structure)
- [Clustering Summary](#clustering-summary)
- [Workflow: Data Preprocessing and Clustering](#workflow-data-preprocessing-and-clustering)
- [Insights and Business Recommendations](#insights-and-business-recommendations)
- [Future Directions](#future-directions)
- [Acknowledgments](#acknowledgments)

---

## Abstract

This project aimed to develop a customer segmentation strategy for **ABCDEats, Inc.**, using unsupervised learning techniques. By analyzing behavioral and demographic data, we identified customer clusters to enhance marketing and service strategies. The project involved:
- Exploratory Data Analysis (EDA) to uncover patterns and relationships.
- A robust preprocessing pipeline to address inconsistencies, outliers, and missing values.
- Clustering techniques, including **KMeans** and **Hierarchical Clustering**, to identify meaningful customer groups.
- Customer profiling to generate actionable business insights.

---

## Introduction

The goal of this project is to analyze customer behavior and create a segmentation strategy that enhances **ABCDEats, Inc.**'s marketing efforts. Through detailed analysis of customer data, we sought to answer the following question:

**"How can we group customers based on their purchasing behavior to design targeted marketing strategies?"**

Using a structured methodology, this project combines data preprocessing, advanced clustering techniques, and actionable profiling insights to provide ABCDEats with a scalable, data-driven segmentation strategy.

---

## Repository Structure

- **`DM2425_Part1_04.pdf`**: Initial report detailing EDA and feature engineering.
- **`DM2425_Part2_04.pdf`**: Final project report with preprocessing pipeline, clustering, and business insights.
- **`notebooks`**:
  - `part1_eda.ipynb`: Exploratory Data Analysis and initial insights.
  - `part2_clustering.ipynb`: Clustering techniques and profiling.
- **`data`**: `DM2425_ABCDEats_DATASET.csv`

---

## Clustering Summary

We identified six distinct customer clusters using a combination of KMeans and Hierarchical Clustering techniques:
1. **Selective Spenders**: High spend per order but low frequency.
2. **The Average Joe**: Large volume of low-value orders.
3. **Revenue Powerhouses**: Highest overall spend and order volume.
4. **Western Preference Shoppers**: Preference for Western cuisines with lower spend.
5. **Occasional High Spenders on Asian Cuisine**: Low frequency but high-value Asian cuisine orders.
6. **Popular Asian Cuisine Enthusiasts**: Moderate spend with a focus on popular Asian dishes.

Each cluster was analyzed and profiled to guide targeted business strategies.

---

## Workflow: Data Preprocessing and Clustering

1. **Preprocessing**:
   - Addressed inconsistencies (e.g., duplicate rows, incoherent categorical features).
   - Handled missing values using logical imputation and KNN Imputer.
   - Engineered features such as aggregated cuisines, spending proportions, and customer activity metrics.
   - Scaled numerical features using **StandardScaler**.

2. **Feature Perspectives**:
   - Divided features into two key perspectives:
     - **Value Perspective**: Focused on monetary value and purchasing habits, including:
       - `total_money_spent`
       - `avg_spent_per_product`
     - **Preference Perspective**: Captured customer preferences for different cuisine types, including:
       - Cuisine proportions: `proportion_CUI_asian`, `proportion_CUI_western`, `proportion_CUI_popular_asian`, etc.
       - `orders_from_chain`: Reflecting preferences for chain restaurants.
   - These perspectives were used to create separate clusters based on distinct aspects of customer behavior.

3. **Clustering**:
   - Conducted SOM analysis to uncover patterns and correlations.
   - Removed outliers using DBSCAN.
   - Performed clustering using:
     - **KMeans**: Applied separately to each perspective (value and preference) to form initial clusters.
     - **Hierarchical Clustering**: Used to merge the clusters from the value and preference perspectives, refining the overall cluster structure.

4. **Profiling**:
   - Visualized clusters using t-SNE and UMAP.
   - Analyzed key features to differentiate and interpret clusters.

---

## Insights and Business Recommendations

Based on cluster profiles, we propose the following strategies:
- **Selective Spenders**: Encourage more frequent orders by offering free delivery for large orders.
- **The Average Joe**: Focus on increasing average order size through promotions.
- **Revenue Powerhouses**: Implement loyalty programs to retain high-value customers.
- **Western Preference Shoppers**: Promote complementary items in Western cuisine categories.
- **Occasional High Spenders on Asian Cuisine**: Incentivize higher order frequency with targeted discounts.
- **Popular Asian Cuisine Enthusiasts**: Highlight premium Asian cuisine offerings to boost engagement.

---

## Future Directions

- Explore additional clustering techniques.
- Develop an interactive dashboard for real-time customer segmentation insights.

---

## Acknowledgments

We would like to thank:
- **Professor Farina Pontejos** for her guidance and feedback.
- Open-source libraries such as **scikit-learn**, **pandas**, and **matplotlib** for enabling our analysis.

