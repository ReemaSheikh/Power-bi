# Power BI
## Dataset link: https://www.kaggle.com/datasets/bravehart101/sample-supermarket-dataset
## Problem Statement
Using Dax & power query to analyse, transform, calculate power bi calculations. This includes flagging, percentage calculation, Dax time knowledge, dynamic visuals, running total etc.

### [1] Flagging of project:
When a project involves several different kinds of expenses, note:

- The project whose deviation in more than one expense type, but not in dollars, exceeds 5% for each of those expense kinds.
- When a project has a single expense type and the variance is greater than 5% but the difference in dollars is less than $85,000, flag the project.

#### Table before flagging:
![image](https://github.com/ReemaSheikh/Dax-Query/assets/171484655/86e67e00-3c73-4e41-ac61-0364eaa56183)

#### Table after flagging:
![image](https://github.com/ReemaSheikh/Dax-Query/assets/171484655/43a685ea-8f02-4a59-bdaa-154f756c7f4e)

#### Dax calculation:
![image](https://github.com/ReemaSheikh/Dax-Query/assets/171484655/255020e3-7e64-4fae-ba06-aa465097ed84) ![image](https://github.com/ReemaSheikh/Dax-Query/assets/171484655/941eab01-44db-4cfd-9f5a-0ad6c33fe26f)

           Here, "0" is not flagged and "1" is flagged. 
           
### [2] Monthly Profit Growth % by comparing Last year Monthly Profit:

Using Sales Order Table user need to see Segment, Region, Category wise Monthly Profit Growth % by comparing Last year Monthly Profit value.

#### Table:
![image](https://github.com/ReemaSheikh/Dax-Query/assets/171484655/b53d4c20-165a-46ce-8b8a-779f4317a2ac)

#### Table after calculation of last year profit and growth percentage:
![image](https://github.com/ReemaSheikh/Dax-Query/assets/171484655/018316ca-b774-4b8c-a50d-051119d1f3a6)

#### Dax calculation:
![image](https://github.com/ReemaSheikh/Dax-Query/assets/171484655/0d58da59-026c-4bc8-add7-5cb457250a04) ![image](https://github.com/ReemaSheikh/Dax-Query/assets/171484655/7e4bc64b-aa6e-44b5-b027-c5d93967ed25)

    The last year profit is the profit of the previous year and growth percentage is the comparison of previous year and current year profit.

### [3] Dynamic visuals:
Making Use of Sales Order Table, dynamically alter the First column in a single table. The user needs to view the sales summary for each category, subcategory, area, and state in a single table. 

- First create a duplicate data of the sales order table by right clicking on the sales order in power query.

- Rename the duplicate data to sales order pivot. In the duplicate data remove the columns that are not required.
![WhatsApp Image 2024-06-29 at 16 47 31_cc5205f2](https://github.com/ReemaSheikh/Dax-Query/assets/171484655/f2dae3cb-05b7-4ec5-be47-d09eb72e3b42) 

- Then click on sales column to select, then go to transform - unpivot columns - unpivot other columns, it will create the column based on sales, attributes and fields.
![WhatsApp Image 2024-06-29 at 16 48 21_0f34b7c9](https://github.com/ReemaSheikh/Dax-Query/assets/171484655/ecb4925f-4314-4787-a7a8-1088fabce2d0)

- Then select a table in dashboard and select the sales order pivot data to fill in the columns. This includes fields and value in rows, sum of sales in value.

  ![image](https://github.com/ReemaSheikh/Dax-Query/assets/171484655/c423c770-a94c-4617-8f13-423c5eacfa8a)

- Select a slicer that will contain only field of the duplicate dataset.

#### Table:
![image](https://github.com/ReemaSheikh/Dax-Query/assets/171484655/264e4207-8fd1-4fa7-88ac-34e80f972cbd)
![image](https://github.com/ReemaSheikh/Dax-Query/assets/171484655/3c5af727-aaa8-42df-a41b-04bdbd6a09be)

    The field can be changed in the slicer to dynamically change the column.

### [4] calculation of running total:
Calculation of running total of sales.

- Select a table with columns containing sales.

- Then click on new measure to calculate running total.
![image](https://github.com/ReemaSheikh/Dax-Query/assets/171484655/ac1588b6-4da3-491a-89f3-47de470fb720)

- Select/Add the running total in the table created. The running total will automatically be generated from the sales.

  ![image](https://github.com/ReemaSheikh/Dax-Query/assets/171484655/2674a791-47b5-4bc1-baf0-8759550edef4)

    The running total is generated.
