# Thyroid Cancer Analysis Tool

This is a comprehensive Streamlit web application for thyroid cancer analysis that integrates two distinct prediction methods:

1. **Thyroid Cancer Risk Assessment**: Predicts thyroid cancer risk based on patient clinical data using machine learning models
2. **Thyroid Ultrasound Image Analysis**: Analyzes thyroid ultrasound images to detect potential cancer regions using a YOLO deep learning model

## Features

### Risk Assessment Tool
- Interactive web interface for entering patient data
- Multiple predictive models (Voting Ensemble, Random Forest, Logistic Regression, Decision Tree)
- Risk level assessment with visual gauge
- Feature importance visualization
- Patient-specific recommendations based on risk level

### Image Analysis Tool
- Upload and analyze thyroid ultrasound images
- Detection of potential thyroid cancer regions using YOLO object detection
- Visualization of results with bounding boxes
- Confidence threshold adjustment
- Detection summary and recommendations

## Installation and Setup

### Prerequisites

- Python 3.8 or higher
- Virtual environment (venv)

### Installation

1. Ensure you have Python and virtual environment set up:
   ```
   python -m venv venv
   ```

2. Activate the virtual environment:
   - **Windows**:
     ```
     venv\Scripts\activate
     ```
   - **Mac/Linux**:
     ```
     source venv/bin/activate
     ```

3. Install required packages:
   ```
   pip install -r thyroid/requirements.txt
   ```

## Running the Application

### Windows

Simply double-click the `run_app.bat` file, which will:
- Activate the virtual environment
- Start the Streamlit server
- Open the application in your default web browser

### Manual Start

1. Activate the virtual environment:
   - **Windows**:
     ```
     venv\Scripts\activate
     ```
   - **Mac/Linux**:
     ```
     source venv/bin/activate
     ```

2. Run the application:
   ```
   python run.py
   ```
   
   Or directly with Streamlit:
   ```
   streamlit run thyroid/app.py
   ```

## Using the Application

### Risk Assessment Tool

1. Navigate to the "Thyroid Cancer Risk Assessment" tab
2. Enter patient information in the sidebar:
   - Demographic information (Gender, Age, Country, Ethnicity)
   - Risk factors (Family History, Radiation Exposure, etc.)
   - Clinical measurements (TSH Level, T3 Level, T4 Level, Nodule Size)
3. Select a prediction model from the dropdown menu
4. Click "Predict Risk" to get the results
5. View the prediction results:
   - Diagnosis prediction
   - Risk level assessment
   - Probability percentage
   - Risk visualization gauge
   - Feature importance chart
   - Patient-specific recommendations

### Image Analysis Tool

1. Navigate to the "Thyroid Ultrasound Analysis" tab
2. Upload a thyroid ultrasound image (JPG, JPEG, or PNG format)
3. Adjust the detection confidence threshold if needed
4. Click "Analyze Image" to process the image
5. View the results:
   - Original and annotated images
   - Detection details (class, confidence)
   - Summary of findings
   - Recommendations based on detections

## Model Information

The application uses two types of trained models:

1. **Clinical Data Models** (in `thyroid_cancer_models.pkl`):
   - Trained models (Voting Ensemble, Random Forest, Logistic Regression, Decision Tree)
   - Feature scalers
   - Label encoders
   - Feature column lists
   - Target encoder

2. **Image Analysis Model** (in `best.pt`):
   - YOLOv8 model trained on thyroid ultrasound images
   - Detects regions of potential thyroid cancer

## Disclaimer

This application is intended for educational and research purposes only. It should not replace professional medical advice, diagnosis, or treatment. Always consult with a qualified healthcare provider for medical decisions. 