# Analyzing Covid-19 Deaths in Patients with Different Conditions among Various Counties in the United States of America

As a group project comprising of 2 team memebers, this repository presents the work done by me, moreover there are 2 Jupyter Notebooks uploaded, and it contains analysis performed on Coivd-19 using Pandas dataframes, numpy, regression techniques and No-SQL databases design.

Below is the abstract, detailing about the problem faced and how it will be tackeled thorugh this research.

* Since the spread of Covid-19 virus which has impacted the whole world, dislodging some of the world’s biggest economies to the bottom with no exception of the United States of America, the death rates across America spiked at a tremendous rate therefore causing tremendous loss of life. Thus such an impact around the world has been a motivation for the research, so as to evaluate the covid-19 mortality among various counties with patients suffering under various conditions such as some patients have septic, influenza and many other moreover finding the probable cases so as to predict the mortality rates of the region, which can help the counties to take measures to avoid such an outcome.

* The study aims to analyze various patients’ under different categories of their respective health status. The research in the topic helped to generalize the data in a more efficient manner so as to analyze the Covid deaths across various counties moreover exploring new insights in the hidden data such as number of probable deaths, new cases, updated probable deaths, identifying different age groups and their corresponding symptoms.

# ETL Process described below:

![image] (https://github.com/neil996/Database-and-analsytics-programming/blob/main/images/etl.PNG)

* Data Extraction Process: The data is processed is done using ETL method i.e. Extract, Transform and Load. ETL is a powerful system through which data can be stored and transformed for example applying some calculations , joining, grouping, filtering, etc. in an efficient manner. At present ETL is mutating at a rapid growth as more and more data is generating each day as evident with Amazon Redshift and Google Big Query . These tools provide functionalities to transform and analyze the results without shifting the data to any staging area. In the four distinct datasets related to Covid-19, the data has been extracted from different sources, transformed and then loaded in PostgreSQL database for later usage i.e. finding patterns and making predictions.

1. Extraction: This is the phase where data from various sources is gathered and processed in the staging area. As staging provides various advantages such as it reduces the performance issue that would be faced if the data would be directly migrated to Data Warehouse as shifting data directly to a central data warehouse could result in unwanted circumstances such as data getting corrupted and thus making a rollback would be a challenge. Thus the data from individual sources is first stored in Mongo DB then followed by pre-processing the same data in Python Notebook and then finally migrating the entire data suite to Azure PostgreSQL.

2. Transformation: It is the second step in ETL (Extraction, Transformation and Load). We have mainly used Python for the purpose of Transformation. From different datasets we have removed unwanted columns which are not required for our analysis. After this next step we have checked in all the data frames if any Null value present as we must remove them for the proper analysis of our datasets. In our cases we have used imputation methods to remove “NA” or “NULL” like replacing NA values by Median. We have Chosen Median as the percentage of Missing Values is 15 percent. Finally, we have used Group by function to do analysis on Covid 19 datasets, like getting the Top 3 state in U.S.A with most no of Covid19 deaths.


3. Warehousing: We have used PostgreSQL hosted on Azure as a warehouse database because of the following reasons.
- It’s an Open Source Database Management System (D.B.M.S)
- Its best suited for Complex queries which have high I/O and involves lot System resources.

4. Research Findings:
The Research Question aimed to answer is “Predicting the probable new cases along with evaluating current new cases in different counties across United States of America.”
The combined datasets are imported from PostgreSQL using Python and on basis of the pre-processed and cleaned data, Machine Learning algorithm and Visualizations on the combined datasets are done which gave interesting insights on the grouped data, such as plotting the Total cases vs. New Cases on a scatter plot, it was observed that between 0 to 1.25 Million cases, the number of new cases tend to be clustered and not increasing at a rapid rate, but as the total number of cases are increasing the number of new cases are increasing moderately as shown in the scatter plot.


