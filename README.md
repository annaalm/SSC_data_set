# SSC_data_set

Data for "Social Security Contributions and the Business Cycle"
Almosova, Burda, Voigts


The Excel file containes aggregated SSC rates in text format


The MATLAB file SSC_schedules_data.mat contains three variables: schedules_data, itemlist_countries and itemlist_years.

Cell array schedules_data is organized as follows. Rows are associated with countries as they are stored in itemlist_countries, 
while columns are associated with years as they are found in itemlist_years. For example, schedules_data(7,3) contains the tax schedule 
for France (the 7th country in itemlist_countries) in the year 2013 (the 3rd year in itemlist_years).

Each element in schedules_data contains an array describing the tax schedule for the respective country and year. In such an array, 
rows are associated with specific tax brackets, with the first (second) column showing the repective marginal tax rate (upper end of 
the bracket). For example, schedules_data{7,3}(2,1) holds the marginal tax rate of the 2nd tax bracket for France in the year 2013, 
while schedules_data{7,3}(2,2) shows the upper end of this tax bracket. The value -2 for the upper end of a tax bracket means the upper 
end is infinity. Taking up the example, the value -2 at schedules_data{7,3}(4,2) means that 4th tax bracket in France in 2013 applies to 
all income in excess of 145488 (the upper end of the previous bracket).
