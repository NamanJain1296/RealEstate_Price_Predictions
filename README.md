# Real Estate Price Prediction

This project is an end-to-end implementation of a machine learning-powered real estate price prediction system. It provides a user-friendly interface for users to input property details and receive price predictions based on a trained machine learning model. The project demonstrates the seamless integration of data preprocessing, machine learning, and web development technologies.

---

## Features

1. **Price Prediction**:
   - Predicts property prices based on user inputs such as location, square footage, number of bedrooms, and bathrooms.
   - Uses a trained regression model to ensure accurate predictions.

2. **Interactive Web Interface**:
   - Developed with Flask and Bootstrap for a responsive and intuitive experience.
   - Allows users to input property details and receive real-time results.

3. **Data-Driven Insights**:
   - Analyzes property data to identify trends and key pricing factors.
   - Feature importance ranking included for better understanding of the model.

4. **Deployment-Ready**:
   - Can be deployed on cloud platforms like AWS, Azure, or Heroku.
   - Includes configurations for local testing and cloud deployment.

---

## Technology Stack

### Frontend
- **HTML5**: Markup for creating the structure of the web application.
- **CSS3**: Styling for a visually appealing interface.
- **JavaScript**: Added interactivity, including dynamic form validation.

### Backend
- **Python (Flask)**: Lightweight web framework to handle API requests and serve web pages.

### Machine Learning
- **Scikit-learn**: For implementing regression models.
- **Pandas & NumPy**: Data cleaning and manipulation.
- **Matplotlib & Seaborn**: Visualizations for data exploration.

---

## Dataset

### Overview
- **Source**: Kaggle (Bangalore House Price Data)
- **Size**: ~13,000 records
- **Features**:
  - **Independent Variables**: Location, Square Footage, Number of Bedrooms, Bathrooms, Balconies
  - **Dependent Variable**: Price (in Lakhs)

### Data Preprocessing
- Removed duplicates and irrelevant records.
- Handled missing values by imputation.
- Normalized numerical data to a standard range.
- Performed one-hot encoding for categorical data (e.g., location).

### Feature Engineering
- Extracted meaningful features from textual inputs (e.g., splitting "3 BHK" into bedrooms and bathrooms).
- Eliminated outliers using the IQR method to improve model accuracy.

---

## Machine Learning Model

1. **Algorithm**: Linear Regression
   - Chosen for its simplicity and interpretability.
   - Hyperparameter tuning was conducted to optimize performance.

2. **Performance Metrics**:
   - **R-squared**: 0.85
   - **Mean Absolute Error (MAE)**: 2.1 Lakhs
   - **Root Mean Squared Error (RMSE)**: 3.7 Lakhs

3. **Model Pipeline**:
   - Data Cleaning -> Feature Engineering -> Model Training -> Validation.

4. **Model Export**:
   - Trained model exported as a `.pkl` file for integration with the Flask application.

---

## Application Architecture

```
Frontend (HTML/CSS/JS) → Flask Backend → ML Model → API Response → User Interface
```

### Flow
1. User inputs property details on the web app.
2. Backend sends the inputs to the machine learning model.
3. Model processes the inputs and returns a predicted price.
4. Flask app displays the result on the web interface.

---

## Installation

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/real-estate-price-prediction.git
   cd real-estate-price-prediction
   ```

2. Install required libraries:
   ```bash
   pip install -r model/requirements.txt
   ```

3. Run the Flask app:
   ```bash
   python main.py
   ```

4. Open a browser and visit:
   ```
   http://127.0.0.1:5000
   ```

---

## Screenshots

### Homepage
![Homepage](https://via.placeholder.com/800x400?text=Homepage+Screenshot)

### Prediction Results
![Results](https://via.placeholder.com/800x400?text=Prediction+Results+Screenshot)

---

## Deployment

To deploy this application on a cloud platform:

1. **Heroku**:
   - Create a `Procfile` with the following content:
     ```
     web: gunicorn main:app
     ```
   - Use the Heroku CLI to deploy the app.

2. **AWS**:
   - Package the app as a Docker container.
   - Deploy on AWS Elastic Beanstalk or EC2.

3. **Azure**:
   - Use Azure App Services to upload and configure the Flask app.

---

## Future Enhancements

- **Integration with a Database**: Store user input and predictions for later analysis.
- **Model Optimization**: Explore advanced regression techniques like XGBoost or Random Forest.
- **Mobile-Friendly Design**: Enhance the frontend to improve usability on smartphones.
- **Additional Features**:
  - User authentication and profile management.
  - Visualization tools for market trends.

---


---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
