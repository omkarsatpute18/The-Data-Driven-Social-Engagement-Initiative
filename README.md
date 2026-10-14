# Data-Driven Social Engagement Initiative

A data-driven social media analytics and recommendation system designed to understand what makes relatable content perform well, identify viral content patterns, analyze audience emotional responses, forecast emerging trends, and generate content recommendations.

---

## 1. Project Overview

The **Data-Driven Social Engagement Initiative** combines data analytics, natural language processing, statistical analysis, machine learning, trend analysis, and an interactive Flask dashboard.

The system analyzes social media content and audience comments to understand:

- Which topics perform better
- What characteristics are associated with viral content
- How audiences emotionally respond to content
- How relatable and problem-aware audience comments are
- Which topics have higher viral potential
- How emerging trends can influence content strategy
- What content strategy can be recommended for future posts

The project uses **YouTube data as the primary public data source** and **MySQL** as the database component.

---

## 2. Problem Statement

Social media platforms generate large amounts of content and audience interaction data. However, identifying why certain relatable topics receive significantly higher engagement is difficult without systematic analysis.

This project addresses that problem by building a data-driven pipeline that:

1. Collects content and audience data.
2. Cleans and validates the collected data.
3. Performs exploratory and statistical analysis.
4. Analyzes audience comments using NLP.
5. Identifies patterns associated with viral content.
6. Builds machine learning models for viral-content prediction.
7. Generates content recommendations.
8. Analyzes emerging trends.
9. Combines historical performance, ML predictions, and trend signals.
10. Presents the results through an interactive Flask dashboard.

---

## 3. Project Objectives

The main objectives are:

- Analyze social media content performance.
- Calculate engagement-related metrics.
- Identify high-performing and viral content.
- Understand audience emotional responses.
- Classify comments based on relatability and problem awareness.
- Identify important relationships between audience response and content performance.
- Compare machine learning models for viral-content prediction.
- Generate data-driven content recommendations.
- Analyze emerging topic trends.
- Build a user-friendly analytics dashboard.

---

## 4. Key Features

### Data Collection

- YouTube video search data
- YouTube video statistics
- YouTube public comments
- Trend data
- Controlled content-series data for A/B experiment design

### Data Processing

- Data validation
- Duplicate handling
- Dataset integration
- Feature engineering
- Clean analytical datasets

### NLP Analysis

- Comment cleaning
- Sentiment analysis
- Relatability classification
- Problem-awareness classification
- Video-level audience response aggregation

### Statistical Analysis

- Correlation analysis
- Engagement analysis
- Viral vs non-viral comparison
- A/B testing experiment design
- Cross-validation comparison

### Machine Learning

- Viral-content classification
- Logistic Regression
- Random Forest
- Model comparison
- Viral probability scoring

### Recommendation Engine

- Topic performance analysis
- Content characteristic analysis
- Historical recommendation scoring
- ML-based viral probability
- Trend-aware recommendations

### Trend Analysis

- Search-volume analysis
- Hashtag-volume analysis
- Trend-score calculation
- Rising-topic identification

### Dashboard

Interactive Flask dashboard containing:

- Overview
- Content Performance
- Audience & NLP
- Trend Analysis
- Recommendations

---

# 5. System Architecture

```text
                ┌──────────────────────┐
                │   YouTube / Trend    │
                │        Data          │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │   Data Collection    │
                │   & Validation       │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │   Data Processing    │
                │   & Feature          │
                │   Engineering       │
                └──────────┬───────────┘
                           │
             ┌─────────────┼─────────────┐
             ▼             ▼             ▼
       ┌──────────┐  ┌───────────┐  ┌────────────┐
       │   EDA    │  │    NLP    │  │ Statistics │
       └────┬─────┘  └─────┬─────┘  └──────┬─────┘
            │              │               │
            └──────────────┼───────────────┘
                           ▼
                ┌──────────────────────┐
                │ Machine Learning     │
                │ Viral Prediction     │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │ Recommendation       │
                │ Engine               │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │ Trend-aware          │
                │ Recommendations      │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │ Flask Dashboard      │
                └──────────────────────┘

6. Technology Stack
Programming Language
- Python
Data Analysis
- Pandas
- NumPy
Visualization
- Matplotlib
- Seaborn
- HTML
- CSS
- JavaScript
Machine Learning
- Scikit-learn
Natural Language Processing
- NLTK
- TextBlob
Statistical Analysis
- SciPy
- Statsmodels
Database
- MySQL
Web Application
- Flask
- HTML
- CSS
- JavaScript
Data Collection
- YouTube Data API
Environment Management
- Python Virtual Environment
- python-dotenv
7. Dataset
The project uses multiple datasets collected and generated throughout the analytical pipeline.
Raw Data
data/raw/
├── comments/
│   └── youtube_comments.csv
│
├── tremds/
│   └── trend_data.csv
│
├── youtube/
│   ├── video_search_results.csv
│   ├── video_statistics.csv
│   └── youtube_combined.csv
│
└── content_series.csv

The tremds folder name is retained because it is the existing project path used by the trend-analysis implementation.
Processed Data
data/processed/
├── clean_comments.csv
├── final_recommendations.csv
├── master_video_dataset.csv
├── ml_features.csv
├── nlp_comments.csv
├── rising_topics.csv
├── sentiment_comments.csv
├── test_data.csv
├── topic_performance.csv
├── train_data.csv
├── trend_analysis.csv
├── trend_aware_recommendations.csv
├── video_features.csv
├── video_nlp_dataset.csv
├── video_viral_dataset.csv
└── viral_predictions.csv

8. Data Collection
The project collected YouTube content around relatable topics including:
- Overthinking
- Social Anxiety
- Academic Pressure
- Career Anxiety
- Loneliness
- Friendship Problems
- Dating Anxiety
- Self Confidence
- Procrastination
- Student Stress
The initial collection contained:
- 200 search records
- 200 statistics records
After duplicate handling, the analytical dataset contains:
- 196 unique videos
The project also collected:
- 15,682 public YouTube comments
9. Data Processing
The processing pipeline performs:
1. Data validation
2. Duplicate identification
3. Dataset integration
4. Feature generation
5. Preparation of analytical datasets
Important generated datasets include:
master_video_dataset.csv
video_nlp_dataset.csv
ml_features.csv
train_data.csv
test_data.csv

10. Exploratory Data Analysis
Exploratory analysis was performed to understand:
- Distribution of video views
- Likes and comments
- Engagement
- Topic-level performance
- Relationship between views and engagement
- Viral vs non-viral content
- NLP-related audience metrics
EDA outputs are stored in:
reports/eda/

Example outputs include:
average_views_by_topic.png
comments_vs_views.png
correlation_matrix.png
engagement_by_topic.png
engagement_rate_distribution.png
engagement_vs_views.png
likes_vs_views.png
views_distribution.png
viral_comparison.csv

11. NLP Analysis
The NLP pipeline analyzes public comments to understand audience response.
Step 1: Comment Cleaning
The original dataset contained:
- 15,682 comments
After cleaning and duplicate/empty-comment handling:
- 14,169 clean comments
The output is:
data/processed/clean_comments.csv

Step 2: Sentiment Analysis
Sentiment analysis classified comments into:
- Positive
- Neutral
- Negative
Results:
- Positive: 6,146
- Neutral: 5,662
- Negative: 2,361
Average sentiment score:
0.0978

Step 3: Relatability Analysis
The analysis identified:
- Relatable comments: 607
- Neutral comments: 13,562
Approximate relatability rate:
4.28%

Step 4: Problem Awareness
The system identified:
- Problem-aware comments: 4,235
- Not problem-aware: 9,934
Approximate problem-awareness rate:
29.89%

The NLP results are aggregated at video level in:
data/processed/video_nlp_dataset.csv

12. Statistical Analysis
Statistical analysis was performed to investigate relationships between content performance and audience response.
Spearman correlation analysis was used because several variables were highly skewed.
Important findings included:
- Views and likes showed a very strong positive relationship.
- Views and comments also showed a strong positive relationship.
- Relatability rate had a weak positive relationship with views.
- Problem-awareness rate did not show a significant relationship with views.
- Average sentiment did not show a significant relationship with views.
The relationship between relatability rate and views was:
Spearman rho ≈ 0.1585
p ≈ 0.0265

This indicates a weak statistical association in this dataset. It should not be interpreted as proof of causation.
13. Viral Content Analysis
Viral content was defined using the 90th percentile of views.
The viral threshold was approximately:
4,278,044 views

The dataset contained:
196 total videos
20 viral videos
176 non-viral videos

The viral sample included topics such as:
- Self Confidence
- Loneliness
- Overthinking
- Friendship Problems
- Procrastination
- Academic Pressure
- Career Anxiety
- Dating Anxiety
- Student Stress
Self Confidence and Loneliness represented a substantial portion of the viral sample.
Because the viral sample contains only 20 videos, these patterns should be treated as indicative rather than conclusive.
14. A/B Testing
The project includes a controlled content-series dataset for experiment design.
The current experiment variables include:
- Short vs Long content
- Visual vs Text hooks
- Evening vs Night posting periods
- Different caption styles
The current experiment dataset contains five controlled content-series records.
However, the dataset does not contain corresponding performance outcomes for these experimental groups.
Therefore, statistical significance tests and definitive A/B winners cannot be established from the current sample.
The experiment design is stored in:
reports/statistics/ab_experiment_design.csv

Future controlled data collection can be used to calculate statistically significant experiment results.
15. Machine Learning
The project evaluates machine learning models for viral-content classification.
Target
The target variable is:
viral

where:
1 = Viral
0 = Non-Viral

The target is based on the 90th-percentile view threshold.
Features
Only features available before or around publication are used for prediction.
Examples include:
- Topic
- Publishing hour
- Publishing day
- Weekend indicator
- Title length
- Title word count
- Question-mark presence
- Exclamation-mark presence
- Number presence
- Uppercase-character count
Post-publication performance variables such as views, likes, comments and NLP-derived audience response metrics are excluded from the predictive feature set to reduce target leakage.
16. Model Comparison
Two primary models were evaluated:
Logistic Regression
Test performance:
Accuracy  : 0.6750
Precision : 0.1538
Recall    : 0.5000
F1 Score  : 0.2353
ROC-AUC   : 0.5417

Random Forest
Test performance:
Accuracy  : 0.8500
Precision : 0.0000
Recall    : 0.0000
F1 Score  : 0.0000
ROC-AUC   : 0.4236
PR-AUC    : 0.1058

Cross-validation also favored Logistic Regression on the more relevant classification metrics.
Therefore, Logistic Regression was selected as the preferred model for the current dataset.
Because only 20 videos are classified as viral, the positive class is small and model metrics should be interpreted cautiously.
17. Viral Prediction
The final Logistic Regression model was trained on the available dataset and used to generate viral probability scores.
Output:
data/processed/viral_predictions.csv

The system categorizes predicted viral potential into levels such as:
- Low
- Medium
- High
The probability score represents model-estimated viral potential and should not be interpreted as a guarantee that a video will become viral.
18. Recommendation Engine
The recommendation engine combines multiple signals to rank content topics.
The topic recommendation score uses:
30% Median Views
25% Viral Rate
20% Average ML Probability
15% Average Relatability
10% Average Problem Awareness

The highest-ranked topics in the current dataset include:
1. Loneliness
2. Self Confidence
3. Overthinking
4. Friendship Problems
5. Academic Pressure
The recommendation output is stored in:
data/processed/final_recommendations.csv

The scoring system is a transparent heuristic rather than a separately trained recommendation model.
19. Content Characteristics
The project also analyzes content characteristics including:
- Publishing hour
- Publishing day
- Title length
- Title word count
- Question-based titles
- Number-based titles
- Exclamation usage
The current dataset suggested stronger performance for some early-morning publishing hours and particular days.
However, some hourly groups contain very few observations. Therefore, these findings should be treated as exploratory rather than universal posting-time rules.
The recommendation system applies minimum sample-size thresholds when selecting posting characteristics.
20. Trend Analysis
Trend analysis uses:
- Search volume
- Hashtag volume
The current trend dataset contains three observations for the keyword:
overthinking

Search volume increased from:
6,200 → 7,100 → 8,500

Hashtag volume increased from:
45,000 → 48,000 → 53,000

This indicates a preliminary upward trend.
Trend analysis outputs:
data/processed/trend_analysis.csv
data/processed/rising_topics.csv

Visualizations are stored under:
reports/forecasting/

Because the current trend dataset contains only three observations for one keyword, it should be considered a preliminary trend signal rather than a robust long-term forecasting model.
21. Trend-Aware Recommendations
The final recommendation stage combines:
40% Historical Performance
30% Machine Learning Score
30% Trend Signal

This allows the system to combine historical content performance with predicted viral potential and emerging trend information.
Output:
data/processed/trend_aware_recommendations.csv

22. MySQL Database
The project includes a MySQL database schema covering:
content
performance_metrics
comments
sentiment_results
trend_data
experiments
recommendations

The SQL implementation is available at:
database/sql/social_engagement_db.sql

The SQL file contains:
- Database creation
- Table creation
- Foreign-key relationships
- Sample records
- JOIN queries
- Engagement calculations
- Share-rate calculations
- Save-rate calculations
- Save-to-share ratio
- Follower-growth calculations
- Additional source metadata fields
23. Flask Dashboard
The project includes an interactive Flask dashboard.
Dashboard structure:
dashboards/
├── app.py
├── static/
│   ├── css/
│   │   └── style.css
│   └── js/
│       └── dashboard.js
│
└── templates/
    ├── base.html
    ├── index.html
    ├── content.html
    ├── audience.html
    ├── trends.html
    └── recommendations.html

Dashboard Pages
Overview
Provides a high-level summary of:
- Total videos
- Total views
- Engagement
- Viral content
- Topic performance
Content
Provides content-level performance information.
Audience & NLP
Displays:
- Average sentiment
- Relatability
- Problem awareness
- Audience response analysis
Trend Analysis
Displays:
- Trend signals
- Search-volume trends
- Hashtag trends
- Rising topics
Recommendations
Displays:
- Recommended topics
- Viral probability
- Recommendation scores
- Trend-aware recommendations
24. Running the Dashboard
Activate the Python virtual environment.
Then run:
python dashboards/app.py

Open the dashboard in a browser:
http://127.0.0.1:5000/

Do not use VS Code Live Server for the Flask dashboard.
25. Installation
1. Create a Virtual Environment
python -m venv venv

2. Activate the Virtual Environment on Windows
venv\Scripts\activate

3. Install Dependencies
pip install -r requirements.txt

4. Configure Environment Variables
Create a .env file in the project root.
Example:
YOUTUBE_API_KEY=your_api_key_here

Do not commit real API keys or other secrets to GitHub.
26. Running the Data Pipeline
The major processing stages can be executed through the scripts inside src/.
Data Collection
python src/data_collection/youtube_search.py
python src/data_collection/youtube_statistics.py
python src/data_collection/youtube_comments.py

Data Processing
python src/data_processing/validate_data.py
python src/data_processing/create_master_dataset.py
python src/data_processing/feature_engineering.py

NLP
python src/nlp/clean_comments.py
python src/nlp/sentiment_analysis.py
python src/nlp/relatability_analysis.py
python src/nlp/nlp_video_summary.py

Statistical Analysis
python src/statistics/eda.py
python src/statistics/statistical_analysis.py
python src/statistics/viral_analysis.py
python src/statistics/ab_testing.py

Machine Learning
python src/model/feature_engineering.py
python src/model/prepare_ml_data.py
python src/model/train_baseline.py
python src/model/train_random_forest.py
python src/model/model_comparison.py
python src/model/final_model.py

Recommendations
python src/model/topic_recommendation.py
python src/model/content_characteristics.py
python src/model/final_recommendation_engine.py

Trend Analysis
python src/forecasting/trend_analysis.py
python src/model/trend_aware_recommendation.py

Final Validation
python src/data_processing/final_project_validation.py

Finally, launch the dashboard:
python dashboards/app.py

27. Project Structure
The Data-Driven Social Engagement Initiative/
│
├── dashboards/
│   ├── app.py
│   ├── static/
│   │   ├── css/
│   │   │   └── style.css
│   │   └── js/
│   │       └── dashboard.js
│   │
│   └── templates/
│       ├── base.html
│       ├── index.html
│       ├── content.html
│       ├── audience.html
│       ├── trends.html
│       └── recommendations.html
│
├── data/
│   ├── raw/
│   │   ├── comments/
│   │   ├── tremds/
│   │   ├── youtube/
│   │   └── content_series.csv
│   │
│   ├── processed/
│   │
│   └── final/
│
├── database/
│   └── sql/
│       └── social_engagement_db.sql
│
├── notebooks/
│
├── reports/
│   ├── eda/
│   ├── forecasting/
│   ├── statistics/
│   └── validation/
│
├── src/
│   ├── data_collection/
│   ├── data_processing/
│   ├── forecasting/
│   ├── model/
│   ├── nlp/
│   └── statistics/
│
├── .env
├── .gitignore
├── README.md
└── requirements.txt

28. Final Data Validation
A final project data-validation script was created:
src/data_processing/final_project_validation.py

The validation checks the required raw and processed datasets.
Current validation result:
======================================================================
FINAL PROJECT DATA VALIDATION
======================================================================

Total files checked : 19
Passed              : 19
Failed              : 0

======================================================================
ALL DATASETS PASSED VALIDATION
======================================================================

The validation report is stored at:
reports/validation/final_data_validation.csv

Additional validation information:
Missing cells : 5
Duplicate rows: 914

The datasets passed the implemented validation checks with no failed files.
29. Dashboard Validation
The Flask dashboard was manually tested after completing the data pipeline.
The following dashboard routes were verified:
/
 /content
 /audience
 /trends
 /recommendations

The dashboard successfully loaded the processed datasets and displayed the corresponding analytical results.
The Flask application also exposes:
/api/summary

for dashboard summary information.
30. Limitations
The following limitations should be considered when interpreting the results.
Public YouTube Metrics
Public YouTube data does not provide all creator-level analytics such as:
- Shares
- Saves
- Retention rate
- Follower changes
for arbitrary public videos.
Therefore, these metrics should not be fabricated or assumed to be available for the public dataset.
The MySQL schema contains these fields because they are required for the broader project design and can be populated when controlled/creator-level analytics are available.
NLP Classification
Relatability and problem-awareness classification currently use keyword and phrase-based rules.
Therefore, these classifications are estimates and can contain false positives or false negatives.
A/B Testing
The current A/B dataset contains experiment design variables but does not contain sufficient performance outcomes for statistical significance testing.
Therefore, no definitive A/B winner is claimed.
Machine Learning
The dataset contains only a small number of viral examples.
Therefore:
- Classification metrics are noisy.
- Probability estimates should be interpreted cautiously.
- The model should be retrained with more labeled data for production use.
Trend Forecasting
The current trend dataset contains only a small number of observations and one keyword.
Therefore, the trend analysis represents a preliminary signal rather than a robust long-term forecasting model.
Recommendation Engine
The current recommendation scoring system uses transparent heuristic weights rather than a separately trained recommendation model.
31. Future Scope
The project can be extended by:
- Connecting official creator analytics APIs
- Adding Instagram or other social platforms
- Collecting larger datasets
- Collecting controlled A/B test outcomes
- Using transformer-based NLP models
- Improving relatability classification with supervised learning
- Adding time-series forecasting models
- Increasing the number of trend keywords
- Building personalized recommendations
- Adding automated data refresh
- Deploying the Flask dashboard online
- Adding authentication and user management
- Implementing automated model retraining
- Adding real-time analytics
- Adding automated report generation
32. Conclusion
The Data-Driven Social Engagement Initiative demonstrates how social media data can be transformed into actionable content strategy using data analytics, NLP, statistics, machine learning, trend analysis, and visualization.
The system provides an end-to-end workflow from:
Data Collection
      ↓
Data Validation
      ↓
Data Processing
      ↓
Exploratory Data Analysis
      ↓
NLP Analysis
      ↓
Statistical Analysis
      ↓
Viral Content Analysis
      ↓
Machine Learning
      ↓
Recommendation Engine
      ↓
Trend Analysis
      ↓
Trend-Aware Recommendations
      ↓
Flask Dashboard

The project provides exploratory insights into relatable content, audience response, viral-content characteristics, and emerging topics while clearly documenting the limitations of the current dataset and methodology.
33. Author
Omkar Satpute
Third-Year Electronics & Telecommunication Engineering Student
Areas of Interest
- Data Science
- Machine Learning
- Natural Language Processing
- Data Analytics
- Artificial Intelligence
- Data Visualization
34. Project Status
Data Collection             ✅ Complete
Data Processing             ✅ Complete
EDA                         ✅ Complete
NLP Analysis                ✅ Complete
Statistical Analysis       ✅ Complete
Viral Analysis              ✅ Complete
A/B Experiment Design       ✅ Complete
Machine Learning            ✅ Complete
Recommendation Engine       ✅ Complete
Trend Analysis              ✅ Complete
Trend-Aware Recommendation  ✅ Complete
MySQL Database Schema       ✅ Complete
Flask Dashboard             ✅ Complete
Final Data Validation       ✅ Passed
Documentation               ✅ Complete