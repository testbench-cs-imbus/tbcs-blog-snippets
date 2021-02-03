# Table import via Excel for TestBench CS

## Objective:
Import data tables for Data-Driven Testing into TestBench CS.
A roundtrip (export, edit, re-import) is possible.

This is a sample for using the TestBench CS API.
Read more in our blog https://www.testbench.com/blog/how-to-import-data-tables-for-data-driven-testing

## Preconditions:
* Account for TestBench CS  workspace (free BASIC account is available at http://www.testbench.com)
* Test Case in TestBench CS which is _not_ Data-Driven yet
* Excel VBA macro execution is admitted
* Product ID and Test Case ID are known

## How to identify IDs
* To get your product ID: open product in browser. The URL contains the ID - e.g. in https://cloud01-eu.testbench.com/en/products/17/home the number "17", following "products" is the ID of the current product.
* To get your Test Case ID: open Test Case in browser. The URL contains the ID - e.g. in https://cloud01-eu.testbench.com/en/products/17/testcases/8 the number "8" is the ID of the current test case in this product.

## How to install:
* place the two files (.xls and .ini) in a folder
* edit .ini file. You need to replace placeholders for workspace, login, password and product ID. 

## How to use:
* In the Excel file in sheet "Control", specify the Test Case to which you want to add a data table (Test Case ID).
* Edit data in sheet "Test Data"
* Use the buttons in sheet "Control" to import data to TestBench CS, export data from TestBench CS, or delete a table
Remark: when importing, the Ids of the data tabel, rows and columns are recorded in the worksheet.


## Limitations:
* Table rows and columns are currently resticted to a count of 50 each.
* for BASIC license users, row count is limited to 5.
* The macro tries to access table, rows and columns by their IDS, if IDs are contained in the Excel sheet. If the IDs are outdated, the macro is likely to fail. In this case, remove the IDs for table (Sheet "Control"), columns and rows (Sheet "Test Data").