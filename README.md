# Student Performance Indicator

## 📌 Project Overview
The **Student Performance Indicator** is an End-to-End Machine Learning project designed to understand how student performance (test scores) is affected by demographic and background variables such as Gender, Ethnicity, Parental Level of Education, Lunch Type, and Test Preparation Course. This application takes multiple feature inputs and predicts a student's quantitative performance (aimed typically at mathematics score based on correlation with reading and writing skills).

## 🚀 Features
- **End-to-End ML Pipeline**: Seamless integration of Data Ingestion, Data Transformation, and Model Training components.
- **Interactive Web Interface**: A Flask-based web application providing a clean UI for users to test the model with custom inputs.
- **Custom Exception Handling & Logging**: A robust error tracking and logging architecture implemented across the application.
- **Multi-Model Evaluation**: Evaluates multiple state-of-the-art machine learning models (CatBoost, XGBoost, Random Forest, etc.) and auto-selects the best-performing algorithm.
- **Modular Codebase**: Clean, highly scalable, and modular object-oriented project structure.

## 🛠️ Technology Stack
- **Language**: Python 3.8+
- **Machine Learning**: Scikit-Learn, CatBoost, XGBoost
- **Data Manipulation**: Pandas, NumPy
- **Data Visualization**: Matplotlib, Seaborn
- **Web Framework**: Flask
- **Frontend**: HTML5, CSS3

## 📂 Project Structure
```text
.
├── artifacts/                  # Created after running pipelines (contains model.pkl, preprocessor.pkl, raw data, etc.)
├── logs/                       # Stores real-time application and error logs
├── notebook/                   # Jupyter Notebooks for EDA (Exploratory Data Analysis) and model experiments
├── src/                        # Core application source code
│   ├── components/             # Individual pipeline stages
│   │   ├── data_ingestion.py   # Script to extract and split data into train/test sets
│   │   ├── data_transformation.py # Script for feature engineering, scaling, and handling missing data
│   │   └── model_trainer.py    # Script for hyperparameter tuning and training multiple ML models
│   ├── pipeline/               # Orchestration pipelines
│   │   ├── predict_pipeline.py # Handles passing external web inputs to the model for predictions
│   │   └── train_pipeline.py   # Evaluates and trains the overarching end-to-end pipeline
│   ├── exception.py            # Custom exception handling class definition
│   ├── logger.py               # Custom logging configuration
│   └── utils.py                # Helper utility functions for model saving/loading and metric evaluation
├── templates/                  # HTML templates for the Flask application
│   ├── index.html              # Landing page
│   └── home.html               # User Input prediction form UI
├── app.py                      # Flask Application Entry Point
├── setup.py                    # Script to package the project as a python module
└── requirements.txt            # Required python package dependencies
```

## ⚙️ Installation & Usage

1. **Clone the repository:**
   *(Ensure you change to your actual repository directory)*
   ```bash
   git clone <your-repository-url>
   cd "Student Performance Indicator"
   ```

2. **Create and Activate a virtual environment:**
   ```bash
   python -m venv .venv
   
   # On Windows
   .venv\Scripts\activate   
   
   # On macOS/Linux
   source .venv/bin/activate  
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Application:**
   ```bash
   python app.py
   ```

5. **Test the Model:**
   Open your browser and navigate to `http://127.0.0.1:5000/`. Click on the predictions link or navigate directly to `http://127.0.0.1:5000/predictdata` to enter values and see the prediction results.

## 📊 Model Training (Optional)
If you wish to train the models from scratch and generate new `model.pkl` and `preprocessor.pkl` files:
1. You can step through the Jupyter Notebooks located in the `notebook/` directory for an interactive approach.
2. Alternatively, run the data ingestion python script directly. It is configured to automatically trigger the data transformation and model training processes, outputting the freshly trained models into the `artifacts/` folder:
   ```bash
   python src/components/data_ingestion.py
   ```

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page or submit a pull request if you want to improve the codebase.

## 📝 License
This project is licensed under the MIT License.

---
_Author: Ankan_
