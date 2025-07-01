
AI-Driven Product Review Intelligence System
________________________________________
 Project Overview
 
This is an end-to-end AI system that analyzes product reviews to provide:
•	  Rating and helpfulness predictions
•	  Semantic search using Sentence-BERT & FAISS
•	  Visual analytics (sentiment, ratings, word clouds)
•	  Intelligent product recommendations
•	  A/B testing with feedback tracking and logging
•	  Export insights to PDF and CSV
________________________________________
 Dataset
 
•	Source:	https://www.kaggle.com/datasets/karkavelrajaj/amazon-sales-dataset
________________________________________
 Features
 
•	Text preprocessing (cleaning, lemmatization, sentiment analysis)
•	TF-IDF + additional features (review length, sentiment polarity)
•	Rating prediction with XGBoost Regressor
•	Helpfulness prediction with XGBoost Classifier (synthetic labels)
•	Semantic review search with Sentence-BERT + FAISS
•	Hybrid recommendation scoring (sentiment × rating × helpfulness)
•	Interactive dashboard built using Dash
•	Visual analytics including word clouds, sentiment vs helpfulness plots, rating distributions
•	Clickable product cards with summaries
•	Feedback collection for A/B tests
•	Export dashboard insights as PDF/CSV
________________________________________
 How I Built It
 
This project was implemented using Python, Dash, and machine learning tools. Here's what I did and how I did it:
________________________________________
 1. Installed Required Packages
    
•	Dash, XGBoost, Pandas
•	Sentence-Transformers, FAISS
•	WordCloud, TextBlob, NLTK
________________________________________
 2. Data Cleaning and Preprocessing
    
•	Removed duplicates and nulls
•	Cleaned text using regex, stopword removal, and lemmatization (NLTK)
•	Added features:

o	TF-IDF vectors (top 300 terms)
o	Sentiment polarity (TextBlob)
o	Review length
________________________________________
 3. Machine Learning Models
    
•	XGBoost models for:

o	Rating Prediction (regression)
o	Helpfulness Prediction (binary classification with synthetic labels)
•	Performance:

o	RMSE ≈ 0.85 (rating)
o	Accuracy ≈ 75% (helpfulness)
________________________________________
 4. Semantic Search with FAISS
    
•	Used Sentence-BERT to embed all reviews
•	Indexed embeddings with FAISS for fast semantic queries
________________________________________
 5. Dashboard with Dash
    
•	Interactive UI with 3 tabs:

o	Tab 1: Recommender – semantic search + top suggestions
o	Tab 2: Analytics – rating distribution, word cloud, sentiment, sentiment vs helpfulness
o	Tab 3: ML Insights – RMSE, AUC, top products by hybrid score, feedback collection

•	Clickable product cards with summary pop-ups
•	Export insights to PDF and CSV
________________________________________
 6. Hybrid Product Scoring
    
Calculated a custom hybrid score:

hybrid score = sentiment × predicted rating × predicted helpfulness
This ranks the most positively reviewed and helpful products.
________________________________________
 7. Visual Analytics
    
•	Word clouds of frequent review terms
•	Pie chart of rating distribution
•	Bar plots of sentiment vs rating and sentiment vs helpfulness
•	Lists of top/bottom products by average rating and hybrid score
________________________________________
 8. Business Impact
    
The dashboard helps:

•	Shoppers discover trusted products
•	Sellers identify what users love or dislike
•	Businesses monitor customer feedback efficiently
________________________________________
 Conclusion
 
SmartReviewAI delivers an end-to-end solution for intelligent product review analysis. By combining natural language processing, machine learning, semantic search, predictive modeling, and interactive visualization, it transforms unstructured review data into actionable business insights. This system supports better decision-making for both consumers and retailers.
________________________________________
 Strengths
 
•	End-to-end pipeline from data ingestion to dashboard visualization
•	Semantic search powered by Sentence-BERT & FAISS
•	Custom hybrid scoring strategy for better recommendations
•	Clean and interactive Dash UI with clickable product cards
•	Comprehensive visual feedback with word clouds, sentiment plots, and product rankings
•	Scalable and modular architecture
•	A/B testing with feedback tracking and data export options
________________________________________
 Limitations
 
•	Helpfulness labels are synthetic, not real user votes
•	No multilingual review support
•	Sentiment analysis based on TextBlob with limited nuance
•	No deep learning classifiers (e.g., fine-tuned transformers) yet
•	Not deployed on cloud or hosted platforms yet
•	Feedback loop and user interaction logging still basic
________________________________________
 Future Work
 
•	Replace synthetic helpfulness labels with real user feedback
•	Add multilingual review processing
•	Explore deep learning models for classification and sentiment
•	Deploy as SaaS platform with user personalization
•	Expand A/B testing capabilities with richer feedback collection
•	Enhance dashboard with real-time updates and collaborative features


