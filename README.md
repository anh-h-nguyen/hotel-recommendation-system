# 🏨 Hotel Recommendation System

## Technologies Used
- Programming Language: Python  
- Libraries: Pandas, NumPy, Matplotlib, Scikit-learn  
- Tools: Jupyter Notebook  
- Datasets: Kaggle (Hotel Reviews & Offerings)  

## Project Overview
With thousands of hotels available, choosing the right one can be overwhelming. This project leverages previous guest reviews from Tripadvisor to build a hotel recommendation system, helping users find properties they’ll love based on their own experiences and those of similar travelers. Tripadvisor can benefit from this system by enhancing personalized recommendations, improving user retention, and gaining valuable insights into factors that impact guest satisfaction.

## Table of Contents
1. Introduction  
2. Features  
3. How It Works  
4. Interactive User Input  
5. Data Exploration  
6. Data Preparation  
7. Model Building & Evaluation  
8. Results Interpretation  
9. Future Improvements  

## Introduction
This project analyzes hotel reviews from Kaggle to identify patterns in guest preferences and recommend hotels that align with their tastes. By clustering reviewers based on their experiences, we create meaningful, tailored recommendations beyond just star ratings.

## Features
- Guest Segmentation Using Clustering: Identifies distinct groups of travelers based on shared preferences.  
- Interactive User Input: Allows users to enter their username, select a city, and define hotel class preferences.  
- Hotel Recommendations: Suggests properties based on user-selected criteria.  
- Advanced Data Processing: Cleans and analyzes text reviews using TF-IDF for meaningful insights.  
- Visualization Tools: Cluster maps and heat maps illustrate review trends and guest preferences.  

## How It Works
1. Users input their username to fetch personal hotel preferences.  
2. They select a city from an available list.  
3. They define their desired hotel class (1–5 stars).  
4. A clustering model analyzes guest preferences using past reviews.  
5. Hotels are recommended based on similar traveler experiences.  

## Interactive User Input  
The system includes an interactive loop where users can:  
- Enter their Tripadvisor username to retrieve relevant recommendations.  
- Choose a destination city from a curated list.  
- Define a preferred hotel class range (minimum and maximum star ratings).
- Receive personalized hotel recommendations based on past liked hotels and guest clusters.  
- Update preferences dynamically – Users can modify hotel class selections or search for another city.  
- Exit the program when they’ve found a hotel that fits their needs.  

## Data Exploration
- Ratings: Helps identify factors affecting overall hotel scores.  
- Author: Provides engagement insights (review count, helpful votes, locations).  
- Date Stayed: Explores seasonal trends in guest experiences.  
- Offering ID: Connects reviews to hotel data for more personalized suggestions.  

## Data Preparation
- Text Cleaning: Removed special characters, misspellings, whitespace, and stop words.  
- Missing Data Handling: Dropped unnecessary columns and filled missing values with "Unknown."  
- Feature Engineering: Converted text reviews into TF-IDF vectors for machine learning models.  

## Model Building & Evaluation
- Algorithm Used: K-Means Clustering  
- Evaluation Metrics:
  - Elbow Method: Determines the optimal number of clusters.
  - Silhouette Score: Measures how well-defined the clusters are.
  - Inertia: Evaluates cluster compactness.

## Results Interpretation
Using the Elbow Method, the optimal number of clusters was 12, meaning travelers fall into 12 distinct preference groups. Clusters showed overlapping features, highlighting shared characteristics among different guest segments.

Clusters can be described as:
- **Cluster 0:** Values high-quality suites & well-thought-out experiences.  
- **Cluster 1:** Focuses on hotel aesthetics and suite quality.  
- **Cluster 2:** Prioritizes location & convenience, with free amenities.  
- **Cluster 3:** Appreciates concierge services but considers price.  
- **Cluster 4:** Interested in pools & overall hotel experience, concerned about value.  
- **Cluster 5:** Mixed reviews—focuses on suites & pools.  
- **Cluster 6 & 7:** Value proximity to transport, but Cluster 7 emphasizes cleanliness.  
- **Cluster 8 & 9:** Ideal for short stays, focused on suite comfort & convenience.  
- **Cluster 10:** Pool access & location-driven preferences.  
- **Cluster 11:** Thoughtful experiences with subway accessibility.  

These clusters allow personalized hotel recommendations, helping Tripadvisor enhance user experience.

## Future Improvements
- Expand to More Recent Data: The dataset is from 2008–2012, so incorporating newer reviews would improve relevance.  
- Enhance User Experience: Allow users to save favorite hotels and refine recommendations based on feedback.  
- Implement Sentiment Analysis: Go beyond keyword clustering to analyze tone and sentiment in reviews.  
- Improve Evaluation Metrics: Use guest feedback validation to confirm recommendation accuracy.  
- Build a Web Interface: Develop a Streamlit or Flask-based app for better interactivity.  
