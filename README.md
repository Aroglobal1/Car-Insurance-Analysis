# Car-Insurance-Analysis

### Project Overview
The objective of this project is to import a car insurance dataset into SQL, create dashboards in Tableau for upper management, and another operational dashboard in Google Data Studio. The project aims to showcase data analysis, visualization, and data pipeline skills.

### Data Source
The data used for this Analysis is the "car insurance_data.csv" file which consists of information on Customer ID, car model, car year, car use, number of drivers, coverage zone, claim frequency, claim amount, household income, gender, educational level and marital status. The data was gotten from Kaggle.

### Tools
- Excel
- MySQL
- Tableau
- LookerStudio


### SQL code
```sql
SELECT Customer_Id, sum(claim_amt) AS Total_claim_amount, avg(claim_amt) AS Average_claim_amount, coverage_zone, car_use, car_year, car_model, car_make, marital_status, parent, gender, car_color, sum(household_income) AS Household_income, sum(kids_driving) AS No_of_Drivers, sum(claim_freq) AS Claim_frequency
FROM `car insurance`.car_insurance
WHERE claim_freq > 0
GROUP BY Customer_Id, coverage_zone, car_use, car_year, car_model, car_make, marital_status, parent, gender, car_color
ORDER BY Customer_Id;
```

### Dashboards

![Car Insurance Management Dashboard](https://github.com/user-attachments/assets/ab2d6d07-0d9c-4d1c-a75b-b253dd30d429)

[Car Insurance Management Dashboard on Tableau](https://public.tableau.com/views/CarInsuranceManagementDashboard/CarInsuranceManagementDashboard?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

![Car Insurance Operational Team Dashboard](https://github.com/user-attachments/assets/577dd6da-8b4e-4710-8d13-6f07b01e9b2d)

[Car Insurance Operational Team Dashboard on LookerStudio](https://lookerstudio.google.com/reporting/fa76356a-e52c-4509-b48f-6811c6ed0891)

### Insights and Recommendations 
