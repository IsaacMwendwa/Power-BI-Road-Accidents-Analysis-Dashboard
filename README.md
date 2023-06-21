# PBI-Road-Acccident-Analysis

![Dashboard Image](https://github.com/IsaacMwendwa/PBI-Road-Accident-Analysis/blob/main/Final%20Dashboard%20Image.PNG "Final Dashboard Image")

## Table of Contents
* [Introduction](#Introduction)
* [Dashboard Requirements](#Dashboard-Requirements)
* [Installation/Usage](#Installation--Usage)
* [DAX Formulas Used in Measures](#DAX-Formulas-Used-in-Measures)
* [Authors](#Authors)
  
## Introduction
* This project is aimed at developing a Power BI Dashboard for generating insights about road accident data in the United Kingdom.
* The dataset can be accessed from this link: [Road Accident Data (UK)](https://drive.google.com/drive/folders/1G3BFBOcSn-i-8aJ6c_MgGWJzhYWM_Okb?usp=sharing)
  
## Dashboard Requirements
* Primary KPI's - Total Casualties and Total Accident values for Current Year and YoY Growth
* Primary KPI's - Total Casualties by Accident Severity for Current Year and YoY Growth
* Secondary KPI's - Total Casualties with respect to Vehicle Type for Current Year
* Monthly Trend showing comparison of Casualties for Current Year and Previous Year
* Casualties by Road Type for Current Year
* Current Year Casualties by Area/Location & Day/Night
* Total Casualties and Total Accident by Location

## Installation/Usage

## DAX Formulas Used in Measures

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




  
