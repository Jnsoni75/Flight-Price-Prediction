# ✈️ Flight Price Prediction using Machine Learning 🤖

Welcome to the Flight Price Prediction project! Our goal is to build a smart regression model that can accurately forecast flight ticket costs. Flight pricing is notoriously complex, influenced by a multitude of factors, so we're using machine learning to unravel these patterns and provide reliable predictions for travelers and industry analysts alike.

## 📊 The Dataset

We're working with a robust and clean dataset of **300,153 flights**, featuring 12 distinct attributes and zero missing values, which provides a solid foundation for our analysis. Here's a look at the data points we're using to train our model:

* **Airline:** 🛩️ The airline company, a key factor in pricing.
* **Flight:** 🎫 The unique flight code.
* **Source City:** 🛫 The city where the journey begins.
* **Departure Time:** ⏰ The time of day for departure, which can heavily influence price.
* **Stops:** 🛑 The number of layovers, from direct flights to multi-stop journeys.
* **Arrival Time:** 🛬 The time of day for arrival at the destination.
* **Destination City:** 📍 The final destination of the flight.
* **Class:** 👑 The travel class (e.g., Economy or Business), a major price determinant.
* **Duration:** ⏳ The total flight duration in hours.
* **Days Left:** 🗓️ How many days before departure the ticket is booked.
* **Price:** 💰 The target variable! This is the flight cost we aim to predict.

## 🚀 Project Workflow

Our project follows a structured approach to ensure a robust and accurate model:

1.  **🔍 Exploratory Data Analysis (EDA):** We dive deep into the data to uncover trends, visualize distributions, and understand the relationships between different features and the final flight price. This helps us identify which factors are most influential.
2.  **🔧 Feature Engineering:** Since machine learning models require numerical input, we transform categorical features like `airline`, `source_city`, and `destination_city` into a machine-readable format using one-hot encoding. This allows the model to interpret text-based data effectively.
3.  **🧠 Model Implementation:** We train and test three different regression models to determine which provides the most accurate predictions. We start with a simple baseline and move to more complex, powerful models:
    * **Linear Regression:** A foundational model to establish a performance baseline.
    * **Random Forest Regressor:** An advanced ensemble model that combines multiple decision trees to improve accuracy and control for overfitting.
    * **Gradient Boosting Regressor:** Another powerful ensemble technique that builds trees sequentially, with each new tree correcting the errors of the previous one.

## 🛠️ How to Use

Ready to run the project yourself? You'll need Python and a few essential libraries.

Install them with pip:
```
pip install pandas scikit-learn matplotlib
```

Once you're set up, you can open and run the `CS4661_Project.ipynb` Jupyter Notebook to follow the complete analysis, from data loading and visualization to model training and evaluation.

## 🏆 Results

We evaluated our models using Mean Squared Error (MSE) and Root Mean Squared Error (RMSE), which measure the average squared difference and the standard deviation of the prediction errors, respectively. In this context, a lower RMSE means the model's predictions are closer to the actual flight prices. Here's how they stacked up:

* **Linear Regression:**
    * MSE: 23,382,925
    * RMSE: 4,835.59
* **🥇 Random Forest Regressor:**
    * **MSE: 3,740,092**
    * **RMSE: 1,933.93**
* **Gradient Boosting Regressor:**
    * MSE: 6,405,011
    * RMSE: 2,530.81

## ✨ Conclusion

The **Random Forest Regressor** was the clear winner! 🏆 With a significantly lower MSE and RMSE, it proved to be the most accurate and reliable model for predicting flight prices in our dataset. This is likely because Random Forest is excellent at capturing complex, non-linear relationships between variables, which are very common in dynamic pricing scenarios like air travel.
