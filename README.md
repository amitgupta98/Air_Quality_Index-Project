# Air-Quality-Index-Prediction
Webapp to predict the Air Quality Index of a region given climate conditions.


**Motivation for this project**:\
**Krish Naik's Youtube Channel**



Environment setup:

requirements.txt: needed only for deployment to Heroku (not needed for local) as there were issues with anaconda installation on it.\
requirements-conda.txt: needed for local development as I used conda locally. Run: conda create --name <env_name> --file requirements-conda.txt

For this project, I have followed the whole lifecycle of a Data Science Project.

1. **Data Collection**: (Folder-Web_Scrapping{execute HTML_script.py})\
For this step, I have written a web scrapper that scraps en.tutiempo.net for climate data from 2013 to 2018 and creates a HTML file for each month.
2. **Data Preprocessing**: (Folder-Web_Scrapping{execute Extract_combine.py)\
For this step, I have taken the data from Krish Naik's project as it was from a paid API.\
Reference: https://github.com/krishnaik06/AQI-Project/tree/master/Data/AQI. \
This data contained hourly measurements of AQI.\
This was converted into a dictionary format where the dictionary key is the year and values are the daily AQI values. \
Next, the data in step 1 was combined with data of this step to create a new CSV file.
3. **Data Cleaning**: (Folder-Web_Scrapping{execute Extract_combine.py)\
The CSV file created in step 2 was cleaned to remove null values and improper data. A new resultant CSV file was created.
4. **Feature Engineering and Model Creation**: (execute individual jupyter notebooks)\
Tried various algorithms, like Linear Regression, Lasso and Ridge Regression, Decision Tree Regressor, KNN Regressor, Random Forest Regressor, XGBoost Regressor.\
Random Forest and XGBoost gave best performance. Finally, used XGBoost to perform predictions.

