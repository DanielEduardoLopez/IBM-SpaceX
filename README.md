# **IBM-SpaceX**
This repository stores the Jupyter notebooks, datasets and the final report of the Applied Data Science Capstone from the IBM Data Science Professional Certificate (https://www.coursera.org/learn/applied-data-science-capstone?specialization=ibm-data-science).

____
### **Introduction**
SpaceX offers Falcon 9 rocket launches with a cost of 62 million dollars while other providers cost upward of 165 million dollars each. A significant amount of the savings is due to SpaceX's ability to reuse the first stage.

____
### **Objective**
To predict the first stage landing of the SpaceX Falcon 9 rocket launches by using a classification model in order to determine the cost of a launch.

____
### **Question**
Will the first stage of the SpaceX Falcon 9 rocket land successfully? 

____
### **Abridged Methodology**
1) Analytical approach: Classification model.
2) Data requirements: Historical launching data from 2010-04-06 to 2020-06-12.
3) Data was collected through calls to the SpaceX's API and web scraping to the Wikipedia's article on List of Falcon 9 and Falcon Heavy launches with Python and its libraries such as Requests and BeautifulSoup.
4) Data then was prepared and cleaned with Python using Pandas and Numpy. 
5) Data was explored and visualized in Python using Matplotlib.
6) A dashboard was built using Plotly and Dash.
7) Several classification models using Logistic Regression, Support Vector Machines, Decision Trees and K-Nearest Neighbors were built and tuned for predicting whether the SpaceX Falcon 9 rocket will land successfuly or not.
8) A final report was written with the complete results obtained from the analysis.

___
### **Main Conclusions**
The classification model built with **Decision Trees** was the one that exhibited the highest accuracy, with an score of **88.9%**. Moreover, the outcome of the model indicated that **most of the launches from SpaceX will land successfully**. 
On the other hand, analysis from the historical launching data suggested that SpaceX has gotten better at launching and its **success rate** has stabilized since 2017 in **about 80%**.
Thus, the present study suggests that the **cost of the Falcon 9 rocket launches** should be set at **62 million dollars**, as stated by SpaceX.

____
### **Description of files in directory**
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
| **dataset_part_3_DEL.csv** | Dataset created after the Feature Engineering process.

