# Crop Recommendation & Yield Prediction System

A machine learning web application that provides crop recommendations based on soil and environmental conditions and predicts agricultural crop yield using historical agricultural data.

## Features

### 1. Crop Recommendation
- Accepts soil nutrient values: Nitrogen (N), Phosphorus (P), and Potassium (K).
- Uses temperature, humidity, soil pH, and rainfall.
- Recommends a suitable crop from 22 crop categories.
- Uses a trained Neural Network model.

### 2. Crop Yield Prediction
- Accepts crop name, year, average annual rainfall, pesticide usage, and average temperature.
- Predicts crop yield using a trained XGBoost regression model.

## Technology Stack

| Category | Technologies |
|---|---|
| Backend | Python, Flask |
| Machine Learning | TensorFlow, Keras, XGBoost |
| Data Processing | Pandas, NumPy |
| Model Utilities | Scikit-learn, Joblib |
| Frontend | HTML, CSS, JavaScript, Bootstrap |
| Development | Jupyter Notebook |

## Project Structure

```text
Project Code/
│
├── app/
│   ├── main.py
│   ├── requirements.txt
│   ├── templates/
│   │   └── index.html
│   ├── model/
│   │   ├── model.py
│   │   ├── recommendation.h5
│   │   ├── recommendation_enc.joblib
│   │   ├── yield.joblib
│   │   ├── yield_item.joblib
│   │   ├── yield_year.joblib
│   │   └── yield.json
│   └── venv/
│
├── ML_model/
│   ├── Crop_recommendation.csv
│   ├── Crop_recommendation2.csv
│   ├── yield_df.csv
│   ├── apy.csv
│   └── crop.ipynb
│
├── static/
│   ├── script.js
│   └── style.css
│
└── README.md

## Machine Learning Models

### Crop Recommendation
- Algorithm: Artificial Neural Network
- Test accuracy: 95.45%
- Test records: 440

### Yield Prediction
- Algorithm: XGBoost Regressor
- MAE: 2476.68
- RMSE: 4147.50
- R2 Score: 0.9981
- Test records: 810

## Installation

Prerequisite: Python 3.11

1. Clone the repository:
   git clone YOUR_GITHUB_REPOSITORY_URL

2. Navigate to the app folder:
   cd app

3. Create a virtual environment:
   python3.11 -m venv venv

4. Activate it:
   source venv/bin/activate

5. Install dependencies:
   pip install -r requirements.txt

6. Run the application:
   python main.py

7. Open http://127.0.0.1:5000 in your browser.

## Notes

- Pre-trained models are stored in app/model/.
- Training notebook and datasets are stored in ML_model/.
- Some model compatibility warnings may appear.
- Flask development server is intended for local testing.

## Future Improvements

- Better input validation.
- Automated application testing.
- Model improvements.
- Cloud deployment.

## License

No license has been specified yet.
