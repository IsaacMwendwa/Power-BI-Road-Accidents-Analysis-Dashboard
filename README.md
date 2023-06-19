# PBI-Road-Acccident-Analysis

#### Power BI DAX Formulas Used in Measures

**1. Current Year To Date Casualties -- CY Casualties Measure**
* `CY Casualties = TOTALYTD(SUM(Data[Number_of_Casualties]), 'Calendar'[Date])`
