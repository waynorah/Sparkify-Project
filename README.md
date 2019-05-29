# Sparkify-Project

The original size of the dataset is 12GB which is too large for my preliminary analysis, I used the small dataset (128MB) to perform data exploration process.

After doing EDA, I created the below features for later modeling part.

- artist: the number of artists
- gender: 0 or 1
- length: the total length
- level: 0 or 1
- page: the number of Thumbs Up / Thumbs Down
- song: the number of songs

I have used three machine learning models:

- Logistic Regression
- Random Forest classifier
- GBT classifier

As a result of the imbalanced dataset (`Churn` users are extremely few), 

Even Logistic Regression predicted zeros (`Not Churn`) for all the users and gives me F1 score 0.732. 

I decided to use this score as a baseline, and better scores than this baseline are necessary for further modeling.

Testing three machine learning models and Random Forest gives me the best score which is 0.738. 

According to the below feature importance provided by the Random Forest model, `Thumbs Up` and `Thumbs Down` seem to be important while the level of the users do not really matter.

