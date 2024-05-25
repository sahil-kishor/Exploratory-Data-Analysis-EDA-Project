# Google Play Store Apps : Exploratory Data Analysis (EDA)

## Problem Statement:

Google Play Store or Play Store for Android Market, is a digital distribution service operated and developed by Google. It serves as the official app store for certified devices running on the Android. The Play Store apps data has enormous potential to drive app-making businesses to success. Actionable insights can be drawn for developers to work on and capture the Android market. Each app (row) has values for category, rating, size, and more. Another dataset contains customer reviews of the android apps. Explore and analyse the data to discover key factors responsible for app engagement and success. This project aims to conduct EDA and extract insights from app data using python and understand user sentiments towards Play Store Applications.

## Dataset Description:

![image](https://github.com/sahil-kishor/Exploratory-Data-Analysis-EDA-Project/assets/159517524/4a3e714a-f9ad-428d-9cfc-34cb26be7726)

## Main Libraries to be used:

- Pandas for data manipulation, aggregation
- NumPy for computationally efficient operations
- Matplotlib and Seaborn for visualisation and behaviour with respect to the target variable. Use at least 5 different visualisations.

## Project Architecture:

![image](https://github.com/sahil-kishor/Exploratory-Data-Analysis-EDA-Project/assets/159517524/18a2a2e0-99be-471e-8ef4-77d19a9fe4d4)

## *Google Play Store Apps Datset:-*

- **App**	: Name of the Application.

- **Category** : Category in which the App belongs.

- **Rating** : Overall rating of the App given by the Users.	

- **Reviews** : Number of reviews given by the Users.

- **Size** : The total size of the App, i.e, the amount of space it will reqire on a device.	

- **Installs** : The total number of times the Apps have been installed by the users across various devices.	

- **Type** : Describes whether the app is Free or Paid.	

- **Price**	: If the App is of a Paid type then the corresponding amount and if the app is Free then 0.

- **Content Rating** : Decrribes what category of Audience is the App ment for.

- **Genres** : The Genre of the App.

- **Last Updated**	: When was the last update given for the Apps to the users by the Play Store.

- **Current Ver**	: The Current Version of the App that is available on the Play Store with all the latest updates.

- **Android Ver** : The Android version on the devices which is required for the Application to be installed, run and function.

## Tasks Performed:

1. **Importing Data** :- Imported the dataset into Google Colab notebook and converted into a Pandas dataframe using Pandas Library.

2. **Data Cleaning** :- There were a significant amount of Null Values found in the Google Play Store Apps Datasets
   - Rating has 1465 null values which contributes 14.14% of the data. Handled by Imputing the values with the Median value of the column.
   - The 'Type' column contains 1 null value, representing 0.01% of the data. This null value was addressed by replacing it with 'Free,' as it constituted a negligible percentage of the dataset. Additionally, the corresponding 'Price' column value was '0,' indicating that these were indeed free apps.
   - Current_Ver has 8 null values which contributes 0.07% of the data. Handled by Dropping it as it was in a very less percentage.
   - Android_Ver has 3 null values which contributes 0.03% of the data. Handled by Dropping it as it was in a very less percentage.
   - Content_Rating has 1 null value which contributes 0.01% of the data. After all these process, this column was ultimately cleaned.

3. **Data Wrangling** :- Several columns had incorrect data types, so I converted them to the appropriate formats as needed to ensure accurate analysis.
   - Changed the datatype of the Last Updated column from string to datetime.
   - Converted the datatype of the Price column from string to float and removed the Dollar sign($).
   - Converted the values in the Installs column from string datatype to integer datatype and dropped the Plus(+) sign with it.
   - Changed the values in the Size column to a same unit of measure(MB).
  
4. Data Exploration-Univariate & Bivariate Analysis :- Pair plot is used to understand the best set of features to explain a relationship between two variables or to form the most separated clusters. It also helps to form some simple classification models by drawing some simple lines or make linear separation in our data-set.



