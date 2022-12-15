# Project_Elixir
This project mainly provides details of all the Diseases, Drugs, Hospitals and the Diagnosis details of the patient. It includes data gathering from various data sources, which includes data repositories, web scraping using BeautifulSoup and twitter scraping utilizing Twitter API. A detailed audit is made using Pandas Profiling.


Project Description:
This project mainly provides details of all the Diseases, Drugs, Hospitals and the Diagnosis details of the patient. It includes data gathering from various data sources, which includes data repositories from various sites, web scraping using BeautifulSoup and twitter scraping utilizing Twitter API. The gathered data is preprocessed according to the database structure and schema. A detailed audit of the data sources is made using Pandas Profiling. Preprocessed the database using python scripts and normalization is done for all the tables.

GitHub: https://github.com/nikhil-enni/Project_Elixir.git

Audit:
Please find the visualized audit report of the data sources gathered in the python notebook 
Diagnosis Data :
Relevancy: The data should meet the requirements for the intended use.

Comments: Data created by the Elixir team to manage the functioning of Hospitals in a professional and optimal manner.

Completeness: The data should not have missing values or miss data records.

Comments: 
Bed Grade                            	 113
City_Code_Patient                   4532
   
Above are empty value counts for bed grade and city_code _patient. 
city_code_patient: Filling with "null" value 
Bed Grade: Filling with mean value of bed grade 
                
Consistency: The data should have the data format as expected and can be cross reference-able with the same results.
    
Comments: 
Age and Stay have interval values
 	Age - Mean of the interval taken
Stay - Mean of the interval taken

Hospitals
Relevancy: The data should meet the requirements for the intended use.

Comments: This dataset is provided by the Homeland Infrastructure Foundation-Level Data (HIFLD) without a license and for Public Use.

Completeness: The data should not have missing values or miss data records.
 
Comments: 
        		TTL_STAFF: Have constant value -999.        
            	Diagnosis - We have dropped the column as there is no information in TTL_STAFF

WEBSITE: 377 ARE NOT AVAILABLE. 
Diagnosis: Mode Imputation will lead to wrong websites to hospitals. So filled null values with empty string.

Consistency: The data should have the data format as expected and can be cross reference-able with the same results.
 
Comments: Data format is as needed to directly join with diagnosis data. No preprocessing is done.

Drugs:

Relevancy: The data should meet the requirements for the intended use.

Comments: This dataset is created from web scraping of various health websites 

Completeness: The data should not have missing values or miss data records.

Comments: There are no missing values in diseases-drugs data. 

Consistency: The data should have the data format as expected and can be cross reference-able with the same results.

Comments: Data format is as needed to directly join with diagnosis data.No preprocessing is done.


Elixir Twitter Bot:

​​Description:
This twitter bot which is a python script, scrapes the data utilizing Twitter API. The bot essentially extracts the Tweets related to Diseases, Drugs and Hospitals, this also stores the user information like user name, user handle, twitter joining date, followers count etc. associated with the Tweets that were extracted. Additional feature of this bot is to store the tags used by the users to Tweet in Twitter. One important functionality is to add a sentiment score to all the tweets, by this it would be possible to know the user's opinion on the medicines and hospitals. Extraction is done on the basis of the details stored in the Diseases, Drugs and Hospitals table. All the extracted details are committed in the Database used using a python script. Below are the details that are being scrapped from Twitter.

Below are the data fields that were scrapped using Twitter API
Tweet Details:
Tweet ID
Twitter Handle 
Tweet
Tweet creation date
Retweet count
Likes count 

User Details:
User ID
User Name
User Handle
User Profile Picture link
Followers Count

Tag Details:
Tag Name

Sentiment score:
Sentiment score of all the tweets are calculated
score>0 implies positive opinion
score<0 implies negative opinion 
score=0 implies neutral opinion

Steps followed: 
Created problem statements by considering a real world problem, that is hospital management and drug distribution which involves Hospitals, Drugs, Diseases, Patients, Diagnosis and public opinion from twitter. 
Scrapped the twitter data using Twitter API and collected data like tweets, usernames, user handles, twitter tags, likes and followers count. 
Gathered data repositories from various medical data sources to use this while scraping and also to construct the database.
And also gathered some data fields using Beautiful Soup
A detailed audit is done utilizing Pandas Profiling to get a clear understanding of the data and to clean the database.
Preprocessed the data frames to fit into the desired database structure and schema.
Removed all the empty values and replaced with nulls
Changed the intervals into mean values, to make it convenient for the constructed queries
Removed all the unwanted data fields which don't add value to the project in the interest of storage.
Connection to a database is made and all the data is loaded to the SQL tables. 
Normalized the end database
Maintained unique values and atomicity. Every table has a primary key.
No partial dependency of the data fields 
No transitive dependency of the data fields
Provided result set for all the use cases using SQL queries. 

Code: 
Please refer to the below link for the well commented python scripts, 

Scripts for:
Twitter Bot 
Audit report
Preprocessing of the data 

GitHub: https://github.com/nikhil-enni/Project_Elixir.git
