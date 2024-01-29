
# AdventureWorks-Dashboard

### Dashboard Link : https://app.powerbi.com/groups/me/reports/1a3e3435-aa4e-4f11-b7d7-d8af1f645072/ReportSection?experience=power-bi

## Problem Statement

This dashboard helps Adventureworks (A Global Manufacturing Company that produces cycling equipment and accessories) track KPIs (sales, revenue, profit, returns), compare regional performance, analyze product-level trends and identify high-value customers.

## Objectives
-	Connect and transform the raw csv files that contain information about transactions, returns, products, customers and sales territories.
-	Build a relational data model.
-	Create calculated columns and measures with DAX.
-	Design an interactive dashboard to visualize the data.

 

### Steps followed 

- Step 1 : Load all datasets (csv files) into Power Query editor columns and rename all datasets. This creates queries.
- Step 2 : Remove Product Size Column, change data type of Product Cost and Product Price Columns to Fixed Decimal Number in the Product Table.
- Step 3 : Add a new column to extract all characters before the dash (“-“) in the Product SKU column and name it “SKU Type” in the Product Table . Update the SKU Type calculation to return all characters before second dash, instead of the first. Then replace Zeros (0) in the Product Style column with “NA”
- Step 4: Duplicate the email address column and name it “Domain Name”. Remove all text/characters except for the domain name in the Customer table. Also use transformation steps to clean up and capitalize the domain names.
- Step 5: Add Month Name, Month Number, Start of Year and Year to the calendar table.
- Step 6: Close and apply all changes. This loads all data into the data model in the front end of power BI.
- Step 7: Create a star schema by creating relationships between the Sales, Calendar, Customer, Product and Territories tables.
- Step 8: Connect all three product tables (Product Subcategory, Category) in a snowflake schema
- Step 9: Create a new hierarchy based on the Start of Year and name it “Date Hierarchy”. Right click or drag to add fields until your hierarchy contains the Start of Year, Start of Month, Start of Week and Date.
- Step 10: Create a measure named Total Customers. To calculate the number of distinct AdventureWorks customers who made a transaction.
- Step 11: Create a measure named Return Rate, defined as quantity returned divided by quantity sold.
- Step 12: Create new columns in the Customer table to identify Priority customers based on income levels named “Priority” and “Standard”. Create another column named Education Category grouped into “High School”, Undergrad” and “Graduate”

Snap of new calculated column

![Screenshot (3)](https://github.com/Afolabiopeolu/AdventureWorks/assets/113852375/ba6bcf43-0ab9-4935-afe6-228a9ded692c)
- Step 13: Create a new column in the customer table named Birth Year, to extract only the year from the Birthdate column.
- Step 14: Create a new measure named Bike Returns to calculate the total quantity of bikes returned. Create a new measure named Bike Sales to calculate the total quantity of bikes sold. Create a new measure named Bike Return Rate.

Snap of new measures created

Bike Returns
![Bike Returns](https://github.com/Afolabiopeolu/AdventureWorks/assets/113852375/249a13f7-39fc-4f8e-8262-79822b1bd62e)

Bike Sales
![Bike Sales](https://github.com/Afolabiopeolu/AdventureWorks/assets/113852375/7625d161-4884-4b7c-ac4e-a48b7584efe4)

Bike Return Rate
![Bike Return Rate](https://github.com/Afolabiopeolu/AdventureWorks/assets/113852375/e909d418-9ffc-48e9-883b-42bee5220357)



- Step 15: Create a new measure named Total Cost. Create a new measure named Total Profit.

Snap of measures created

Total Cost
![total cost measure](https://github.com/Afolabiopeolu/AdventureWorks/assets/113852375/c6957e75-c850-4e10-a875-e9b19f8c6714)

Total Profit
![Total Profit](https://github.com/Afolabiopeolu/AdventureWorks/assets/113852375/6d25af67-b382-4cdf-8007-9eda4e690b8b)

Total Revenue
![Total Revenue Measure](https://github.com/Afolabiopeolu/AdventureWorks/assets/113852375/dcbd7ef7-5ad8-498c-b648-acc38a9218b6)


- Step 16 : Add the following measures to the model

  (a) Previous month returns

  (b) Previous month Orders
  
  (c) Previous month profit
  
  (d) Order Target (10% increase over previous month)
  
  (e) Profit Target (10% increase over previous month)
  
  (f) 90-day Rolling Profit.

- Step 17: Sketch Dashboard Layout (Exec Dashboard, Map, Product Detail and Customer detail)
- Step 18: Insert Card Visuals for KPIs in the Exec Dashboard (Revenue, Profits, Orders and Return Rate). Insert a Matrix showing Top 10 products, orders, revenue and return rate.
- Step 19: Insert a card in the Customer Detail report page to show Total Customers and rename the field to ‘UNIQUE CUSTOMERS’. Add a background shape and match the formatting of the cards in the Exec Dashboard tab. Copy and paste to create a second card showing Average Revenue per Customer and rename the field “Revenue Per Customer”.
- Step 20: Insert line chart for Weekly Revenue.
- Step 21: Add a line chart to the Customer Detail report showing Total Customers by week.
- Step 22: Add a donut chart to the customer detail report showing total orders by income.
- Step 23: Add a table to the customer detail report to show customer key, full name, Total orders and Total Revenue.
- Step 24: Add a Map visual in the Map tab of the report view. Add Total orders by country.
- Step 25: Insert Guage and Area Charts in the product detail tab of the report view showing Revenue performance, Orders and Profit
- Step 26: Add bookmarks, custom slicers and page navigation buttons

# Report Snapshots (Power BI Desktop)

![Exec Dashboard](https://github.com/Afolabiopeolu/AdventureWorks/assets/113852375/b12ca0be-9629-4cb4-a57c-0d4b7d79fa11)


![Map](https://github.com/Afolabiopeolu/AdventureWorks/assets/113852375/77671e27-2710-4c72-ac85-30fdf508e079)


![Product Detail](https://github.com/Afolabiopeolu/AdventureWorks/assets/113852375/717e510e-8083-421a-8cae-41fc27e83557)


![Customer Detail](https://github.com/Afolabiopeolu/AdventureWorks/assets/113852375/048dd265-523d-433a-95dc-431a991fe096)


 - Step 27 : The report was then published to Power BI Service.

# Snapshot of Executive Dashboard (Power BI Service)

![Exec Dashboard PowerBI service](https://github.com/Afolabiopeolu/AdventureWorks/assets/113852375/e40ad75a-86be-47a8-935c-6a51754117a2)



