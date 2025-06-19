📱 App Rating Prediction – Google Play Store Analysis
🔍 Objective
Predict app ratings using key attributes such as reviews, installs, size, price, and app metadata. This helps Google Play Store identify promising apps that should be boosted for visibility under features like “You might also like” or “Top New Apps”.

🗂 Dataset
Source: Google Play Store

File: googleplaystore.csv

Records: ~10,000 apps

Fields Include:

App, Category, Rating, Reviews, Size, Installs, Type, Price, Content Rating, Genres, Last Updated, Current Ver, Android Ver

🛠 Tools & Technologies
Language: Python

Libraries: Pandas, NumPy, Seaborn, Matplotlib, Scikit-learn

Model Used: Linear Regression

📌 Key Steps Performed
1️⃣ Data Cleaning & Preprocessing
Removed 30% null records and fixed data type inconsistencies.

Standardized fields like Size, Installs, Price to numeric.

Applied sanity checks:

Removed ratings outside 1–5.

Dropped apps with Reviews > Installs.

Ensured all free apps have $0 price.

2️⃣ Univariate Analysis
Plotted boxplots & histograms for Price, Reviews, Ratings, Size.

Identified outliers in price (apps > $200), reviews (>2M), and installs (top 1%).

3️⃣ Outlier Treatment
Removed junk and outlier entries to avoid skewing results:

Dropped apps priced > $200

Dropped apps with >2M reviews

Removed apps above the 95th percentile in Installs

4️⃣ Bivariate Analysis
Explored relation of Rating with:

Price (weak positive correlation)

Size (moderate correlation)

Reviews (non-linear pattern)

Content Rating & Category (insightful group trends)

5️⃣ Feature Engineering
Applied log transformation to Reviews and Installs to reduce skew.

Dropped irrelevant columns (App, Last Updated, etc.)

Created dummy variables for categorical features (Category, Genres, Content Rating)

6️⃣ Model Building & Evaluation
Split data into 70% training / 30% testing

Built Linear Regression model

Achieved:

📊 R² (Train): ~0.75

📈 R² (Test): ~0.72

Model effectively predicts app ratings using structured metadata and usage metrics.

✅ Business Impact
Helps Google prioritize apps with high user satisfaction potential for promotion.

Offers developers insights into features influencing higher ratings.

Provides a framework for automated app assessment and recommendation scoring.

📎 Deliverables
Jupyter Notebook: App Rating Prediction.ipynb

Final Model: Trained Linear Regression model

Visual Insights: EDA and correlation plots

Output: Prediction-ready dataset and rating insights

📌 Future Enhancements
Use advanced models like Random Forest or XGBoost for better accuracy

Perform time-based rating analysis using Last Updated

Incorporate user sentiment analysis from review text (NLP)
