# Crime Profile based Recommendation Engine for the City of Chicago

`Team` – **Krishna Kumar, Shilpi Jain, Christopher Manley, Kalvin Edwards, Sumit Machwe, Aditya Tadakaluru**

## DESCRIPTION

Neighbourhood safety is crucial for any new homeowner or renter. Many times, an area that is considered safe may or may not be safe for an individual or a group of individuals.
Current apps such as Trulia, Zillow, Crime grade and City Data provide overall general safety rating of a zip code without any personalization i.e., they do not take the factors associated with given user’s profile into account. 
These websites use factors such as school ratings, dwelling attributes and comparable etc. that are limited in scope when it comes to personalization.
Unlike general safety ratings, we want to personalize the safety ratings based on the user's profile i.e., find the areas that are safe or unsafe for an individual associated with specific user profile.

### Project Organization

1. [User Profile Recommender System Needs & Complications.pptx](reports/User%20Profile%20Recommender%20System%20Needs%20&%20Complications.pptx) : Describes user profile and crime profile `Cosine Similarity` alogrithm for recommendation engine.
 
2. [Dashboard](src/dashboard) `CrimeMap.twbx` : Package Tableau Dashboard with descriptive analytics and recommendation engine dashboard.


4. [Data](src/data)
 - `Victim_Profile_Categories_v2.xlsx` : Victim profile attributes
 - `profile_probs.xlsx` : Curated user/crime probablity
 - `ref_class_probs.csv` : User profile probablity distribution for vaious crimes 
   - `ten_user_recommendations.csv` : Final output from recommendation engine to Tableau Dashboard 
   - `user_profilesv3.csv` : Database of user profiles

4. [Notebook](src/notebook)
 - `CrimeDB-FeatureEngineering.ipynb` : Data wrangling and feature engineering of Chicago City crime database (2015 - 2021)
 - `Probability_Mapping.ipynb` : Mappinig user profile to probability distribution of crimes
 - `User_Profile_Recommender_System.ipynb` : User profile based crime succeptability
 - `User_Profile_Simulation.ipynb` : Simulate user profile to be tested by recommendation engine.

5. [scripts](src/scripts)
 - `ref_class_probs_CreateDDL.sql` : Mapping user profile to probability distribution of crimes.

## INSTALLATION
How to install and setup your code
1. Launch python environment and make notebook as default directory
2. Ensure data from below urls are downloaded to /data directory:
   1. Chicago Crime Database: [https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2](https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2)
   2. Chicago IUCR Code Mapping: [https://data.cityofchicago.org/Public-Safety/Chicago-Police-Department-Illinois-Uniform-Crime-R/c7ck-438e](https://data.cityofchicago.org/Public-Safety/Chicago-Police-Department-Illinois-Uniform-Crime-R/c7ck-438e)
   3. Hate Crime DataBase: [https://home.chicagopolice.org/statistics-data/data-dashboards/hate-crime-dashboard/](https://home.chicagopolice.org/statistics-data/data-dashboards/hate-crime-dashboard/) 
   4. ESRI Latitude Longitude Mapping to Zip Code: [https://www.esri.com/en-us/home](https://www.esri.com/en-us/home)
   5. Department of Justice: [https://www.bjs.gov/index.cfm?ty=nvat](https://www.bjs.gov/index.cfm?ty=nvat) and [https://bjs.ojp.gov/data](https://bjs.ojp.gov/data)

    
3. Install Tableau desktop. `Version 2021.3`

## EXECUTION
1. Launch Tableau Desktop and open /dashboard/CrimeMap.twbx