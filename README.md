# Per_Scholas Data Engineering Capstone_350
 ##Per_Scholas Data Engineering Final Capstone 2024
 This project contains all files related to the submission of the Data Engineering Capstone 350 in July of 2024. The primary goal of this capstone project entails the extraction of credit card transaction, cutomer, branch, and loan data from various datasets. The raw data requires extensive data cleaning (as described below) at which point the data can be loaded into a database.  In addition, the project includes a detailed analysis of the data, including several data visualizations, as well as a front-end console user interface application for interaction with the data.

 ## Primary Objectives
1. Extract data from 3 customer related datasets, clean data, and load into a database.  The datasets cover Credit Card Transactions, Bank Branch information, and Customer information.  Tools used to meet objective 1 include:
   * PySpark for extracting and cleaning
   * MySQL database
2. Build a front-end python based Menu console application to find customer data and modify that data in the database, if necessary, based on menu commands entered by the front-end user.
   * MySQL connector library
   * PrettyTable library
3. Provide visualizations that perform the following tasks:
    * Calculate and plot which transaction type has the highest transaction count
    * Calculate and plot top 10 states with the highest number of customers
    * Calculate the total transaction sum for each customer based on their individual transactions. Identify the top 10 customers with the highest transaction amounts (in 
        ** python libraries
        ** Tableau
4. Pull Loan Application data from an API (https://raw.githubusercontent.com/platformps/LoanDataset/main/loan_data.json) endpoint and store it in the database
   * python libraries
   * PySpark SQL
   * MySQL database
5. Provide visualizations that provide analysis using loan data loaded in step 4: 
   * Calculate and plot the percentage of applications approved for self-employed applicants. Use the appropriate chart or graph to represent this data.
   * Calculate the percentage of rejection for married male applicants. Use the ideal chart or graph to represent this data
   * Calculate and plot the top three months with the largest volume of transaction data. Use the ideal chart or graph to represent this data
   * Calculate and plot which branch processed the highest total dollar value of healthcare transactions. Use the ideal chart or graph to represent this data
        ** python libraries
        ** Tableau


## Requirements to run this repo
* The requirements.txt file contains all the python libraries needed to run this project.  
* The pyspark 3.4 library requires installation of spark on your system for the library to function. If necessary for proper functioning, the my-sql connector needs to be installed in the jars subfolder
* The credentials.py file contains the information needed to log into the MySQL db.  Adjust these credentials as per your own specific use case.
## Notes about the files in this repo
* The files with a leading number (1-5) corresspond to the nubmers outlined in the Main Objections section above.
* The source data directory contains the 3 datasets I was suplied with (files preceeded by cdw).  The area_codes.json file contains the cleaned up area code data that I used to generate the area codes for the customer's phone numbers.  The full_area_code_dataset.zip is the full area code dataset in a zipped up form because it was too big to be uploaded to github in its raw state.  The states.geojson file contains the US states geo data for use in the folium data visualization (section 3).
* The clean data directory contains the datasets after they had been transformed and cleaned in step 1.
* The cc_db.sql contains the sql script to create and populate the entire MySQL database that I created and loaded during the steps in this project.
* Credentials.py contains the login information for the MySQL database.  It isn't included in the repo because it contains sensitive information.  You will have to create your own credentials.py file with this format:
```
host_name = xxxxxx (for example, localhost was mine)
user_name = xxxxxx
password = xxxxxx
port = xxxxxx
```