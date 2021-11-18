# Laptop Prices Predictor
<ul>
  <li>Designed a web app that predicts the price of the laptop given the configurations. </li>
  <li>Scraped the laptops data from Laptop_Data.csv .</li>
  <li>Developed Linear Regression ans Descision tree algorithms using R2 to get the best model.</li>
  <li>Deployed the Machine Learning model using streamlit library in Heroku.</li>
</ul>

# Links and Resources Used
<li>Streamlit Library: <a href="https://www.streamlit.io/">https://www.streamlit.io/</a>
<li>Model Deployment Github: <a href="https://github.com/shuvamtracker/Machine-Learning-Projects">https://github.com/shuvamtracker/Machine-Learning-Project</a></li>
<li>Packages: pandas, numpy, sklearn, streamlit, joblib</li>

# Web Scraping

This is the Flipkart website comprising of different laptops. This page contains the specifications of 24 laptops. So now looking at this, we try to extract the different features of the laptops such as:
<ul>
  <li> Company</li>
  <li>TypeName</li>
  <li>Inches</li>
  <li>Screen Resolution</li>
  <li>Ram</li>
  <li>Memory</li>
  <li>Gpu</li>
  <li>Operating System</li>
  <li>Weight</li>
  <li>Price</li>
</ul>
So we extract the data from our dataset now consists of the information the 1304 different laptops. <br>
Link to my dataset: https://github.com/shuvamtracker/Machine-Learning-Project/blob/main/Lap_price_predictor/laptop_data.csv 

# Feature Engineering
We go through all the features one by one and keep adding new features. I have made the following changes and created new variables:
RAM - Made columns for Ram Capacity in GB and the DDR version <br>
Processor - Made columns for Name of the Processor, Type of the Processor, Generation <br>
Operating System - Parsed the Operating System from this column and made a new column <br>
Storage - Made new columns for the type of Disk Drive and the capacity of the Disk Drive <br>
Display - Made new columns for the size of the laptop(in inches) and touchscreen <br>
Description - Made new columns for the company and graphic card <br>

# Data Preprocessing
There are a few columns which are categorical here but they actually contain numerical values.So we need to convert few categorical columns to numerical columns. These are DDR_Version,Generation,Storage_GB,Price.

# Exploratory Data Analysis

![image](https://user-images.githubusercontent.com/88879492/142353425-3d656756-78b3-4f57-87aa-0e90ccbc5c8f.png)
![image](https://user-images.githubusercontent.com/88879492/142353566-fa435aa8-1040-4eff-8bf4-b8581c920c17.png)
![image](https://user-images.githubusercontent.com/88879492/142353633-b2daa11f-6a44-42fa-aca0-4c85aa39623c.png)
![image](https://user-images.githubusercontent.com/88879492/142353700-ea5aacd4-92fc-48b9-9f0f-cfd64ef72eae.png)
![image](https://user-images.githubusercontent.com/88879492/142353769-d05d2a7e-4c8d-4fd6-b106-044c4a81bd06.png)
![image](https://user-images.githubusercontent.com/88879492/142353832-2f501d17-a4b4-4efd-a660-9b6257fc83b7.png)
![image](https://user-images.githubusercontent.com/88879492/142353873-17065cf4-35d7-4b53-99a4-db6a38f96951.png)</br>
![image](https://user-images.githubusercontent.com/88879492/142353893-7363458e-0779-479a-8173-1039e15bbd67.png)</br>
![image](https://user-images.githubusercontent.com/88879492/142354316-ed2f2305-5046-4030-a694-aaef1da54ecf.png)</br>
![image](https://user-images.githubusercontent.com/88879492/142354346-30b12478-39bb-4f16-8a03-955d5c3d1dcb.png)




# Model Building
<li>Traditional Method</li>
Used scikit-learn library for the Machine Learning tasks. Applied label encoding and converted the categorical variables into numerical ones.Then I splited the data into training and test sets with a test size of 20%. I tried three different models ( Linear Regression, Random Forest Regression, XGBoost) and evaluated them using Mean Absolute Error. 

<li>Automated Method</li>
Used the auto ML library in python called PyCaret. Compared all the regression models and selected the best model for applied hyperparameter tuning and plotted the various curves.

Link to my article: <a href="https://towardsdatascience.com/leverage-the-power-of-pycaret-d5c3da3adb9b">https://towardsdatascience.com/leverage-the-power-of-pycaret-d5c3da3adb9b</a>

#Creation Web Application for Deployment of Laptop Price Prediction Model
We will use streamlit to create a web app to predict laptop prices. In a web application, we need to implement a form that takes all the inputs from users that we have used in a dataset, and by using the dumped model we predict the output and display it to a user.

# Deploy Application to Heroku
Prepare cloud files for deployment
## 1) Procfile :
Create a file name Procfile which is an initiator file for Heroku.
## 2) requirements:
Create a file named requirements.txt. It is a text file that contains the name and version of a library that you have used to create your project.
## 3) setup file:
Create a file name setup.sh which contains how to create the directory structure in the cloud.

## Upload Code to Github
Log in to your GitHub account and create a new repository of the project name of your choice. Now you can either use the upload button to upload all files by selecting from a local file manager. And you can also use the GIT bash command as stated below to upload your code.
git init #initialize empty repository
git remote add origin   #connect to repository
git pull origin master   #pull initial chnges
gid add -A #to add files in staging area
git commit -m initial commit
git push origin master  #push all files to github

Deploy to Heroku
Log in or register to Heroku if you do not have an account. After you log in in the top-right corner you will have the option of new. create a new app. Give a unique name to your code and this name will be your website URL followed by the Heroku domain and let the region be united states only.

![image](https://user-images.githubusercontent.com/88879492/142361911-ae682422-b9f1-4280-8e29-18d4144a3f58.png)

![image](https://user-images.githubusercontent.com/88879492/142364685-a3bcf5dd-4158-4842-a3b1-ab400e815fc3.png)


# Deploy the code

Now scroll down and you have the option to deploy code. we will deploy on the main branch. Click on deploy branch and observe logs. After successfully deployment it will give you the web app URL on the view app option and your application is deployed successfully.

Now you can share the URL with anyone to use your application.



After creating a new repository copy the ssh link of a repository to connect with a repository. And then line by line follow the below commands. 
![image](https://user-images.githubusercontent.com/88879492/142360271-9027c097-9c64-4cd2-aa09-6730fb07c9cc.png)

![image](https://user-images.githubusercontent.com/88879492/142360437-4dcc0025-9e3a-491c-afea-be0e67e9bbcf.png)

![image](https://user-images.githubusercontent.com/88879492/142360564-4721a96f-3ae0-468d-a9f5-d39574333b45.png)




Web application: <a href="https://laptop-price-prediction-model.herokuapp.com/">https://laptop-price-prediction-model.herokuapp.com/</a>
