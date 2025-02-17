# Airbnb Data Analysis

> Analyzing short-term rental trends, pricing strategies, and market insights to optimize Airbnb listings.

## Table of Contents
* [Overview](#Overview)
* [Research Questions](#research-Questions)
* [Dataset](#Dataset)
* [Recommendation for Airbnb Hosts](#recommendations)
* [Technologies Used](#technologies-used)
* [Setup Instructions](#setup-instructions)
* [How It Works](#how-it-works)
* [Code Snippets](#code-snippets)
* [Features](#features)
* [Status](#status)
* [Challenges](#challenges)
* [Learnings](#learnings)
* [Contributors](#contributors)
* [Contact](#contact)

## Overview
This project analyzes the **Airbnb short-term rental market**, focusing on pricing optimization, room type distribution, and city-wise trends. The goal is to help hosts establish competitive rates, predict factors impacting pricing, and identify market patterns.

## Research Questions
* What are the trends in the short-term rental market?
* How can hosts set competitive pricing strategies?
* What room types are most popular across different cities?
* How do different factors influence pricing and occupancy rates?

## Dataset
The dataset was obtained from **Kaggle** and includes:
- **ID, Listing Name, Host ID, Host Name** (Removed for analysis)
- **Neighbourhood, Neighbourhood Group**
- **Latitude, Longitude**
- **Room Type** (Private room, Shared room, Entire home/apartment)
- **Price per night**
- **Minimum nights required**
- **Number of reviews, Last review date, Reviews per month** (Removed missing values)
- **Availability (days per year)**
- **Total listings per host**

### Data Preprocessing
- Removed **irrelevant columns**: ID, Listing Name, Host ID, Host Name
- Dropped **missing values** from columns: Last Review, Neighbourhood Groups, Reviews Per Month
- Removed **outliers** in 'Price' using percentile-based filtering

### Price Prediction Using Multiple Linear Regression
Objective: Help hosts optimize pricing strategies.

**Insights:**
- **Private rooms** dominate when pricing is **under $65.5**
- In **New York**, private rooms remain preferred up to **$85.5**
- **Entire homes/apartments** become dominant as prices increase beyond **$85.5**
- If a stay exceeds **65 nights**, entire homes are preferred in **New York**

### Clustering Analysis
Using clustering techniques, Airbnb listings were grouped into **four major clusters**:

1. **Highly Reviewed Dwellings** - Low price, high availability, and high reviews (e.g., Seattle, Portland, Nashville)
2. **Diverse Accommodations Hub** - Medium price, varied room types, lower review counts (e.g., Los Angeles, NYC)
3. **Extended Stay Options** - Budget-friendly, long-stay accommodations (e.g., Boston, Chicago, SF)
4. **Upscale Retreats** - Luxury listings with high pricing and low minimum nights (e.g., Austin, San Diego)

## Recommendations for Airbnb Hosts
- **Encourage Reviews:** Hosts in **diverse hubs** should encourage guest reviews for better visibility.
- **Personalized Experiences:** Luxury rentals should focus on personalization to enhance guest satisfaction.
- **Extended Stay Listings:** Promote **amenities** for long-term guests.
- **Competitive Pricing:** Ensure year-round availability and adjust prices based on market demand.
- **Private Room Pricing:** Keep prices **below $65.5** for better occupancy (except NYC, where guests accept **$65.5-$85.5** pricing).
- **Regularly Adjust Pricing:** Monitor market trends and adjust prices to stay competitive.

## Technologies Used
- **Python** (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)
- **Jupyter Notebook**
- **Machine Learning Models** (Linear Regression, Decision Trees, Clustering)
- **Data Cleaning & Visualization**

## Setup Instructions
1. Clone the repository: `git clone [repo-url]`
2. Install dependencies: `pip install -r requirements.txt`
3. Run the analysis: `python analysis.py`

## How It Works
1. **Load and clean the data**
2. **Perform exploratory data analysis** (EDA)
3. **Train machine learning models** for price prediction
4. **Analyze classification trees** for room type optimization
5. **Perform clustering analysis** for market segmentation
6. **Generate insights and recommendations** for Airbnb hosts

## Code Snippets
```python
# Example: Training a multiple linear regression model
from sklearn.linear_model import LinearRegression
model = LinearRegression()
model.fit(X_train, y_train)
```

## Features
- **Airbnb Pricing Analysis**
- **Market Trend Analysis**
- **Predictive Price Modeling**
- **Optimal Room Type Classification**
- **Clustering Analysis for Segmentation**


## Status
✅ **Completed** – Open to further refinements and feedback.

## Challenges
- Handling **large datasets** with missing values
- Ensuring **price predictions are interpretable**
- Managing **imbalanced data** for classification models
  
## Learnings
- **Improved ML model selection** for pricing predictions
- **Understanding Airbnb market dynamics** across cities
- **Applying clustering for customer segmentation**

## Contributors
- **Vinmathi Iyappan** - Data Analysis & Machine Learning

## Contact 
🔗 **LinkedIn:** [YourLinkedInProfile]([https://www.linkedin.com/in/vinmathi-iyappan/])  
🖥 **GitHub:** [YourGitHubProfile](https://github.com/Vinmathiiyappan)
