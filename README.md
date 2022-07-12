# tech_job_salaries
This code aims to answer questions about base salary and total annual compensation for Data Science and STEM Salaries.  Data was analyzed from Kaggle located here: https://www.kaggle.com/datasets/jackogozaly/data-science-and-stem-salaries

## Blog Post
https://medium.com/@daniel.abreu_14097/salaries-in-tech-9f5ef4b3f218

## Project motivation
Questions which drove this project were the following:
1) Which tech job pays the most base salary and total yearly compensation on average?
2) What is the average number of years people stay at a company?
3) Do males have a larger overall annual compensation than females in the tech industry?
4) What are the biggest contributors to the overall annual compensation you make?

## Libraries used
numpy, pandas, and Pyplot from Matplotlib - These are standard libraries for analyzing and visualizing data in Python

sklearn - This package is a standard package in Python for machine learning and is used to build a Linear Regression model in this project

## Files in the repository
Levels_Fyi_Salary_Data.csv: This is a csv file obtained from the Kaggle site listed above.  Full information on the data, columns, data types, etc are located there

tech_job_salaries.ipynb: This is the jupyter notebook created in order to answer the questions listed above.  It note only goes through some data wrangling in order to answer some analysis questions, but it also includes a machine learning Linear Regression model at the end to look into question (4) listed

NOTE: tech_job_salaries.ipynb will need to be located in the same folder as Levels_Fyi_Salary_Data.csv in order to run the script

## Summary of results
### Based on analysis the following conclusions were made:
- Top 10 companies respondents belong to are: Amazon, Microsoft, Google, Facebook, Apple, Oracle, Salesforce, Intel, Cisco, IBM

- Overwhelming number of respondents are in Software Engineering

- The upper-bound for max base salary and total annual compensation are very high compared to their respective means

- Mean and max base salary stay pretty consistent for most companies except for a few like Netflix, Roku, Doordash, Brex.  Note that Netflix and Squarespace have the largest max base salary available which is where the high Product Management and Software Engineer jobs are

- Base salaries seem higher in CA and NJ

- Within companies, there are some which have very large max annual compensation compared to the mean annual compensation meaning some companies are able to offer their employees considerable perks 

- There is one very clear outlier where their total annual compensation is much much larger than the average for that area.  They work at Facebook in Menlo Park, CA.  Besides this most areas don't have instances where their employees are able to get more annual compensation than the average.  Exceptions are San Mateo, FL; Lost Gastos, CA; Los Altos, CA 

- Most people stay with the company for only a few years before moving on since the number of people with more years at the same company drastically decreases after 2 years

- We do see a clear gender bias in the data for total annual compensation

- Titles with a discernable gender bias are: Human Resources, Marketing, Product Designer, and Product Manager


### Based on machine learning the following conclusions were made:

- Location plays a central role in overall compensation, majority of locations being in California

-->This agrees with the analysis done above

- Company Booking.com, Nvidia and Intel have good overall compensation, whereas other companies do not like Yandex, Qualcomm, Netflix

--> This result seems strange to me.  Booking.com, Nvidia, and Intel are all companies that are NOT in the top 20 for highest mean annual total compensation which was analyzed above.  Also Netflix IS in the top 20 companies with high mean annual total compensation according to the analysis above but the coefficient weight is negative meaning the model is indicating working at Netflix will have a negative impact on your overall annual compensation

- Years of experience, years at the company, tag, race, education, and gender don't play as much of a central role as location and company do since their coefficients don't show up in the top 20 weights

Because of these descrepancies I'll generally conclude from the model that:

- Location and company play a key role in your total annual compensation, with companies in CA providing better compensation

- I won't conclude any of the other findings based on the model since I'm unsure of it's accuracy

## Acknowledgements
I'd like the thank Verizon Communications who paid for this course and enabled me to further my learning in this deep field of Data Science.  I'd also like to thank Udacity for hosting the course in a format that accomodates my learning style most-efficiently
