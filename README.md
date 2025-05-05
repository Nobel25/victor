# Superstore Data Project
## Table of Content 
1. Project Overview
2. Dataset Source
3. Tools
4. Data Cleaning
5. Exploratory Analysis
6.  Data Analysis


### Project Overview
The project aims to analyze the Superstore trends at [Sample_Superstore]
using the provided dataset.
It will identify patterns and potential impacts on the company's sales, profit and the maximun quantity 
the company had sold.
The findings will support decision-making and strategic planning for marketing management and more profit.

### Dataset Source
This dataset was obtained a third party given to me Neovarsity Institution

### Tools
- Excel-Data Extraction[www.superstore.dataset.com]
- PowerBi - Data Cleansing
- PowerBi - Data Visualization

### Data Cleaning
1. 	I Loaded the data:
2.	Open Power BI Desktop.
3.	Click Home → Get Data → Excel.
4.	Select the Sample - Superstore.xlsx) and choose the sheet(s) Orders, People and Returns
5.	I clicked Transform Data → it opens Power Query Editor
6.	I removed the unneeded columns like Row ID.
7.	I Fixed the data types by making sure Order Date and Ship Date are set as Date.
8.	I remove duplicates in Order ID.
9.	I cleaned up text columns such as Customer Name (trim spaces).

#### Step-by-step inside Power Query:
•	Home → Transform Data (open Power Query).
•	Remove Row ID:
   o	Right-click on Row ID column → Remove.
•	Set Data Types:
   o	Click each column’s small icon (e.g., 123, ABC).
   o	Assign Date to Order Date and Ship Date.
   o	Assign Decimal Number to Sales, Profit, Discount, Quantity.
•	Trim and Clean Text:
   o	Select multiple text columns → Transform tab → Format → Trim → then again Format → Clean.
•	Remove Duplicates:
   o	Highlight Order ID and Product Name → Remove Duplicates.
•	Replace Nulls:
   o	Select columns like Discount → Transform tab → Replace Values → Replace null with 0.
•	Add Order Year Column (Optional):
  o	Select Order Date → Add Column tab → Date → Year → Year.


### Exploratory Analysis
### Page 1 – Sales Report
The dashboard include the following metrics and visuals:
KPIs:
- Total Sales
-	Maximum of Sales
-	Average Sales
  
Visual Reports:
-	Sales by Sub-Category
-	Average of Sales by Segment
-	Sales by State and City
-	Sales by Ship Mode
-	Sales by Region

### Page 2 – Profit Report
This page will focus on profitability, using the following metrics:
KPIs:
-	Total Profit
-	Total Quantity
  
Visual Reports:
-	Profit by Category
-	Profit by Region
-	Profit by Segment
-	Profit by Year and Month
-	Profit by Sub-Category

  ### Data Analysis
  1. I went back to the main Power BI canvas
      •	Click Home → Close & Apply (after cleaning in Power Query).
 2.  Create Calculated Measures (KPIs)
      Use DAX (Data Analysis Expressions) for advanced KPIs:

     •	Total Sales:
           Total Sales = SUM('Orders'[Sales])
     •	Maximum of Sales:
           Max Sales = MAX('Orders'[Sales])
     •	Average Sales:
          Average Sales = AVERAGE('Orders'[Sales])
     
 3.    Once created:
     •	Insert Card Visuals → Drag each measure into a Card → Set titles (e.g., "Total Sales".
 4. Create Visual Reports:
    
      * Report                    - Chart Type   	  - Fields
    
     - Sales by Sub-Category	   - Bar Chart     -	Sub-Category (Axis), Sales (Values)
     - Average Sales by Segment -	Column Chart -	Segment (Axis), Sales (Average aggregation)
     - Sales by State and City  -	Map Chart    -	State/City (Location or Row/Column), Sales
     - Sales by Ship Mode       - Donut Chart	   - Ship Mode (Legend), Sales
     - Sales by Region	         - Bar Chart      -	Region (Axis), Sales (Values)
   
       I added slicers for:
   •	Region
   •	Order Date
   •	Category

5. Create the KPIs (DAX Measures)
I went to the Modeling tab → Click New Measure, and enter:
1.	Total Profit

Total Profit = SUM('Orders'[Profit])
2.	Total Quantity

Total Quantity = SUM('Orders'[Quantity])
I inserted Card Visuals for both:
    •	Card 1: Drag Total Profit
    •	Card 2: Drag Total Quantity
    •	Rename their titles accordingly


6. Create Visual Reports

   
- Report                 -	Chart Type    -	Fields
  
- Profit by Category    - 	Donut Chart -	Axis: Category,
                                          Values: Profit
- Profit by Region	    - Bar Chart	    -  Axis: Region,
                                          Values: Profit
- Profit by Segment	     -Donut Chart	    -  Axis: Segment, 
                                          Values: Profit
- Profit by Year and Month-	Line Chart	  - Axis: Order Date ( Year → Month),
                                          Values: Profit
- Profit by Sub-Category-	Horizontal Bar Chart-	Axis: Sub-Category, 
                                                Values: Profit

   - I used slicers (filters) for:
    •	Region
    •	Category
    •	Year

