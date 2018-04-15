---
title: "CodeBook"
author: "Group2"
date: "4/9/2018"
output: html_document

---
Description: This code book describes each of the variables, the data, and any transformations or work that you performed to clean up the data

## Task 1
Here is the description for task 1.



## Task 2
1) The data was imported, given column titles, and saved as Panel_8595.2  
2) Panel_8595.2 was compared to the research paper to better label the variables. The research paper gave only the data for years 1987 and 1995, so we only looked at the summary statistics for 1987 (or 1995) in order to figure out which variables belonged to each column.  
3) Panel_8595.2 was relabeled with better names and superfluous variables (such as the column with periods and the last two columns) were removed from the data table. This was saved as Panel_8595.3.  
4) Panel_8595.6 contains all the converted data after Energy was converted to MWh and $ were converted to 2017 dollars. See conversions below.  
5) Panel_8595.7 is the data table after we added another variable, Phase1 which indicates whether the Phase 1 of the Clean Air Act had been initiated.   
6) We saved this table as a text file, "tidy2.txt".  
7) tidy2.txt was analyzed to find the average of all variables across all years for each plant for the 11 year period. This became tidy2_a.txt.  
8) tidy2.txt was analyzed to add all variables across all variables within a particular year across all 92 plants. That will give you the totals for each year. For example, the total Energy per day used by all plants in 1990. This became tidy2_b.txt. 





Variable     | Variable Name   | Description                  |Units (Initial)  | Units (Final)
-------------| ----------------|----------------------------|-----------------|--------------
Electricity  | Electricity     | Net electrical generation    |kWh (millions)|  Daily MWh
SO2          | SO2             | Bad output sulfur dioxide    |short tons|      Daily short tons
NOX          | NOX             |Bad output nitrogen oxides    |short tons|      Daily short tons
Capital Stock| CapStock        | Input                        |$ (millions, 1973)| $ (millions, 2017)
Employees    | Employees       |Input                         |Workers|           Workers
Heat Content Coal | HC_Coal    |Input                         |Btu (billions)|    Daily MWh
Heat Content Oil | HC_Oil      |Input                         |Btu (billions)|Daily MWh
Heat Content Gas | HC_Gas      |Input                         |Btu (billions)|Daily MWh
Phase 1 CAA | Phase1           |Whether or not Phase 1 of CAA has been announced | Unitless (1= Announced, 0 = Not announced)|Unitless (1= Announced, 0 = Not announced)

##### Conversions:  
(Wh/year)(1 year/ 365 days)(1MWh/1E6 Wh) = MWh/day  
(Btu/year)(1 year/ 365 days)(2.93E-7 MWh / 1Btu) = MWh/day  
$1 in 1973 = $5.52 in 2017