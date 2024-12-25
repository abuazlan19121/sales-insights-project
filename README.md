
# Sales Insights Project

### Dashboard Link : https://app.powerbi.com/groups/me/reports/384d017e-e935-44dc-9e7d-1626c1a36de1/ReportSection

## Problem Statement

Atliq Hardware, a well-established computer hardware and peripheral manufacturer 
headquartered in New Delhi, operates through 10 branches across India. Despite the 
market's dynamic growth, the company has been experiencing a steady decline in sales. 
The Sales Manager has struggled to obtain accurate and consistent insights from regional 
managers, who often provide fragmented data in Excel files or rely on verbal reports. 
This has made it difficult to pinpoint the root causes of declining sales and hampered 
data-driven decision-making.
The current manual reporting process is time-consuming, prone to errors, and lacks the 
depth of insight necessary to adapt to the fast-changing market. Regional managers tend 
to assure the Sales Manager of future improvements without providing detailed analysis 
or actionable insights. As a result, the company is losing opportunities to optimize sales 
strategies, identify underperforming regions, and focus on high-demand products.
To address these challenges, Atliq Hardware aims to implement a robust, automated 
solution using Power BI. The objective is to replace manual reporting with a real-time, 
interactive dashboard that provides the Sales Manager and other key stakeholders with 
comprehensive, up-to-date sales insights. This system will pull data directly from the 
company’s database, streamlining the data collection process and reducing reliance on 
regional managers for fragmented reports.
The project will leverage SQL for data extraction, and Power BI for data visualization. 
This approach will provide the company with the tools necessary to monitor sales 
performance in real-time, track trends, and optimize decision-making processes. The 
automated solution is expected to save time, reduce costs, and improve the overall 
effectiveness of Atliq Hardware's sales strategies, ultimately driving increased revenue 
and competitiveness in the market.

## Steps followed :

### Project Planning: AIMS Grid  

This project is structured using the **AIMS Grid**, a focused project management framework with four key components:  

1. **Purpose**  
   - Reveal hidden sales insights that were previously unavailable.  
   - Empower the sales team with data-driven decision-making through automation.  
   - Minimize manual efforts in data gathering and streamline workflows.  

2. **Stakeholders**  
   - Sales Director  
   - Marketing Team  
   - Customer Service Team  
   - Data and Analytics Team  
   - IT Team  

3. **End Result**  
   - An automated and dynamic dashboard delivering real-time, actionable insights.  
   - Foster a culture of informed decision-making across the sales team.  

4. **Success Criteria**  
   - A dashboard that uncovers key sales order insights using the most recent data.  
   - Sales team achieves a 10% reduction in total costs through improved decision-making.  
   - Sales analysts save 20% of their time previously spent on manual data tasks, allowing them to focus on high-value activities.  

### Data Cleaning and ETL (Extract, Transform, Load)  

This phase focuses on preparing and transforming data for analysis by leveraging ETL processes.  

1. **Connect to MySQL Database**  
   - Establish a connection between the MySQL database and Power BI Desktop.  

2. **Load Data into Power BI**  
   - Import all tables from the database into Power BI Desktop.  
   - Use the "Load" option to retrieve records from SQL and populate them into the Power BI environment.  

3. **Model View and Star Schema**  
   - In the Model View, review and organize data to align with the Star Schema format, ensuring efficient and scalable analysis.  
![Screenshot 2024-09-14 183204](https://github.com/user-attachments/assets/5dbf57f2-ac77-47d1-9a25-dc248b69a53d)

### Step 3: Transform Data with Power Query  

Data transformation is carried out using Power Query Editor, where essential ETL tasks like data cleaning, wrangling, and munging are performed.  

1. **Filter Null Values in Market Table**  
   - Navigate to the **Power Query Editor** by selecting the "Transform Data" option.  
   - Apply filters to remove rows with null values by deselecting the "Blank" option.  
   - This step ensures only valid data is retained for analysis.  

2. **Filter Invalid Values in Transactions Table**  
   - Use MySQL to query and identify negative or zero values in the transactions data.  
   - Replicate the same filtering in Power BI by deselecting unwanted values directly in the Power Query Editor.  
   - Removing these garbage values ensures the dataset contains meaningful, accurate records.
   ![Screenshot 2024-09-14 191226](https://github.com/user-attachments/assets/2866bcdc-a583-4aad-bbf8-53f093ad93d8)
  

3. **Convert USD to INR in Transactions Table**  
   - AtliQ Hardware operates exclusively in India, making USD values irrelevant.  
   - Add a **Conditional Column** in Power Query to normalize currency by converting USD amounts to INR using the appropriate conversion rate formula.  
   - Include a new column titled **Normalized Currency** to reflect sales amounts in INR.
   ![Screenshot 2024-09-14 192035](https://github.com/user-attachments/assets/bdaedfdf-368d-4a18-9571-5d3e8d57e9f7)
  

4. **Identify USD Transactions**  
   - Use Power Query Editor to find and analyze rows where USD is the currency, ensuring all such entries are converted accurately to INR.  

This structured transformation process prepares the data for accurate and meaningful insights.  

### Data Modeling  

Once the dataset was cleaned and transformed, it was prepared for data modeling.  

The sales insights data tables are structured as follows:  
![Screenshot 2024-12-24 194703](https://github.com/user-attachments/assets/44fa0c9a-562a-4279-bbe2-8d4e61f823af)

### Data Analysis (DAX)  

The following DAX measures were used to derive key insights for all visualizations:  

#### **Key Measures**  
- **Profit Margin Contribution %**  
![image](https://github.com/user-attachments/assets/9d5cf700-f8bf-49b7-ab6e-d0567686c898)

- **Profit Margin Percentage**
![image](https://github.com/user-attachments/assets/da63e8ce-4d02-4e3b-8adb-85743c4dcfb5)

- **Revenue**  
![image](https://github.com/user-attachments/assets/043c3993-560d-4c4d-b9e4-16656ae4513c)


- **Revenue Contribution %**  
![image](https://github.com/user-attachments/assets/587c4b87-8d70-4594-a0ce-9802e13d936a)
 

- **Revenue LY (Last Year)**  
![image](https://github.com/user-attachments/assets/1011920b-a7fb-4515-a03d-a33bf19c6db8)
 

- **Sales Quantity**  
![image](https://github.com/user-attachments/assets/3913d2a0-f1ca-4235-9aeb-5838997bcba4)
  

- **Total Profit Margin**  
![image](https://github.com/user-attachments/assets/14f83a5a-e20e-49dc-b886-c0151cfaf451) 

#### **Profit Target**  
- **Profit Target1**  
![image](https://github.com/user-attachments/assets/bd6eb7b2-427d-47f4-a7b5-4bc1cfe4a84d)
  

- **Profit Target Value**  
![image](https://github.com/user-attachments/assets/4eb36ee8-549c-42e6-9d36-fa7a793bf130)
 

- **Target Difference**  
![image](https://github.com/user-attachments/assets/386128be-8139-4d04-a102-4ec3c6877797)

### Build Dashboard or Report  

Data visualization for the data analysis (DAX) was created using **Microsoft Power BI Desktop**.  

#### **Visualizations from Sales Insights:**  
- **Top Performance** :  
![image](https://github.com/user-attachments/assets/e4cb1053-15fb-4ce8-b2c3-e6b90cd63bda)


- **Profit & Revenue Analysis** :  
![image](https://github.com/user-attachments/assets/09d7dd8a-3907-41e8-a822-b5db5e5d1a24)
  

- **Performance Analysis** :  
![image](https://github.com/user-attachments/assets/12f6b48d-bd96-47f1-a84a-4aeda10031fc)

### Tools, Software, and Libraries  

1. **MySQL**  
   - Used to retrieve and query data from the database for analysis.  

2. **Microsoft Power BI**  
   - Employed for creating interactive dashboards and reports.  

3. **Power Query Editor**  
   - Utilized for data transformation, cleaning, and ETL processes.  

4. **DAX (Data Analysis Expressions) Language**  
   - Applied for writing measures and performing complex data analysis in Power BI.  





