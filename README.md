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

![Car Insurance Management Dashboard](https://github.com/user-attachments/assets/0b16942f-a9b3-419e-b39d-af9732377501)

[Car Insurance Management Dashboard on Tableau](https://public.tableau.com/views/CarInsuranceManagementDashboard/CarInsuranceManagementDashboard?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)


![Car Insurance Operational Team Dashboard](https://github.com/user-attachments/assets/6694846d-814c-492c-87c2-9e826a411105)

[Car Insurance Operational Team Dashboard on LookerStudio](https://lookerstudio.google.com/reporting/fa76356a-e52c-4509-b48f-6811c6ed0891)

### Insights
**Claims Overview:** A total of 10,340 claims was observed, with a total claimed amount of ₦518.24 million. The minimum household income of the customers is ₦45,000, while the maximum is ₦250,000, indicating a broad economic spectrum among claimants.

**Gender distribution:** 50.47% of the claims were made by females and 49.53% by males. This indicates a fairly balanced distribution of claims across both genders.

**Car Usage:** Private vehicles have higher claim rate (80.5%) compared to commercial vehicles (19.5%), suggesting potential risk factors associated with private car usage. 

**Claim Frequency:** A majority of vehicles (5,912) have only claimed once, indicating a low frequency of claims for many customers. As claim frequency increases, there is a notable decline, with 1,400–1,550 claims in the higher frequency ranges (2–4), suggesting a potential relationship between claim frequency and risk.

**Household Income and Claim Amount:** There is no clear correlation between household income and claim amount, implying that income does not significantly influence claim amounts.

**Car Make and Model:** Ford vehicles, particularly the Mustang model, have a higher claims(124), suggesting potential risk factors associated with specific car makes and models.

**Car Year:** Claims increased significantly from the late 1980s to early 2000s and then declined, indicating that cars manufactured during this period may have higher claim risks.

**Coverage Zone:** While claims are relatively balanced across coverage zones, suburban and highly urban areas exhibit slightly higher claim frequencies. This suggests that factors such as traffic density, road conditions, and population density in these areas may contribute to increased risk.

**Distribution of Customers Based on Claim Frequency and Number of Drivers:** For all claim frequencies, households with zero drivers significantly outnumber those with one or more drivers. This trend is particularly pronounced for claim frequency 1, where over 80% of customers have zero drivers. As the number of drivers in a household increases, the overall claim frequency tends to decrease. This suggests that having multiple drivers may be associated with lower claim risks.
