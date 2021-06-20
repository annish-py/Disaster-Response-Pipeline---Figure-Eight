## Disaster Response Pipelines
### Table of Contents


<a href="#intro">1. Project Motivation

<a href="#desc">2. Project Description

<a href="#files">3. File Descriptions

<a href="#install">4. Installations

<a href="#execute">5. Execution

<a href="#author">6. Authors

<a href="#images">7. Data Visualizations

<a href="#results">8. Results   

<a href="#license">9. Acknowledgement and License


<a id='intro'></a>
## 1. Project Motivation

This Project is one of the Data Science Nanodegree Program of [Udacity](https://www.udacity.com/school-of-data-science) in collaboration with [Figure Eight](https://appen.com/) to build a model for an API that classifies disaster messages.. The  data-set contains pre-labelled tweet and messages from real-life disaster situations.
The goal of the project is to classify the disaster messages into categories. In this project, I analyzed disaster data from  Through a web app, the user can input a new message and get classification results in several categories. The web app also display visualizations of the data.

<a id='desc'></a>
### 2. Project Description

The project has three componants which are:

#### ETL Pipeline: [process_data.py](https://github.com/Suveesh/Disaster-Response-Pipeline/blob/main/data/process_data.py) file contain the script to create ETL pipline which:

- [x] Loads the messages and categories datasets.
- [x] Merges the two datasets
- [x] Cleans the data
- [x] Stores it in a SQLite database

#### ML Pipeline: [train_classifier.py](https://github.com/Suveesh/Disaster-Response-Pipeline/blob/main/model/train_classifier.py) file contain the script to create ML pipline which:

- [x] Loads data from the SQLite database
- [x] Splits the dataset into training and test sets
- [x] Builds a text processing and machine learning pipeline
- [x] Trains and tunes a model using GridSearchCV
- [x] Outputs results on the test set
- [x] Exports the final model as a pickle file

#### Flask Web App: the web app enables the user to enter a disaster message, and then view the categories of the message.

- [x] The web app also contains some visualizations that describe the data.

<a id='files'></a>
### 3. Files Descriptions

#### The files structure is arranged as below:

- README.md: read me file
- Project Components.txt: Project requirements to complete
- workspace
	- \app
		- run.py: flask file to run the app
	- \templates
		- master.html: main page of the web application 
		- go.html: result web page
	- \data
		- disaster_categories.csv: categories dataset
		- disaster_messages.csv: messages dataset
		- DisasterResponse.db: disaster response database
		- process_data.py: ETL process
	- \models
		- train_classifier.py: classification code
		- MLclassifier.pkl: model pickle file
		
	- \Pipeline Preparation
		- ETL Pipeline Preparation.py
		- ML Pipeline Preparation.py
		
<a id='install'></a>
### 4. Installations

All libraries are available in Anaconda distribution of Python. The used libraries are:

- pandas, re, sys, json, pickle
- sklearn, nltk
- sqlalchemy, sqlite3
- flask

The code should run using Python versions 3.*.

<a id='execute'></a>
### 5. Execution

To execute the app follow the instructions:

   Run the following commands in the project's root directory to set up your database and model.
        To run ETL pipeline that cleans data and stores in database python 'data/process_data.py data/disaster_messages.csv' 'data/disaster_categories.csv' 'data/DisasterResponse.db'
        To run ML pipeline that trains classifier and saves python 'models/train_classifier.py' 'data/DisasterResponse.db' 'models/classifier.pkl'

   Run the following command in the app's directory to run your web app. python run.py

   Go to http://0.0.0.0:3001/ (or) http://127.0.0.1:5000/ (Based on ur machine IP config)
   

<a id='author'></a>
### 6. Authors
   - [Annish Prashanth](https://github.com/annish-py)

<a id='images'></a>
### 7. Data Visualizations
![image1](https://github.com/annish-py/Disaster-Response-Pipeline---Figure-Eight/blob/main/workspace/newplot.png)
![image2](https://github.com/annish-py/Disaster-Response-Pipeline---Figure-Eight/blob/main/workspace/newplot%20(1).png)
![image3](https://github.com/annish-py/Disaster-Response-Pipeline---Figure-Eight/blob/main/workspace/newplot%20(2).png)
![image4](https://github.com/annish-py/Disaster-Response-Pipeline---Figure-Eight/blob/main/workspace/newplot%20(3).png)
![image5](https://github.com/annish-py/Disaster-Response-Pipeline---Figure-Eight/blob/main/workspace/newplot%20(4).png)


<a id='results'></a>
### 8. Results
When a disaster message is submitted to the Disaster Response Pipeline and the Classify Message button is invoked, the app shows how the outcomes it classified by highlighting the categories in green. 
For example for the message "We have nothing here and urgently require clean water, food, clothes, doctors, medicines and tents for shelter" 
The outcome we get are the following categories: 'Request', 'Aid Related', 'Food', 'Water', 'Medical', 'Medical Products', 'Shelter'
![image6](https://github.com/annish-py/Disaster-Response-Pipeline---Figure-Eight/blob/main/workspace/Result.PNG)

<a id='license'></a>
### 9. License and Acknowledgement:
   Thanks to [Udacity](https://www.udacity.com/school-of-data-science) - Data Science Nano Degree and to [Figure Eight](https://appen.com/) for providing messages dataset to train the model.


[![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html)

  ##### Contact Me at [LinkedIn](https://www.linkedin.com/in/annishprashanth/)