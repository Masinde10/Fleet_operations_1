# Fleet-operations
#### Author: [Masinde Victor](https://github.com/Masinde10)

## BUSINESS UNDERSTANDING
### Project Overview
This project is designed to help a company manage it`s fleet effectively. The project is developed with the transport department of the said comapny in mind. The comapny has several vehicles that are being managed by the transport department. For the smooth running of the company processes, every department needs to work optimally, transport department included. The project aims at making sure the fleets are utilised in a manner that serves their purpose effectively.

### Problem Statement 
The comapny having a huge fleet, makes it hard to handle and manage them cassually. There needs to be a system that helps to manage the same. The project at hand aims to adress some of the challenges that the department could otherwise face on fleet management. The project aims to do the following. 
1.  Monitor Fuel, maintainance and Insurance expenses for the fleets. This helps us to determine the units that are prooving expensive  to own
2.  Monitor fuel effieciency, Vehicle downtime and maintainace frequencies. This is critical for pinpointing units that are less efficient.
3.  Assess the quality of maintaince products from different suppliers. Spare parts of good quality are more durable and therefore we aim to identify which suppliers and parts are to be ordered.
### DATA UNDERSTANDING
The Data we are using for this project has been sourced from the internet with the help of AI tools. I fed it with instructions of columns that I would like in my dataset and helped refine the values. The data therefore does not represent the real picture on the ground. The dataset has 2000 rows and 14 columns. The columns represent different features such as Vehicle type, part name, supplier, Issue_reported, Fuel_consumed, Cost of ownership etc. From the overall summary of the data, we see Float and Object present as the data type. The numerical columns are 5 while the categorical ones are 9 in total.  
### DATA CLEANING
In this chapter we aim to clean our data before proceeding with analysis. The core focus is checking for null values and duplicates. Null values can be handled by dropping the entire row or by filling them with mean or mode of the column. Duplicates are dropped so as to get the correct represantation of features during analysis. From the code below, we see that we do not have any null values. There are no duplicates in our data too. We can therefore proceed to the next step
### EXPLORATORY DATA ANALYSIS
In this section, we visualize different feature relationships. we aim to uncover the trends our our data at this point. Often, this is where we decide on the model that we will use for our project depending on the results of the visualizations.
![Cost of Ownership Distribution](https://github.com/Masinde10/Fleet_operations_1/blob/main/Images/Cost%20of%20ownership.png)

From the above visualization above, we see that the cost of maintainance is on the average. The Medium Bin is the highest followed by the bin for low cost of maintainance.The goal is to shift the maintanance cost to the lower side.

![Relationship between Fuel consumed and distance travelled](https://github.com/Masinde10/Fleet_operations_1/blob/main/Images/Fuel%20vs%20Distance%20covered.png)

The scatter plot shows that there is a hge relationship between fuel consumed and distance covered. Furthermore, it shows how differnt vehicles behave when it comes to fuel consumption. Motorcycles have the lowest ratio of fuel consumption from the graph. 

![Distribution of units](https://github.com/Masinde10/Fleet_operations_1/blob/main/Images/Units.png)

The visualization above shows the distriutio of different units in the company. Being a sugar mills company, the fleet with the highest number is the tractor fleet, followed by trucks, light vehicle, heavy vehicles and then Motorbikes.


![Distribution of Models](https://github.com/Masinde10/Fleet_operations_1/blob/main/Images/Models.png)

The above visualization goes deeper to give more insights on the fleet visualized earlier. It shows the differentt models present in the different classes of vehicles. 

### MODELLING
After completing exploratory data analysis and getting the charactreistics of our data, We dive into modelling. I chose the baseline model to be a linear regression model since the data showed lots of linear properties. It perfomed well but to exhaust our options, I fitted other different models. I fitted Random forest regressor which perfomed slightly lower than the baseline model. I introduced hyperparamaters and model tuning but still the perfomance was lower. I fitted the Decision Tree classifier which perfomed the worst among all the models. The behaviours of the other models convinced me fully that the data had huge linear properties and therefore went back to improving the baseline moedl. I introduced the lasso penalty which helps in reducing overfitting and setting the coefficients of the less useful features to zero. At the end, those feature with more importance are the ones used for prediction. While fitting the random forest regressor, I checked for feature importance and the results are below. 

![Feature Importance](
