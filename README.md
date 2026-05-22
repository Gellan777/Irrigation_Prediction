# 🌱 Irrigation Prediction System
# 📌 Overview

This project is a Machine Learning-based Irrigation Prediction System that predicts the irrigation requirement level of crops as Low, Medium, or High based on environmental and agricultural conditions.

The system helps farmers and agricultural decision-making by providing intelligent irrigation insights using data-driven predictions.

# 🚀 Project Objective

To build a classification model that can accurately predict irrigation needs using features such as:

Temperature
Humidity
Soil Moisture
Rainfall
Sunlight Hours
Crop type & growth stage
Irrigation history and more
# 🧠 Machine Learning Approach
Model Type: Deep Learning (Neural Network using Keras)
Problem Type: Multi-class Classification
Classes:
Low
Medium
High
# ⚙️ Feature Engineering

Advanced feature engineering was applied to improve model performance:

Temp_Humidity = Temperature × Humidity
Water_efficiency = Soil_Moisture / Previous_Irrigation
Moisture_Temp = Soil_Moisture × Temperature
Rain_per_Sun = Rainfall / Sunlight_Hours
Humidity_per_Temp = Humidity / Temperature
# 🧹 Data Preprocessing
Handling categorical features using:
One-Hot Encoding
Ordinal Encoding
Scaling numerical features using StandardScaler
Train/Validation split with stratification
Class imbalance handled using class_weight
# 🏗️ Model Architecture
Input Layer → Features after preprocessing
Dense Layers:
128 units (LeakyReLU + Dropout)
128 units (L2 Regularization + Dropout)
64 → 32 → 16 neurons
Output Layer:
3 neurons (Softmax)
# 🛠️ Training Configuration
Optimizer: Adam (lr = 0.0005)
Loss Function: Sparse Categorical Crossentropy
Batch Size: 64
Epochs: 150
Callbacks:
EarlyStopping
ReduceLROnPlateau
# 📊 Model Performance
Validation Accuracy: ~97.7%
Strong performance across all classes:
Low: ~0.99 F1-score
Medium: ~0.97 F1-score
High: ~0.88 F1-score
# 📈 Visualizations

The project includes extensive EDA:

Correlation heatmap
Boxplots for feature analysis
Distribution plots
Scatter plots between key variables
Target class distribution
Outlier detection plots
# 📁 Project Structure
├── train.csv
├── test.csv
├── model_training.ipynb
├── submission.csv
├── README.md
# 📤 Output

The model generates a prediction file:

submission.csv

Containing:

id
Irrigation_Need (Low / Medium / High)
# 💡 Key Highlights
Strong feature engineering improved model accuracy
Balanced learning using class weights
Robust preprocessing pipeline using ColumnTransformer
High performance deep learning classifier
# 🔧 Libraries Used
NumPy
Pandas
Scikit-learn
TensorFlow / Keras
Matplotlib
Seaborn
# 📌 Future Improvements
Try ensemble models (XGBoost / LightGBM)
Hyperparameter tuning (Optuna / Keras Tuner)
Deploy as Flask / FastAPI web app
Add real-time sensor integration
# 👩‍💻 Author

Gellan Romany
Machine Learning Developer
