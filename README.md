# Making healthcare easy, accurate, and efficient for all
Accessing medical care should be simple and accessible to all, but that isn't the case for a lot of the world. Whether it be poorer communities in developed countries or entire nations, there is an estimated 400 million people who don't have access to healthcare services, which should be a basic human right.

The SDGs this project is focusing on are SDG 3: good health and wellbeing and SDG 10: reduced inequalities. The goal is to create a model that will be able to identify diseases based off of symptoms to have this kind of software (essentially a virtual doctor) on one's phone or something just as accessible and accurate.

## What does the system do
### The model
The model takes in symptoms as an input and identifies what disease it is. After classifying what type of disease a person has, this will be outputted to be used for other purposes.

The model has an accuracy of 96% meaning it is generally very accurate at identifying diseses based on symptoms. The model is a machine learning random forrest model, and is trained off of data from this source https://www.kaggle.com/datasets/itachi9604/disease-symptom-description-dataset?select=dataset.csv, and has been cleaned to have 3 symptoms for each patient with that disease. It has a total of 41 diseases and 133 symptoms. Note that the symptoms are coded into numbers for the sake of the model, but with the code provided the given symptom should be converted to a integer.

## Development Process
I followed a standard development process with this model's creation, first cleaning, train test splitting, running it through a classifier, and testign accuracy. I chose a random forrest classifier as I tested a few other models (decision tree and KNN), and this one had the highest accuracy.

Something to be careful of and a potential change in the future is that the dataset provided 17 possible symptoms to be put in, but many only had 3-5 symptoms inputted. I was thinking of finding a way to rank severity of the symptoms as that was provided, but I wasn't able to find a clear way to do that, so I ended up dropping all columns with null values.

## Uses of the model + Future work
### Uses
Initially I had two ideas of using this model.

1. My first idea was as a mobile app for simple diagnosis. It would be similar to a first step of punching your symptoms into Google but significantly more accurate and with less fake news. This is beneficial because it can help a lot of people who don't have the time or money to go to a hospital or doctor's office, and this app may work as a digital hospital where patients punch in their symptoms and depending on confidence of the diagnosis of disease, doctors can respond virtually with help or the app can reccomend nessecary treatments. Ideally, this would make a lot of healthcare much more accessible, but it is important to note this would likely be for less severe diseases with simpler over the counter treatments. I tried to do this with a downloaded model in JavaScript (just putting the model in) but I was unsuccessful. 

2. My second idea was to use this model in a emergency response situation. It would work in conjunction with a vitals tracking machine (heart rate, blood pressure, etc) and a person's medical history to diagnose what an incoming ER patient has and will need. Doctors have a very difficult job of having to remember thousands of potential diseases and their symptoms and diagnosing a person based off of this internal knowledge. This model is capable of doing this same thing with less error and much faster, and in an ER situation, the first response and knowing what to do is neccesary. I don't have the medical knowledge or equipment to make this happen, but to do so would be a really interesting next step.

The model can be downloaded via this Github repository to be used and tested. 

## Improvements
The dataset I had needs to be considered further (note the 17 symptoms comment from earlier), and it only had 41 diseases, so if there was a dataset with more diseases and symptoms, that would make the project much better.

## List of References
https://www.kaggle.com/datasets/itachi9604/disease-symptom-description-dataset?select=dataset.csv
https://www.worldbank.org/en/news/press-release/2015/06/12/new-who-and-world-bank-group-report-shows-that-400-million-do-not-have-access-to-essential-health-services-and-6-of-population-tipped-into-or-pushed-further-into-extreme-poverty-because-of-health-spending#:~:text=Who%20We%20Are-,New%20WHO%20and%20World%20Bank%20Group%20Report%20Shows%20that%20400,Poverty%20because%20of%20Health%20Spending
https://sdgs.un.org/goals
