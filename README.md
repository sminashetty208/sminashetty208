🌿 EcoDriveAI+: Intelligent Driving Behavior and Energy Optimization System

---
🚗 Overview
EcoDriveAI+ is an intelligent system designed to enhance the energy efficiency of electric vehicles (EVs) by combining predictive analytics, behavioral classification, and route optimization. The project uses real-world Tesla and EV datasets to build models that:

Predict energy consumption based on driving patterns.

Classify driving behavior (eco-friendly vs. aggressive).

Simulate smart route recommendations.

---

🎯 Problem Statement
With EV adoption increasing, optimizing energy consumption and promoting sustainable driving are essential. Traditional GPS systems often ignore driver behavior and dynamic battery usage. EcoDriveAI+ aims to address this gap with:

Predictive models for energy use.

Behavioral insights for eco-driving.

Optimization algorithms for route planning.

---

📊 Data Description
Two datasets are used:

Tesla Driving Logs: Includes vehicle speed, acceleration, steering, brake pressure, and battery status.

General EV Dataset: Features environmental conditions, driving behavior, and battery usage.

---

🧹 Data Engineering & Preprocessing
Selected relevant features such as speed, acceleration, SOC, voltage, etc.

Renamed columns for clarity and consistency.

Removed missing values and reset indices.

Standardized and normalized data for model input.

---

🧠 Model Implementation
Three core models were developed:

Regression Model: Predicts energy consumption (Wh/km).

Classification Model: Categorizes driving behavior.

Clustering & Route Optimization: Uses KMeans to group driving patterns and suggest energy-efficient routes.

Each model uses:

Scikit-learn (RandomForest, KNN, etc.)

Deep Learning (ANN via TensorFlow/Keras)

PCA & clustering techniques for high-dimensional data

---

🔬 Experimental Section
Tested 10+ configurations with varying architectures and hyperparameters.

Evaluated using validation scores (not test accuracy) to prevent data leakage.

Applied cross-validation for reliable performance metrics.

---

📈 Results & Evaluation
Visualized model performance through loss curves, confusion matrices, and accuracy plots.

Regression and classification models showed strong generalization.

Clustering revealed distinct driving profiles useful for optimization.

---

🔧 Hyperparameter Tuning
Used GridSearchCV and manual tuning for optimal depth, learning rate, and neuron count.

Applied dropout and batch normalization for regularization.

---

📌 Business Implications
For Drivers: Personalized feedback on driving habits.

For Fleet Managers: Better energy forecasting and routing.

For Manufacturers: Data-driven design improvements.

---

📎 Future Directions
Incorporate real-time GPS and traffic data for live route optimization.

Integrate with mobile or vehicle-based applications.

Expand to hybrid and fuel vehicles for comparative insights.

---

🛠️ Technologies Used
Python, NumPy, Pandas, Matplotlib, Seaborn

Scikit-learn, Keras/TensorFlow

Jupyter Notebook / Google Colab

---

📫 Let's Connect
📧 Email: smina.shetty208@gmail.com
💼 LinkedIn: linkedin.com/in/smina-shetty-a6575126b


