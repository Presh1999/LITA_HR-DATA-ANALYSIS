# LITA_HR-DATA-ANALYSIS
This is an analysis to determine  employee attrition in a company, and the reason for the attrition.

### Overview
----
This analysis examines employee attrition within the company, focusing on the reasons behind employee exits and identifying trends or patterns that may influence retention strategies. The dataset contains information on employees' demographics, job roles, travel status, and employment history, providing insights into both the current workforce and those who have left the company. The goal is to understand the factors contributing to employee attrition and how they can inform HR strategies to improve retention.


### Project Objective
----
The objective of the project is to:
 - Calculate the attrition rate within the organization.
 - Identify key factors contributing to attrition, such as department, age group, job role, marital status, and travel frequency.
 - Analyze the reasons for attrition to understand the causes of employee exits and highlight areas for improvement.
 - Provide actionable insights that can guide HR and management in reducing attrition and improving employee retention.

### Data Sources
----
The data provided includes the following columns:
  - Attrition: Whether the employee has left the company (`Yes` or `No`).
  - Business Travel: The frequency of business travel (`Travel_Rarely`, `Travel_Frequently`, `Non-Travel`).
  - Age Band: The age band of the employee (e.g., `Under 25`, `25 - 34`, `35 - 44`, `45 - 54`, `Over 55`).
  - Attrition Label: Whether the employee is a current or former employee (`Ex-Employees`, `Current Employees`).
 -  Department: The department the employee works in (e.g., `Sales`, `R&D`).
 -  Education Field: The field of education of the employee (e.g., `Life Sciences`, `Medical`).
 -  Employee Number: A unique identifier for the employee.
 -  Gender: Gender of the employee (e.g., `Male`, `Female`).
 -  Job Role: The job title of the employee (e.g., `Sales Executive`, `Research Scientist`).
 -  Marital Status: Marital status of the employee (e.g., `Single`, `Married`, `Divorced`).
 -  Over Time: Whether the employee works overtime (`Yes` or `No`)

### Tools Used
----
  - Excel: For basic data manipulation, filtering, and summary statistics.
  -  Power BI: For creating interactive dashboards and visualizations.
    
    

### Data Analysis
----
#### Data Analysis in Excel worksheet
   
   - To calculate employee attrition, use the COUNTIF function
      =COUNTIF(A2:A1,470, "Yes")

   This counts how many "Yes" enteries are in the Attrition columbn.
  
   - To get the	Attrition Rate (as a percentage of total employees)
   =COUNTIF(A2:A32, "Yes") / COUNTA(A2:A32)

 This will give the attrition rate as a percentage.

 - To determine the reasons for attrition, pivot table was used to get a breakdown of Attrition by;
   -  Department: Are certain departments experiencing higher attrition?
   -  Age Band: Does attrition vary across age groups?
   -  Gender: Are men or women leaving at higher rates?
   -  Job Role: Which job roles are most affected by attrition?
   -  Educational field: Do employees in certain educational field have higher attrition rates?
   -  By Marital Status: Are single, married, or divorced employees more likely to leave?

  ####  Data Analysis and Visualization in Power BI
   -  Step 1: Import the Data
      -  Open Power BI Desktop.
      -  Go to Home > Get Data > Excel or SQL Server (depending on where your data is stored).
       - 	Import the dataset into Power BI.

   -  Step 2: Create Measures for Attrition
       a. Percentage of Attrition/Attrition Rate:
      
          - Attrition rate=Sum(['Attrition count'])/Sum(['Total Employee'])
      
         -  N/B: First use condidtional column to convert the Attrition(from text to number)
           
        b. Average age
      
          - Average age=Ave(age)

   - Also create a conditional column for Job satisfaction rating

#### Visual Analysis and Inference
 - Attrition Rate by Department: A bar chart to show how attrition varies across departments.
 - Attrition Rate by Age group and gender: Donut charts to display attrition across different age group and gender
 - Attrition Rate by Educational Fields: A column chart to show attrtion count across Educational Fields.
 - Travel Frequency vs Attrition: A bar chart comparing attrition for different travel categories (`Travel_Rarely`, `Travel_Frequently`, `Non-Travel`).

#### Use of Slicers
  - Use Slicers to allow users to filter the data by Department, Age Group, Gender, Educational field.

#### Create Dashboards
  -	Combine these visualizations into a dashboard.

### Key Inference Example
- **Age Group**: It might be observed that attrition is higher in younger employees (e.g., `25 - 34`), which could suggest that younger workers are more likely to leave for career advancement or personal reasons.
- **Travel Frequency**: Employees with `Travel_Rarely` may show a higher attrition rate, suggesting that infrequent travel may be associated with dissatisfaction or lack of career progression.


7. Key Metrics

- Overall Attrition Rate: 19.35% (for the sample data).
- Attrition Rate by Department: The rate of attrition by department (e.g., 10% attrition in `R&D` and 25% in `Sales`).
- Attrition Rate by Age Band: For instance, the attrition rate for employees aged 25-34 might be 25%, while it’s lower for employees aged 45-54.
- Attrition Rate by Travel Frequency: Do employees who rarely travel leave at higher rates?
- Gender-specific Attrition: If you find a significant difference between male and female attrition rates, this could be a critical metric.
-Overtime Impact on Attrition: Does working overtime affect attrition? Compare those who work overtime vs. those who don’t.


### Example of Key Metrics Breakdown:

| Metric                        | Value |
|-------------------------------|-------|
| **Overall Attrition Rate**     | 19.35%|
| **Attrition Rate (Sales Dept.)**| 25%   |
| **Attrition Rate (R&D Dept.)** | 15%   |
| **Attrition by Age (25-34)**   | 30%   |
| **Attrition by Gender (Male)** | 20%   |
| **Attrition by Travel Frequency**| 22% (Travel_Rarely) |
