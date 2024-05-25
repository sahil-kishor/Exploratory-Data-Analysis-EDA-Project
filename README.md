# Google Play Store Apps : Exploratory Data Analysis (EDA)

![image](https://github.com/sahil-kishor/Exploratory-Data-Analysis-EDA-Project/assets/159517524/311fef32-1728-4b50-9005-e474d5d60674)


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

- **App**	: Name of the Application, Unique Identifier.

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

5. Exploratory Data Analysis :- Plotted the dependent variable and analyzed the distributions of both dependent and independent variables. Checked and visualized the correlation between the dependent and independent variables, and explored the relationships between each pair of variables through various visualization techniques.

## Insights on The Google Play Store Apps Datset Analysis:

- Almost 93% of the apps in Play Store are Free. Only 7% of the apps a paid.

- Most of the Paid Apps have Rating around 4.

- As the number of installation increases the number of reviews of the particaular app also increases.

- Most of the Apps are light-weighted.

- People are preffering free aps more over the paid apps as the free apps have more number of intalls.

- The Family, Games and Tool category of apps are the most available ones in playstore. Whereas, Comics and Beauty related apps are least in the playstore.

- Game, Communication and Tools categories has the highest number of installs compared to other categories of apps.

- Kimbrough AH, CL Strength, Selfie with Champion AJ Style are some Highly rated apps with Rating of 5 out of 5.

- CB Mobile Biz, Lottery Ticket Checker - Florida Results & Lotto, FE Mechanical Engineering Prep are some lowest rated apps with a rating of 1 out of 5.

- We can Also concludde that lowest rated apps have the minimum rating of 1 and highly rated apps have the maximum rating of 5.

- Subway Surfers, Candy Crush Saga, Temple Run 2 are some Highest installed apps in the Game Category.

- Google Play Games, Pou, Taking Tom are the mostly installed apps in the Family Category.

  

## *User Review for Apps Datset:-*

- **App** : Name of the App on the Google Play Store, Unique Identifier.
  
- **Translated_Review** : Text column containing diccriptive User Review.

- **Sentiment** : Whether the Sentiment is Possitive or Negative by the Users.

- **Sentiment_Polarity** : Measures the positivity or negativity of a text, ranging from -1 (negative) to +1 (positive).

- **Sentiment_Subjectivity**  : Indicates the degree of personal opinion or factual information in a text, ranging from 0 (objective) to 1 (subjective).

## Tasks Performed: 

1. **Importing Data** :- Imported the dataset into Google Colab notebook and converted into a Pandas dataframe using Pandas Library.

2. **Data Cleaning** :- There were a Huge amount of Null Values found in the User review Datasets. Except the App column all the columns had arround 42% of Null Values. Looking into it I found that all these null values are wrong and it may have got here due to some error so all of them were dropped together.

3. Exploratory Data Analysis :- Plotted the dependent variable and analyzed the distributions of both dependent and independent variables. Checked and visualized the correlation between the dependent and independent variables, and explored the relationships between each pair of variables through various visualization techniques.

## Insights on the User Review Dataset:

- Positive reviews are 64%, Negative reviews are 22%, Neutral reviews are 14%.

- Helix Jump, Duolingo, Calorie Counter are some Apps having highest Possitive Sentiments.

- Angry Birds, Candy Crush, Bowmaster are some Apps having highest Negative Sentiments.

- There is a Storng Possitive Co-Relation between Reviews and Install Columns. This means higher the number of installs, Higher is the user base and so the number of reviews are also higher, irrespective of wether the reviews are positive or negative

- A Negative correlation between Ratings and Installs indicates that the relationship between these two variables is not straight-forward. Users consider multiple factors when deciding which applications to install, and a lower rating does not necessarily prevent installs, while a higher rating does not guarantee more installs.

- There is a Negative correlation between Price and Ratings/Reviews/Installs which suggests that consumers may feel that higher-priced products less favorably in terms of value. However, the Positive correlation between Price and Sentiment porality/ Sentiment Subjectivity suggests that higher-priced products may be associated with more positive perceptions or sentiments, possibly due to perceived quality or prestige.


## Challenges & Future Work: 
- Our major challenge was data cleaning.

- 13.60% of reviews were NaN values, and even after merging both the dataframes, we could not infer much in order to fill them. Thus we had to drop them.

- The merged data frame of both play store and user reviews, had only 816 common apps. This is just 10% of the cleaned data, we could have given more valuable analysis, if we had atleast 70% - 80% of the data available in the merged dataframes.

- User Reviews had 42% of NaN values, which could have been used for developing an understanding of the category wise sentiments, which would help us to fill 13.60% NaN values of the Reviews column.

- There is so much more which can be explored. Like we have current version, android version available which can be explored in detail and we can come out with more analysis where we can tell how does these things effect and needs to be kept in mind while developing app for the users.

- We can explore the correlation between the size of the app and the version of Android on the number of installs.

- Machine learning can help us to deploy more insights by developing models which can help us interpret even more better. We have left this as future work as this is something where we can work on.


## Conclusion:

In this project of analyzing play store applications, we have worked on several parameters which would help AlmaBetter to do well in launching their apps on the play store.
In the initial phase, we focused more on the problem statements and data cleaning, in order to ensure that we give them the best results out of our analysis.

Google Play needs to focus more on:

- Developing apps related to the least categories as they are not explored much. Like events and beauty.

- Most of the apps are Free, so focusing on free app is more important.

- Focusing more on content available for Everyone will increase the chances of getting the highest installs.

- They need to focus on updating their apps regularly, so that it will attract more users.

- They need to keep in mind that the sentiments of the user keep varying as they keep using the app, so they should focus more on users needs and features.

- Percentage of free apps = ~92%

- Percentage of apps with no age restrictions = ~82%

- Most competitive category: Family

- Category with the highest average app installs: Game

- Percentage of apps that are top rated = ~80%

- Family, Game and Tools are top three categories having 1906, 926 and 829 app count.

- Tools, Entertainment, Education, Buisness and Medical are top Genres.

- 8783 Apps are having size less than 50 MB. 7749 Apps are having rating more than 4.0 including both type of apps.

- There are 20 free apps that have been installed over a billion times.

- Minecraft is the only app in the paid category with over 10M installs. This app has also produced the most revenue only from the installation fee.

- Category in which the paid apps have the highest average installation fee: Finance

- The median size of all apps in the play store is 12 MB.

- The apps whose size varies with device has the highest number average app installs.

- The apps whose size is greater than 90 MB has the highest number of average user reviews, ie, they are more popular than the rest.

- Helix Jump has the highest number of positive reviews and Angry Birds Classic has the highest number of negative reviews.

- Overall sentiment count of merged dataset in which Positive sentiment count is 64%, Negative 22% and Neutral 13%.


## Author

Sahil Kishor

Project : https://github.com/sahil-kishor/Exploratory-Data-Analysis-EDA-Project/blob/main/Copy_of_Capstone_Project_1_Exploratory_Data_Analysis.ipynb 

Email : kishorsahil555@gmail.com

LinkedIn : www.linkedin.com/in/sahil-kishor
