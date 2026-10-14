❤️ Heart Disease Prediction using Machine Learning
A machine learning web application built with Python, Scikit-learn, and Streamlit to predict the likelihood of heart disease from user-provided health measurements.
The app uses a trained K-Nearest Neighbors (KNN) model and a saved scaler to process the input features and generate a prediction.
Disclaimer: This project is for educational and demonstration purposes only. It is not a medical diagnosis tool and must not be used as a substitute for advice from a qualified healthcare professional.

✨ Features
- Interactive web interface built with Streamlit
- Collects health-related inputs such as age, resting blood pressure, cholesterol, maximum heart rate, and other clinical indicators
- Uses a saved KNN model to make predictions
- Applies the saved scaler to input features before prediction
- Displays a simple result indicating the model's predicted heart-disease class
🧰 Tech Stack
- Python — application logic
- Pandas — input data handling
- Scikit-learn — machine learning preprocessing/model ecosystem
- Joblib — loading saved model artifacts
- Streamlit — interactive web application
- Jupyter Notebook — data exploration and preprocessing
📁 Project Structure
HeartDicease-main/
├── app.py
├── KNN_heart.pkl
├── scaler.pkl
├── columns.pkl
└── HeartDiseas/
    ├── heart (1).csv
    └── ̱Heart.ipynb
- app.py — Streamlit user interface and prediction workflow
- KNN_heart.pkl — saved trained KNN model
- scaler.pkl — saved feature scaler used during training
- columns.pkl — expected model input column names and order
- HeartDiseas/heart (1).csv — dataset used for exploration/training
- HeartDiseas/̱Heart.ipynb — notebook for exploratory data analysis and preprocessing
⚙️ Getting Started
1. Clone the repository
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd HeartDicease-main
Replace <YOUR_GITHUB_REPOSITORY_URL> with your repository URL.
2. Create and activate a virtual environment (recommended)
macOS / Linux
python3 -m venv .venv
source .venv/bin/activate
Windows
python -m venv .venv
.venv\Scripts\activate
3. Install dependencies
pip install streamlit pandas scikit-learn joblib
Use a compatible version of scikit-learn for the one used when the model and scaler were saved, because serialized model files can be version-sensitive.
4. Run the application
Make sure you are in the directory containing app.py and the three .pkl files, then run:
streamlit run app.py
Streamlit will display a local URL in the terminal. Open that URL in your browser.
🧠 How It Works
1. The user enters health-related values in the Streamlit interface.
2. The app creates a single-row Pandas DataFrame from the inputs.
3. Missing one-hot encoded feature columns are added with a value of 0.
4. The input is reordered to match the saved training columns in columns.pkl.
5. The saved scaler transforms the input features.
6. The trained KNN model predicts a class.
7. The app displays the prediction result.
🩺 Input Features
The interface asks for the following values:
- Age
- Sex
- Chest pain type
- Resting blood pressure
- Cholesterol
- Fasting blood sugar indicator
- Resting ECG result
- Maximum heart rate
- Exercise-induced angina
- Oldpeak (ST depression)
- ST slope
📊 Prediction Output
The app displays one of two model outputs:
- High Risk of Heart Disease — the model predicted class 1
- Low Risk of Heart Disease — the model predicted class 0
These labels reflect the model's output, not a confirmed medical assessment.
🔮 Future Improvements
- Add model evaluation metrics such as accuracy, precision, recall, F1-score, and confusion matrix
- Validate inputs and handle model-loading or prediction errors gracefully
- Document the dataset source and preprocessing decisions
- Add automated tests and dependency version pinning
- Deploy the application so it can be accessed online
👨‍💻 Author
Siddharth Kushwaha
- GitHub: @siddharth-kushwaha03
- LinkedIn: Siddhartha Kushwaha
If you find this project useful, consider giving the repository a ⭐ on GitHub.
