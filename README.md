# Airbnb Data Analysis

> Analyzing short-term rental trends, pricing strategies, and market insights to optimize Airbnb listings.

## Table of Contents
* [Overview](#overview)
* [Demo](#demo)
* [Screenshots](#screenshots)
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

## Data Preprocessing
- Removed **irrelevant columns**: ID, Listing Name, Host ID, Host Name
- Dropped **missing values** from columns: Last Review, Neighbourhood Groups, Reviews Per Month
- Removed **outliers** in 'Price' using percentile-based filtering

## Data Visualization
- **Average price across each city**
- **Number of listings per city**
- **Room type distribution**
- **Distribution of listings across cities**

## Price Prediction Using Multiple Linear Regression
Objective: Help hosts optimize pricing strategies.

**Key Findings:**
- Higher **availability (365 days/year)** slightly increases price
- More **minimum nights** leads to lower pricing
- **Higher review count** correlates with lower price (potentially due to competitive pricing strategies)
- **Private rooms** are priced **$98.92 lower** on average than entire homes/apartments

Despite a small **RMSE increase** (137.07 to 140.14), simplifying the model improved interpretability and practicality for real-world pricing strategies.

## Classification Trees
Objective: Identify optimal room type selection for pricing strategies.

**Insights:**
- **Private rooms** dominate when pricing is **under $65.5**
- In **New York**, private rooms remain preferred up to **$85.5**
- **Entire homes/apartments** become dominant as prices increase beyond **$85.5**
- If a stay exceeds **65 nights**, entire homes are preferred in **New York**

## Clustering Analysis
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

### Future Enhancements
- Add **time-series analysis** for seasonal price trends
- Improve predictive accuracy using **advanced ML models**
- Deploy an **interactive dashboard** for real-time insights

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
- **Contributor Name** (if applicable)

## Contact
📧 **Email:** [your-email@example.com](mailto:your-email@example.com)  
🔗 **LinkedIn:** [YourLinkedInProfile](https://linkedin.com/in/yourprofile)  
🖥 **GitHub:** [YourGitHubProfile](https://github.com/yourprofile)

# [Project Title]
> A brief, catchy tagline for the project.

## Table of Contents
* [Overview](#overview)
* [Demo](#demo)
* [Screenshots](#screenshots)
* [Technologies Used](#technologies-used)
* [Setup Instructions](#setup-instructions)
* [How It Works](#how-it-works)
* [Code Snippets](#code-snippets)
* [Features](#features)
* [Status](#status)
* [Contributors](#contributors)
* [Contact](#contact)

## Overview
Provide a summary of the project, its purpose, and the problem it solves. Mention if it was built during a hackathon or for a specific challenge.

## Demo
Include a link to a demo video, deployment, or presentation. Optionally embed a GIF or image of the project in action.

## Screenshots
Add 1-3 images showcasing the main features of your project. Describe the screenshots briefly.

## Technologies Used
List the main languages, libraries, frameworks, and tools used in the project. For example:
* Python
* TensorFlow
* React
* MongoDB

## Setup Instructions
Explain how to set up and run the project locally. For example:
1. Clone the repository: `git clone [repo-url]`
2. Install dependencies: `pip install -r requirements.txt`
3. Run the application: `python app.py`

## How It Works
Describe the core workflow or logic of the project in a few points. You can break it into steps or modules for clarity.

## Code Snippets
Include a small, key snippet of code to highlight an interesting or critical part of your project. For example:
````python
# Example: Training a machine learning model
model.fit(train_data, train_labels, epochs=10, validation_split=0.2)

````

## Features
Highlight the features your project currently supports:
* User authentication
* Real-time predictions
* Mobile responsiveness

### Future Enhancements
List potential features to add in the future:
* Add more datasets
* Improve accuracy
* Deploy the project on a cloud service

## Status
Clearly state the current status of your project:
* _In Progress_: Actively working on new features and improvements.
* _Completed_: No further updates planned, but open to feedback and collaboration.

## Challenges
Document any challenges faced during the project:
* Handling large datasets with limited compute power.
* Training the model on imbalanced datasets.
* Integration of multiple APIs for seamless functioning.

## Learnings
Highlight the key takeaways from the project:
* Enhanced understanding of model optimization techniques.
* Improved skills in debugging deployment issues.
* Learned to manage collaborative projects efficiently.

## Contributors
List all contributors involved in the project:
* [Your Name](https://github.com/YourGitHubProfile) - Role/Responsibility  
* [Contributor 1](https://github.com/Contributor1) - Role/Responsibility  
* [Contributor 2](https://github.com/Contributor2) - Role/Responsibility  

Feel free to add collaborators' GitHub or LinkedIn links for recognition.

## Contact
Feel free to reach out for collaboration, feedback, or questions.  
**Created by:** [Your Name]  

Connect with me:  
* **Email:** [youremail@example.com](mailto:youremail@example.com)  
* **GitHub:** [YourGitHubProfile](https://github.com/harshbg)  
* **LinkedIn:** [YourLinkedInProfile](https://linkedin.com/in/harshbg)  # test
