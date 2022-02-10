# Scrapping Glassdoor data and Predicting Salary

Extracting salary information on data related jobs in order to predict the salaries for certain jobs based on the location, title, and job summary, etc. The project was a real test of data science skills, such as web-scraping, data pre-processing, data analysing, data visualisation, feature engineering, and building multiple regression model to predict the salary and comparing the result which performs best. 

For detailed information about this project refer to the <b>report</b> file.

## Code and Resources Used
Jupyter Notebook <br>
Packages: pandas, numpy, sklearn, matplotlib, seaborn, selenium<br>
Scraper Article: https://towardsdatascience.com/selenium-tutorial-scraping-glassdoor-com-in-10-minutes-3d0915c6d905<br>
Other Resources: Included in Report<br>

## Web Scrapping
Extracted over 1000 jobs from glassdoor.com and obtained the following information from each job

Job title <br>
Salary Estimate <br>
Job Description<br>
Rating<br>
Company<br>
Location<br>
Company Headquarters<br>
Company Size<br>
Company Founded Date<br>
Type of Ownership<br>
Industry<br>
Sector<br>
Revenue<br>
Competitors<br>

## Data Cleaning and Feature Engineering 
The data was not good qaulity to feed the model. Cleaned the data using the following steps also added new features which was useful for the model and visualisations.
- Removed unnecessary columns
- Removed rows where salary data was missing
- Made a new column which gives the average salary
- Made a new column for company state
- Column for description length
- Added a column for if the job was at the company’s headquarters
- Made a new column using Job Title feature to tell the experience.
- Transformed founded date into age of company
  
## Exploratory Data Analysis 
Created various type of plots (barplot, histogram, countplot, Correlation  matrix, etc) to analyse the results easily. 
  ![image](https://user-images.githubusercontent.com/32816737/153202051-dd8c6c9d-8107-4658-be68-87576b5039cc.png)
  ![image](https://user-images.githubusercontent.com/32816737/153202299-38c32e40-1f80-42cc-a13f-7eb2c13ba9d9.png)
  ![image](https://user-images.githubusercontent.com/32816737/153202340-f4057bf4-a6a5-41a9-97dc-a11427e7e473.png)
  ![image](https://user-images.githubusercontent.com/32816737/153202384-edc9933f-24bc-4ac8-bd85-c6e7b895ab16.png)

## Model Building
- Encoding categorical variables using One Hot Encoding. 
- Splitting the data into train set (80%) and test set (20%)
- Built four models (Linear, Ridge, Lasso, Decision Tree, and Random Forest) and analyzed their performance using Mean Absolute Error.


## Model Performance

Results Clearly Shows that Decision Tree is the Best performing model for this dataset followed by Gradient Boosting and Ridge Regression. While the Lasso Regression Mean Absolute Error is the highest among all. 

![image](https://user-images.githubusercontent.com/32816737/153428944-a652c1bf-6157-4172-ba88-51e27adb5f7d.png)

