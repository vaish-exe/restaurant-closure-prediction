#  Restaurant Closure Prediction Using Yelp Reviews

###  Project Overview
This project explores the behavioral and sentiment-driven signals that precede restaurant closures, using review and user data from Yelp. By analyzing customer sentiment, elite user influence, and cuisine trends, we uncover what separates thriving restaurants from those on the brink of closure.

Focused on **Arizona**, the project combines **natural language processing**, **sentiment scoring**, and **machine learning** to model restaurant longevity and predict closures.

---

### Core Research Questions
-  **Sentiment Analysis**: Does customer sentiment predict closure?
-  **Elite User Influence**: Do elite Yelp users shape restaurant success?
-  **Cuisine Trends**: Which cuisines are more closure-prone or high-performing?
-  **Review Trajectories**: How do review patterns evolve for restaurants that eventually close?

---

###  Dataset & Preprocessing
We used and combined three datasets:
- `business.json` – metadata including status (open/closed), categories, location
- `review.json` – customer reviews with text and ratings
- `user.json` – user profile info including elite status

Steps included:
- Data filtering for **Arizona restaurants**
- Time-based slicing of reviews (6–12 months before closure)
- Sentiment scoring using **VADER**
- Feature engineering from review text, dates, and user metadata

---

### Techniques & Tools Used
- **Python**, **Pandas**, **NumPy**
- **VADER** for sentiment scoring
- **Matplotlib**, **Seaborn**, **Plotly** for visualizations
- **Scikit-learn** – logistic regression, random forest
- **TensorFlow / Keras** – LSTM modeling

---

###  Models Implemented

#### 🔹 Logistic Regression  
Interpretable baseline model using structured features like average sentiment, review length, and review volume.

#### 🔹 Random Forest  
Used for better performance and insights into **feature importance** (e.g., elite user ratio, cuisine type, sentiment variance).

#### 🔹 LSTM (Long Short-Term Memory)  
Trained on **time-sequenced sentiment scores** to model how emotional tone shifted leading up to closure.

---

###  Key Findings

- ❌ Restaurants that **closed** often had:
  - Lower sentiment scores
  - Negative sentiment trends
  - Shorter or less detailed reviews
  - Minimal engagement from elite users

- ⭐ **Elite users** wrote longer, more detailed, and more positive reviews for businesses that remained open.

- 🍲 **Cuisine Patterns**:
  - Mexican and Thai restaurants performed well
  - Some niche cuisines showed higher closure risks

- ⏳ **LSTM results** revealed:
  - A downward slope in sentiment in the months leading to closure
  - Detectable negative shifts **weeks before closure**

---

###  Value Proposition

The insights from this work can benefit:
- **Restaurant owners**: proactively monitor sentiment shifts and elite engagement
- **Investors**: identify higher-risk ventures
- **Yelp or review platforms**: improve recommendation and warning signals
- **Researchers**: extend temporal NLP modeling in consumer review analysis

---

###  Project Highlights
-  Combined structured + unstructured data
-  Integrated NLP with time-series deep learning
-  Predicted business closure with actionable indicators
-  Built a pipeline from raw JSON to ML-ready format

---

###  Future Work
- Incorporate **weather data** and **economic signals** per location
- Extend to other states/countries
- Add **topic modeling** (e.g., LDA) to extract common complaints
- Use SHAP for deep model interpretability

