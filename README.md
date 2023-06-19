# PBI-Road-Acccident-Analysis

#### Power BI DAX Formulas Used in Measures

**1. Total Casualties For Current Year and Year on Year Growth**

(a) Current Year To Date Casualties -- CY Casualties Measure
* `CY Casualties = TOTALYTD(SUM(Data[Number_of_Casualties]), 'Calendar'[Date])`

(b) Previous Year Casualties -- PY Casualties Measure
* `PY Casualties = CALCULATE(SUM(Data[Number_of_Casualties]), SAMEPERIODLASTYEAR('Calendar'[Date]))`

(c) Year on Year Growth of Casualties - YoY Casualties Measure
* `YoY Casualties = ([CY Casualties] - [PY Casualties])/[PY Casualties]`

**2. Total Accidents for Current Year and Year on Year Growth**

(a) Current Year Accidents Count -- CY Accidents Count Measure
*  `CY Accidents Count = TOTALYTD(COUNT(Data[Accident_Index]), 'Calendar'[Date])`

(b) Previous Year Accidents Count -- PY Accidents Count Measure
* `PY Accidents Count = CALCULATE(COUNT(Data[Accident_Index]), SAMEPERIODLASTYEAR('Calendar'[Date]))`

(c) Year on Year Growth of Accidents - YoY Accidents Measure
* `YoY Accidents = ([CY Accidents Count]-[PY Accidents Count])/[PY Accidents Count]`




  
