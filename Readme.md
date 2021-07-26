# Speech Recognition System for the Urdu Language

An Automatic Speech Recognition System (ASR) is used to convert the Audio Data or Speech into Text. In this System, Speech Recognition is implemented for the Urdu Language.


## Flask API

We have designed developed an API that accepts an audio file (wav) as input and returns transcript (text) that can be embedded in any third-party Application. Here is the link of API.
 
[API-Link](https://fyp-project-7888.herokuapp.com/predict-api)

## Web Interfaces

A simple HTML page is designed by using Bootstrap and CSS that prompts the user to input an audio file and return the predicted text in a model displaying the selected audio file as well as google API response for comparison. For the demo click on the following link.
 
[Web-App](https://fyp-project-7888.herokuapp.com)

## Mobile Application

An Android Application using Flutter Framework is designed and integrated with the API mentioned above. Mobile Application is consists of three Tabs.

* Model Predictions (with microphone)
* Comparison with Google API (with file chooser)
* Instructions

## Machine Learning Model

Our Model is similar to Deep Speech 2 architecture. It has two main neural network modules - N layers of Residual Convolutional Neural Networks (ResCNN) to learn the relevant audio features, and a set of Bidirectional Recurrent Neural Networks (BiRNN) to leverage the learned ResCNN audio features. The model is topped off with a fully connected layer used to classify characters per time step.

## Deployment of Model and Flask API on Heroku
For the deployment of the Speech Recognition Model and Flask API we have chosen the Heroku Platform. Following are the steps for Deployment.

### Design Template
Create an HTML file to accepts the inputs from the user and handle outputs.

### Create requirements.txt File

```bash
pip freeze > requirements.txt
```

### Create Procfile

```bash
web: gunicorn app:app
```

### Upload on GitHub
Create a new repository and push the Project code to GitHub.
 
### Connect Heroku to GitHub
Create a new app and connect your GitHub repository to Heroku. 


## Installation
Following Libraries are used in Project Development that can be installed using [pip](https://pypi.org/project/pip/)
 
```bash
cffi==1.14.5
click==8.0.1
colorama==0.4.4
Flask==2.0.1
gunicorn==20.1.0
itsdangerous==2.0.1
Jinja2==3.0.1
MarkupSafe==2.0.1
numpy==1.21.0
pycparser==2.20
scipy==1.7.0
SpeechRecognition==3.8.1
torch==1.9.0+cpu
torchaudio==0.9.0
typing-extensions==3.10.0.0
Werkzeug==2.0.1
```

## Routes

```python
# Route to handle HOME
@app.route('/')

# Route to handle PREDICTED RESULT
@app.route('/predict',methods=['POST'])

# API Route
@app.route('/predict-api',methods=['POST'])
```

## Contributing
Free Access to API (without any authentication) is available for third-party applications that will assist users to get a better experience in voice typing (speech recognition).

## Contact
For any query or further assistance approach us using the following links.

[Muhammad Ibtesam Arshad](https://www.facebook.com/muhammadibtesamarshad)

[Hamza Safdar](https://www.facebook.com/codeflirty)