# Predictive-Price-Modeling-

Predictive-Price-Modeling-
![image](https://user-images.githubusercontent.com/90289879/213088928-e25a08b8-dd86-45a5-af25-829c4c00bf59.png)

The project aimed at predicting the price of an Airbnb listing given a number of features. The project involved exploratory data analysis, data pre-processing, feature selection, Model Fitting, Model Comparison and deploying the containerised Webapp on AWS using CI/CD Pipeline.

Project Goals and Objectives
Problem: Currently there is no convenient way for a new Airbnb host to decide the price of his or her listing. New hosts must often rely on the price of neighbouring listings when deciding on the price of their own listing.

Solution: A Predictive Price Modelling tool whereby a new host can enter all the relevant details such as location of the listing, listing properties, available amenities etc and the Machine Learning Model will suggest the Price for the listing. The Model would have previously been trained on similar data from already existing Airbnb listings.

Project Overview
![image](https://user-images.githubusercontent.com/90289879/213088911-80cb3fb4-611c-43df-8c72-2c46ba1bc8ad.png)

Exploratory Data Analysis: Explore the various features, their distributions using Histograms and Box-plots

Pre-processing and Data Cleaning: Normalisation, filling missing values, encoding categorical values.

Feature Selection: Study the correlation with response variable (Listing Price) and determine which features are most useful in predicting the price.

Model Fitting and Selection: Training different models, tuning hyper-parameters and studying Model performance using Learning Curve.

Model Serving: Using FLASK to deploy and serve Model predictions using REST API.

Container: Using Docker to containerise the Web Application.

Production: Using AWS CI/CD Pipeline for continuous integration and deployment.

About Dataset
The Dataset used in this project was obtained from public.opendatasoft.com. There are a total of 494,954 records each of which contains details of one Airbnb listing. The total size of dataset is 1.89 GB.

The dataset has a large number of features which can be categorised into following types,

Location related: Country, City, Neighbourhood

Property related: Property Type, Room Type, Accommodates, Bedrooms, Beds, Bed Type, Cancellation Policy, Minimum Nights

Booking Availability: Availability 30, Availability 60, Availability 90, Availability 365

Reviews related: Number of Reviews, Reviews per Month, Review Scores Rating, Review Scores Accuracy, Review Scores Cleanliness, Review Scores Checkin, Review Scores Communication, Review Scores Location, Review Scores Value

Host related: Host Since, Host Response Time, Host Response Rate, Calculated host listings count, Host Since Days, Host Has Profile Pic, Host Identity Verified, Is Location Exact, Instant Bookable, Host Is Superhost, Require Guest Phone Verification, Require Guest Profile Picture, Requires License

Amenities: TV, Wireless Internet, Kitchen, Heating, Family/kid friendly, Washer, Smoke detector, Fire extinguisher, Essentials, Cable TV, Internet, Dryer, First aid kit, Safety card, Shampoo, Hangers, Laptop friendly workspace, Air conditioning, Breakfast, Free parking on premises, Elevator in building, Buzzer/wireless intercom, Hair dryer, Private living room, Iron, Wheelchair accessible, Hot tub, Carbon monoxide detector, 24-hour check-in, Pets live on this property, Dog(s), Gym, Lock on bedroom door, Private entrance, Indoor fireplace, Smoking allowed, Pets allowed, Cat(s), Self Check-In, Doorman Entry, Suitable for events, Pool, Lockbox, Bathtub, Room-darkening shades, Game console, Doorman, High chair, Pack ’n Play/travel crib, Keypad, Other pet(s), Smartlock

The price of the listing will serve as labels for the regression task. The goal of this project would be to predict these price of the listings.

Exploratory Data Analysis
To get a better insight into where the listings are located, the number of listings in various cities and countries are plotted in the figure below. In the given dataset, United States has the most number of listings followed by European countries and Australia. In terms of cities, Paris, London, New York, Berlin, Los Angeles are some of the cities with most number of listings.

Airbnb offers three types of listings,

Entire home/apartment
Private Room
Shared Room
Entire home is by far the most popular type of listing offered followed by Private Rooms and then a small share of the total listings are shared rooms.

Number of listings: Country wise
![image](https://user-images.githubusercontent.com/90289879/213088889-0ac1baa0-94f2-438d-a8cb-088b9f15c7d2.png)

Number of listings: City wise (Min 2000)
![image](https://user-images.githubusercontent.com/90289879/213088862-e28aea18-e96a-4957-83a9-b108c89232d7.png)

Number of listings: Room Type
![image](https://user-images.githubusercontent.com/90289879/213088837-4eae4ba5-257a-4b5c-ab01-38f053880efa.png)

Boxplot: Listing Price by Room-type
![image](https://user-images.githubusercontent.com/90289879/213088821-81f370ad-0218-44e3-bc7c-2dcfd00bb334.png)

Boxplot: Listing Price by Country
![image](https://user-images.githubusercontent.com/90289879/213088802-79e31e03-0cb1-46ff-a51b-392092837e02.png)

Boxplot: Listing Price by City
![image](https://user-images.githubusercontent.com/90289879/213088783-1b171a43-ea0d-4969-953c-429398f9f924.png)

Number of people accomodated
![image](https://user-images.githubusercontent.com/90289879/213088764-6bb8c47c-6855-40db-9b70-6a1899698814.png)

Beds
![image](https://user-images.githubusercontent.com/90289879/213088740-0893741a-b09f-42df-97f1-3e9a7e92a771.png)

![image](https://user-images.githubusercontent.com/90289879/213088716-3a8c87e7-ad0e-41f6-bdba-c506bf30747e.png)

Data pre-processing and cleaning
![image](https://user-images.githubusercontent.com/90289879/213088689-77551265-1052-4553-8a9b-b1a525bf4894.png)
