# COVID-19 Detection from Chest CT Scans
This web application allows users to upload a 2D chest CT scan image to determine whether it is affected by COVID-19. The detection is performed using a pre-trained deep learning model.

## License
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Features
- Simple and User-Friendly Interface: Upload an image directly via the web app.
- Efficient Detection: Utilizes a trained VGG-based ensembled deep learning model for accurate predictions.
- Real-Time Results: Get instant feedback on the uploaded scan.

## Technologies Used
- Backend: Flask (Python)
- Frontend: HTML, CSS, and JavaScript
- Machine Learning Framework: TensorFlow, Keras
- Model: Ensembled VGG model (VGG.h5)

## Requirements
Before running the application, ensure you have the following installed:
```
Python 3.7+
TensorFlow 2.x
Flask
NumPy
```


## Setup Instructions
1. Clone the Repository
```
git clone https://github.com/your-repo/covid-detection-webapp.git
cd covid-detection-webapp
```
2. Install Dependencies
Use the following command to install the required Python libraries:
```
pip install -r requirements.txt
```
Note: Ensure your environment includes TensorFlow, Keras, Flask, and other required libraries.

4. Add the Trained Model - Place your pre-trained model (VGG.h5) in the Model/ directory.

5. Start the Flask Server - Run the app.py file to start the server:
```
python app.py
```
5. Open the Web Application
Once the server is running, open your browser and navigate to:
```
http://127.0.0.1:5000/
```
## Project Structure

```
.
├── Model/
│   └── VGG.h5               # Pre-trained deep learning model
├── templates/
│   └── base.html            # Base template
│   └── index.html           # Main web page
├── uploads/                 # Temporary storage for uploaded images
├── static/                  # Static files (CSS, JS, images)
├── app.py                   # Flask application
├── requirements.txt         # Python dependencies
└── README.md                # Documentation
```


## Usage
- **Go to the Web Page in your browser.**
  ![Image](/Demo/MainPage.png)
- **Upload a chest CT scan in .png, .jpg, or .jpeg format.**
  ![Image](/Demo/UploadImage.png)
- **Click the "Predict!" button to analyze the image.**
- **The result will display whether the scan is COVID-19 Positive or Negative.**
  ![Image](/Demo/Result.png)
- **For any kind of support click on the `Help` button at the top right corner of the page.**
  ![Image](/Demo/DemoHelp.png)


## Notes
- Ensure the uploads/ folder is writable by the server.
- Remove unused files in the uploads/ directory for better storage management.
- The model is trained on specific datasets. Accuracy may vary on unseen data.

## Acknowledgments
For this project I have used the trained model from the paper cited below. We also thankful to the developers of TensorFlow and Keras for providing excellent tools for deep learning.
```
@article{biswas2021prediction,
  title={Prediction of COVID-19 from chest CT images using an ensemble of deep learning models},
  author={Biswas, Shreya and Chatterjee, Somnath and Majee, Arindam and Sen, Shibaprasad and Schwenker, Friedhelm and Sarkar, Ram},
  journal={Applied Sciences},
  volume={11},
  number={15},
  pages={7004},
  year={2021},
  publisher={MDPI}
}
```
