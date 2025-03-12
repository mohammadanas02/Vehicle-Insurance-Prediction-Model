# Vehicle-Insurance-Prediction-Model

This project covers the end-to-end demonstration of a robust pipeline for managing vehicle insurance data. It integrates machine learning and MLOps best practices to predict whether a vehicle owner is likely to purchase insurance based on various attributes. The entire ML lifecycle, from data preprocessing to model deployment, is implemented, ensuring a scalable and efficient prediction service.

## Key Features

- **End-to-End ML Pipeline**: Covers the complete workflow, including data ingestion, preprocessing, model training, and deployment.
- **MLOps Integration**: Implements industry-standard MLOps methodologies to streamline model lifecycle management.
- **Real-time Predictions**: Uses FastAPI to serve the model and provide instant insurance purchase predictions.

## Technology Stack

- **ML Framework**: Scikit-learn for model training and evaluation.
- **Pipeline Management**: Structured pipelines for data processing, training, and prediction.
- **MLOps Tools**: Docker for containerization, FastAPI for model serving, and separation between training and inference phases.
- **Backend Framework**: FastAPI exposes the ML model.
- **Web Server**: Uvicorn ASGI server runs the FastAPI application.

## Problem Statement

This project aims to predict whether a vehicle owner will purchase insurance based on key factors, such as:

- **Demographic Data**: Gender, age, etc.
- **Driving History**: Driving license status and past insurance claims.
- **Vehicle Characteristics**: Vehicle type, damage history, and ownership details.

## Project Features

- **Trainable ML Model**: Supports retraining of the model with updated data.
- **API-based Predictions**: Users can submit vehicle details to receive predictions.
- **Deployment with FastAPI**: Ensures real-time inference using a lightweight web framework.

## ML & MLOps Workflow

### 1. Data Processing
- Data is ingested, cleaned, and transformed for high-quality training.
- Missing values are handled, and categorical variables are encoded.

### 2. Model Training
- The model is trained using Scikit-learn and evaluated using accuracy, precision, and recall.
- Training pipeline automation allows triggering model retraining via an API endpoint.

### 3. Prediction Pipeline
- The trained model accepts user inputs and returns insurance purchase predictions.
- The prediction service is integrated with FastAPI for real-time accessibility.

### 4. Deployment & MLOps
- The model and API service are packaged and deployed using Docker.
- The containerized application ensures consistent deployment across environments.
- CI/CD pipelines can be integrated for automated retraining, validation, and deployment.

## Installation

### Clone the repository:
```bash
git clone https://github.com/yourusername/Vehicle-Insurance-Predictor.git
cd Vehicle-Insurance-Predictor
```

### Install dependencies:
```bash
pip install -r requirements.txt
```

### Run the application locally:
```bash
uvicorn app:app --host 0.0.0.0 --port 8000
```

### Alternatively, run it in a Docker container:
```bash
docker build -t insurance-predictor .
docker run -p 8000:8000 insurance-predictor
```

### Access the application at:
[http://localhost:8000](http://localhost:8000)

## API Endpoints

### 1. `/train` (GET)
- Triggers model training using the latest dataset.
- Automates the training process for easy retraining when required.

### 2. `/` (GET & POST)
- **GET**: Displays a form where users can input vehicle details.
- **POST**: Accepts user-submitted data and returns a prediction (Yes/No) based on the trained model.

## Project Structure

```
📂 Vehicle-Insurance-Prediction-Model
│── app.py             # FastAPI application exposing model APIs
│── analysis/          # Exploratory Data Analysis (EDA) scripts
│── config/            # Data validation and schema configurations
│── src/
│   ├── components/    # Data ingestion, transformation, validation, and model-related scripts
│   ├── configuration/ # AWS and MongoDB integration configurations
│   ├── constants.py   # Configuration constants
│   ├── pipeline/      # Data processing, model training, and prediction pipelines
│── templates/         # HTML templates for frontend
│── static/            # CSS and static assets for the web interface
```

## MLOps Features

### Model Training Pipeline
- Automates data preprocessing, model training, and evaluation.
- Saves the trained model for use in prediction services.

### Model Deployment (FastAPI)
- Serves the trained model as a REST API.
- Provides real-time predictions through a simple user interface.

### Dockerization
- The entire application is containerized using Docker.
- Ensures seamless deployment and eliminates environment-related inconsistencies.

This project follows a structured ML workflow and MLOps practices, ensuring a scalable and maintainable system for vehicle insurance prediction.

 
