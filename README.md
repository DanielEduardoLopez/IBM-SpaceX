# **IBM-SpaceX**

<p align="center">
	<img src="Images/1-Header.png?raw=true" width=80% height=80%>
</p>

This repository stores the Jupyter notebooks, datasets and the final report of the Applied Data Science Capstone from the **[IBM Data Science Professional Certificate](https://www.coursera.org/learn/applied-data-science-capstone?specialization=ibm-data-science)**.

____
### **1. Introduction**
SpaceX offers Falcon 9 rocket launches with a cost of 62 million dollars while other providers cost upward of 165 million dollars each. A significant amount of the savings is due to SpaceX's ability to reuse the first stage. 

In this context, the main goal of the present study is **to predict the first stage landing of the SpaceX Falcon 9 rocket launch** by using a classification model in order to determine the cost of a launch.

Furthermore, it is also desirable to obtain other insights from the SpaceX Falcon 9 rocket launches.

____
### **2. Objective**
To predict the first stage landing of the SpaceX Falcon 9 rocket launches by using a classification model in order to determine the cost of a launch.

____
### **3. Question**
Will the first stage of the SpaceX Falcon 9 rocket land successfully? 

____
### **4. Abridged Methodology**
1) **Analytical approach**: Classification model with machine learning.
2) **Data requirements**: Historical launching data, including information such as Flight Number, Payload Mass, Launch Site, Orbit, Success Rate, among others.
3) **Data collection:** Data was collected through calls to the SpaceX's API and web scraping to the Wikipedia's article on List of Falcon 9 and Falcon Heavy launches with Python and its libraries such as Requests and BeautifulSoup. Data covers a time period from **2010-04-06 to 2020-06-12**. 
4) **Data exploration:** An exploratory data analysis (EDA) was performed by means of visualization using Matplotlib and SQL. 
5) **Data preparation:** A process of data wrangling was performed using Pandas and Numpy in order to filter the data to the Falcon 9 launches only, imputing missing values with the mean, creating the landing outcome labels; as well as selecting the features for modeling and obtaining dummy variables for the categorical variables.
6) **Data analysis:** Data then was analyzed using SQL in Python. 
7) **Data visualization:** An interactive visual analysis using Folium, Plotly, and Dash was carried out by creating a Dashboard.
8) **Data modeling:** A predictive analysis was performed by means of a Classification Model using Scipy and Scikit-learn. To do so:
- Data was split in a training and test sets.
- The model was built by using several machine learning techniques: Logistic Regression, Support Vector Machines (SVM), Decision Trees and - K-Nearest Neighbors (KNN).
- The models were tuned by using GridSearchCV, in which several parameters were tested, and the data was cross-validated in a 10-fold scheme.
- The best model was selected based on the criteria of outcome of the confusion matrix, precision, recall, f1-score and accuracy.
9) **Reporting:** A final report was written with the complete results obtained from the analysis.

___
### **5. Main Results**
CCAFS SLC 40 is the most used Launch Site and the VAFB SLC-4E is the least used one. Furthermore, KSC LC-39A is the launch site with the highest number of successful missions and it is notable that the success rate has improved over the years as represented by the Flight number (0 for failed landing and 1 for successful landing).

<p align="center">
	<img src="Images/2-LaunchSite_vs_FlightNumber.png?raw=true" width=95% height=95%>
</p>

In addition, CCAFS SLC 40 and KSC LC-39A are used for a broad range of payload masses, from light to extra heavy ones, whereas VAFB SLC-4E is only used for light and medium payloads, which might explain why is the less used launch site. The missions also tend to be more successful with heavier payloads.

<p align="center">
	<img src="Images/3-LaunchSite_vs._Payload.png?raw=true" width=95% height=95%>
</p>

ES-L1, GEO, HEO and SSO are the orbit types with the highest success rates (100%). SO is the orbit type with the lowest success rate (0%). And the rest of the orbit types have a success rate ranging from 50% to 85%.

<p align="center">
	<img src="Images/4-OrbitSuccessRate.png?raw=true" width=50% height=50%>
</p>

LEO, ISS, PO, GTO and VLEO are the most common orbit types. 

EO, PO, GTO and VLEO are less common in recent flight numbers.

VLEO is the most common orbit type in recent flight numbers.

Earlier flight numbers show a tendency to fail regardless of the orbit type.

<p align="center">
	<img src="Images/5-OrbitType_vs_FlightNumber.png?raw=true" width=95% height=95%>
</p>

Heavier payloads are selected for VLEO, IS and PO orbit types and have a high rate of success.

It appears that ES-L1, SSO and HEO are used with light payloads (from 0 to 4000 kg) and have a high rate of success.

The rest of the orbit types are used with light and medium payloads (from 0 to 7000 kg).

<p align="center">
	<img src="Images/6-OrbitType_vs_Payload.png?raw=true" width=95% height=95%>
</p>

Definitely, the launch success rate have improved over the years. In particular, the success rate have improved since 2013, from 0% to an 80% in 2017. And since 2017, it appears that the success rate has stabilized in about 80%.

<p align="center">
	<img src="Images/7-SuccessRateOverTime.png?raw=true" width=50% height=50%>
</p>

Launch sites are located on the coasts and close to the Ecuador.

<p align="center">
	<img src="Images/8-LaunchSitesLocalization.png?raw=true" width=50% height=50%>
</p>

As mentioned above, the Vanderberg (VAFB SLC-4E) Launch Site is the least used and its number of successful landings is fairly low.

<p align="center">
	<img src="Images/9-VAFB.png?raw=true" width=50% height=50%>
</p>

The Cape Canaveral (CCAFS LC-40 and CCAFS SLC-40) is the most used Launch Site, even though its number of failed landings is slightly superior to the its number of successful landings.

<p align="center">
	<img src="Images/10-CCAFS.png?raw=true" width=50% height=50%>
</p>

The Kennedy Space Center (KSC LC-39A) has the highest number of successful missions. Nonetheless, it is not the most used Launch Site.

<p align="center">
	<img src="Images/11-KSC.png?raw=true" width=50% height=50%>
</p>

KSC LC-39A is 6.46 KM far from the Atlantic Sea, and 72.21 KM far from Orlando, FL.

<p align="center">
	<img src="Images/12-KSC_Distances.png?raw=true" width=50% height=50%>
</p>

Indeed, the Highest Launch Success Ratio is hold by the KSC LC-39A launch site, with a 76.9% of success and only 23.1% of failure.

<p align="center">
	<img src="Images/13-KSC_SuccessRate.png?raw=true" width=95% height=95%>
</p>

The payload range(s) with the highest launch success rate was from 1952 kg to 5300 kg.

<p align="center">
	<img src="Images/14-PayloadRangeSuccess.png?raw=true" width=95% height=95%>
</p>

The FT and the B5 Booster versions were the ones with the highest launch success rate.

<p align="center">
	<img src="Images/15-F9BoosterSuccess.png?raw=true" width=95% height=95%>
</p>

The model with the highest classification accuracy was the one built with **Decision Trees** with an accuracy of **88.9%**, when fitted with the following best parameters: 

```bash
{'criterion': 'gini', 
'max_depth': 2, 
'max_features': 'sqrt', 
'min_samples_leaf': 1, 
'min_samples_split': 2, 
'splitter': 'best'} 

```

<p align="center">
	<img src="Images/16-AccuracyModels.png?raw=true" width=50% height=50%>
</p>

Moreover, the confusion matrix suggests that the built model is better at predicting successful landings than unsuccessful landings. So, there is room for improvement in terms of reducing both false positives and false negatives.

<p align="center">
	<img src="Images/17-ConfusionMatrix.png?raw=true" width=50% height=50%>
</p>

In spite of the above, this results suggest that, indeed, most of the launches from SpaceX will land successfully. 

___
### **6. Dashboard**
To view and play with the interactive Dashboard, please download the **[app](https://github.com/DanielEduardoLopez/IBM-SpaceX/blob/main/7-spacex_dash_app.py)** into a directory of your choice. Then, run the app using the following command in Windows:
```bash
python 7-spacex_dash_app.py
```
And visit http://127.0.0.1:8050/ in your web browser.

<p align="center">
	<img src="Images/Dashboard.jpg?raw=true" width=65% height=65%>
</p>

Please note that Python 3 and its libraries Numpy, Pandas, Dash and Plotly are required for properly running the dashboard.

___
### **7. Main Conclusions**
The classification model built with **Decision Trees** was the one that exhibited the highest accuracy, with an score of **88.9%**. Moreover, the outcome of the model indicated that **most of the launches from SpaceX will land successfully**. 

On the other hand, analysis from the historical launching data suggested that SpaceX has gotten better at launching and its **success rate** has stabilized since 2017 in **about 80%**.

Thus, the present study suggests that the **cost of the Falcon 9 rocket launches** should be set at **62 million dollars**, as stated by SpaceX.

Other insights obtained from the present analysis were:
- **KSC LC-39A** is the launch site with the highest number of successful missions and **VAFB SLC-4E** is the one with the lowest. 
- **ES-L1, GEO, HEO** and **SSO** are the orbit types with the highest success rates (100%) but with a small number of missions. On the other hand, **VLEO** is the most common orbit type in recent years.
- The payload range with the highest launch success rate is **from 1952 kg to 5300 kg**.
- **FT** and **B5** are the booster versions with the highest launch success rate.


____
### **8. Description of files in repository**
| **File** | **Description** |
| ------------- | ------------- |
| **1-Spacex-data-collection-api.ipynb** | Notebook for collecting the required data from SpaceX API using Requests. |
| **2-Webscraping.ipynb** | Notebook for collecting the required data from Wikipedia using BeautifulSoup.
| **3-Spacex_Data_wrangling.ipynb** | Notebook for cleaning and exploring the data using Numpy and Pandas.
| **4-EDA_sql_sqllite.ipynb** | Notebook for querying the data using SQL using Sqlite3 and Sqlalchemy.
| **5-EDA_dataviz.ipynb** | Notebook for exploring visually the data and performing Feature Engineering using Matplotlib, Seaborn and Pandas.
| **6-Folium_Launch_site_location.ipynb** | Interactive notebook with maps built with Folium.
| **6-Folium_Launch_site_location.html** | Interactive report from the latter on HTML version.
| **7-spacex_dash_app.py** | Code for setting up an interactive dashboard using Plotly and Dash.
| **8-SpaceX_Dashboard.ipynb** | Report with screenshoots with insights from the dashboard.
| **9-SpaceX_Machine Learning Prediction.ipynb** | Notebook for building the classification models with Scikit-learn.
| **10-Capstone-Project-Final-Report.pptx** | Power Point slides with the full results and insights obtained in the present study.
| **10-Capstone-Project-Final-Report.pdf** | PDF version of the latter.
| **dataset_part_1_DEL.csv** | Data set created from the calls to API SpaceX.
| **spacex_web_scraped.csv** | Data set created from the web scraping to Wikipedia's article on List of Falcon 9 and Falcon Heavy launches.
| **dataset_part_2_DEL.csv** | Data set created after Data wrangling.
| **spacex_launch_dash.csv** | Dataset created for the Dash app.
| **dataset_part_3_DEL.csv** | Dataset created after the Feature Engineering process.

<p align="center">
	<img src="Images/18-Tail.png?raw=true" width=80% height=80%>
</p>
