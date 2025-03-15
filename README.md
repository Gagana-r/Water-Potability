This script is a water potability analysis and classification project using machine learning. Below is a breakdown of its key components:

1. Importing Libraries
Standard libraries: numpy, pandas, seaborn, matplotlib.pyplot
Warnings and formatting: warnings, termcolor
Machine learning tools: sklearn (for data preprocessing, model training, and evaluation)
2. Data Loading and Preprocessing
Reads the water_potability.csv dataset.
Displays basic info, summary statistics, and missing values.
Replaces missing values in ph, Sulfate, and Trihalomethanes columns with median values.
3. Data Visualization
Boxplots: Used to visualize the distribution of all features.
Pie Chart: Shows the proportion of potable vs. non-potable water samples.
Correlation Heatmap: Displays feature correlations.
Pairplot: Explores relationships between features with hue='Potability'.
4. Data Splitting and Scaling
Separates features (X) and target (y).
Uses MinMaxScaler to normalize features.
Splits the dataset into training and testing sets (80/20 split).
5. Model Training & Hyperparameter Tuning
The script trains and evaluates four machine learning models:

Logistic Regression

Uses GridSearchCV for hyperparameter tuning.
Best model is selected and evaluated.
Random Forest Classifier

Trained with GridSearchCV tuning.
Uses n_estimators=1000 and log_loss criterion.
MLP (Multi-Layer Perceptron) Classifier

Neural network with 500 hidden units and logistic activation.
K-Nearest Neighbors (KNN)

Tuning done using GridSearchCV with different values of n_neighbors.
6. Model Evaluation
Confusion Matrix: Displays classification performance.
Classification Report: Shows precision, recall, and F1-score.
Bar Chart: Compares accuracy scores of all four models.
7. Final Results
Scores of all models are stored in a DataFrame.
A bar plot visualizes model performance.
