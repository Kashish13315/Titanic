import pandas as pd
from sklearn.linear_model import LinearRegression

# Load your data
data = pd.read_csv("your_data.csv")

# Define dependent and independent variables
X = data[["independent_variable1"]]  # Assuming one independent variable
y = data["dependent_variable"]

# Create and train the model
model = LinearRegression()
model.fit(X, y)

# Get slope and intercept coefficients
slope = model.coef_[0]
intercept = model.intercept_

# Predict for a new data point (replace with your desired value)
new_x = 10  # Replace with your value for the independent variable
predicted_y = model.predict([[new_x]])[0]
