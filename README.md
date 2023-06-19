# PBI-Road-Acccident-Analysis

#### Power BI DAX Formulas Used in Measures

**1. Current Year To Date Casualties -- CY Casualties Measure**
* `CY Casualties = TOTALYTD(SUM(Data[Number_of_Casualties]), 'Calendar'[Date])`

**2. Previous Year Casualties -- PY Casualties Measure**
* `PY Casualties = CALCULATE(SUM(Data[Number_of_Casualties]), SAMEPERIODLASTYEAR('Calendar'[Date]))`

**3. Year on Year Growth of Casualties - YoY Casualties Measure**
* `YoY Casualties = ([CY Casualties] - [PY Casualties])/[PY Casualties]`

**4. Current Year Accidents -- CY Accidents Count Measure**
*  `CY Accidents Count = TOTALYTD(COUNT(Data[Accident_Index]), 'Calendar'[Date])`

  
