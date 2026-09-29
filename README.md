## Project Overview

This project demonstrates the process of importing employee data from an Excel spreadsheet into ServiceNow using Import Sets and Transform Maps.

The spreadsheet data is loaded into an Import Set table and transformed into a custom Employee Test table. Coalesce is used to prevent duplicate employee records during repeated imports.

## Project Workflow

Excel Spreadsheet  
       ↓  
Import Set Table  
       ↓  
Transform Map  
       ↓  
Field Mapping  
       ↓   
Transform Data  
       ↓  
Employee Test Table  
       ↓  
    Reports  
      ↓  
   Dashboard

## Custom Table

**Table:** Employee Test  
**Name:** `u_employee_test`

### Fields
--------------------------
| Field         | Type   |
| ------------- | ------ |
| Employee ID   | String |
| Employee Name | String |
| Email         | String |
| Department    | String |
| Location      | String |
--------------------------

## Import Set

**Label:** Employee Import  
**Name:** `u_employee_import`

## Transform Map

**Name:** Sample Spreadsheet Import  
**Source Table:** Employee Import  
**Target Table:** Employee Test

## Coalesce

Employee ID is configured as the Coalesce field to identify existing employee records and prevent duplicate records during repeated imports.

## Reports

The project includes:

1. **Employees by Department** – Pie Chart
2. **Employees by Location** – Bar Chart
3. **Employee List Report** – List

## Dashboard

**Dashboard Name:** Employee Analytics Dashboards

The dashboard provides a centralized view of employee information using charts and a list report.

## Project Files

- `Import Data Using Transform Maps.docx` – Detailed project documentation
- `Sample-Spreadsheet.xlsx` – Sample employee data used for the import process

## Conclusion

This project provides practical experience in importing spreadsheet data into ServiceNow, configuring Transform Maps, using Coalesce for duplicate prevention, and creating Reports and Dashboards.
