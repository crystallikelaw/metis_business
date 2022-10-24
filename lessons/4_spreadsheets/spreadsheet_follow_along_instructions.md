## Chapter 1: Spreadsheets for Data Analysis

Today's lesson will walk through some core functionality of spreadsheet tools and demonstrate how spreadsheet tools can be leveraged to move from raw data to useful information. The data we will be using for this activity is the Ames housing datasetLinks to an external site., available on KaggleLinks to an external site.. It contains details about a sample of residential property sales in Ames, Iowa.

Note: Supplemental data on neighborhood population and private schools have been simulated for this exercise.

### Microsoft Excel vs Google Sheets

Two popular spreadsheet tools are Microsoft Excel and Google Sheets. The two applications have very similar functionality, and what you learn in one will translate easily to the other. Main differences between the two applications include:

 * Excel can handle larger data a bit more efficiently and has a bit more functionality
 * Google sheets is much more powerful for collaboration and is completely free

We will be demonstrating today's lessons using Google Sheets. Begin by logging into your Google account and clicking on the nine dots in the upper right corner. Of the available options for Google applications, click on "Sheets" to enter the Google Sheets application.

## Chapter 2: Spreadsheet Basics

Open up a blank Google Sheet by clicking the "+" option on the Google Sheets homepage. Then go to File > Import, and an Import file window will pop up. On the top banner, select "Upload", then "Select a file from your device". Select the workbook we will be working with today, titled "Ames Housing.xlsx".

The remainder of the exercise will walk through eight chapters (tabs) of the workbook, each covering a different core spreadsheets topic. The cells in the workbook highlighted in yellow correspond to the exercises we will be completing in each tab.

We will now introduce some basic concepts of working with spreadsheets, such as navigating the toolbar, the basics of organizing spreadsheets, and working with different data types.

1. Create a new sheet and name it "Data Types".

2. Create one cell for each of the following data types; make up the values as you please:
    * General
    * Number
    * Date
    * Percentage
    * Text
    * Currency

3. Observe the effect of adding three to each of these values. (Note: to input any equation into a cell, begin by typing "=" or "+")

4. Observe the effect of using the toolbar to change the Percentage and Date data types to Number.
5. Use the toolbar to make other edits to the cells, such as:
    * Changing the number of decimal places
    * Changing the data type to currency
    * Changing fonts, font sizes, colors, bold, etc.

## Chapter 3: Spreadsheet Functions

One of the most powerful tools available to us within spreadsheet applications is the ability to manipulate, combine, and arrange data using built-in functions. These functions allow us to perform the basic operations of mathematics, manipulate text, gain insight into the dates, and much more.

For each step below, make sure that you copy the formula for every row in the dataset. Often, Google Sheets will automatically suggest an autofill option. Otherwise, a quick shortcut to copy the cell that you're currently in down to the rest of the column is to double-click the small blue square at the bottom-right of the cell.

1. Create a new column that calculates SalesPrice/Lot Area, i.e price per sq foot.
2. Create a new column that adds up number of Baths, Bedrooms, Fireplaces, and Garage Cars to get an idea of the number of total amenities available.
3. Using the new calculated cell for total amenities, calculate the SalesPrice per amenity.
4. Again using the calculated cell for total amenities, calculate the percentage of total amenities that are bathrooms.
5. Concatenate the text for Neighborhood and Exter Cond (external condition) to create a new column that shows the two combined.
6.  Create a new column that converts the year built into an actual date, with month and day set to equal to January 1st. (Hint: use the DATE function)
7.  Create a new column that calculates the number of days between the date built and today's date, i.e. how many days old the house is. (Hint: use the TODAY function)
8.  Get the minimum of Year Built, minimum of Year Remod/Add, and minimum of Gr Liv Area. Save these values in cells U5, V5, and W5 respectively.
9.  Create a new column that calculates how many years after the minimum year that each house was built. (Hint: use U5 and $ to lock the row number but not the column number)
10. Create two new columns that calculate the number of years after minimum Year Remod/Add and the amount of area above Gr Liv Area for each house. You can do this by simply dragging over and down the formula from the prior step.
11. Play around with other aggregation functions in cells U5, V5, and W5, such as AVERAGE, MAX, and MEDIAN, and observe how your new columns change.

## Chapter 4: Conditional Functions

The functions we've seen so far have been straightforward calculations that do not depend on the contents of other cells. Now we introduce the concept of conditional functions, which execute based on whether certain statements are true or false.

1. Create a new column that returns the year remodeled if the Exter Cond (external condition) column is equal to "Ex" (Excellent), and otherwise returns the year built.
2. Now we are going to work with a compound statement. Create a new column that returns "Good Condition" if the external condition is "Ex" or "Gd" (Good), and otherwise returns "Not Good Condition".
3. Now we will walk through a Nested If statement. Create a new column that returns "Ex" if the external condition is "Ex". If it is not Excellent, check if it was built before or after 1960. If it was built after 1960, then return "NEW but not excellent". If it was built before 1960, then return "OLD and not excellent".
4. We can also build aggregate functions with conditional statements. In cell N4, calculate the average year built for houses where the external condition is "Ex". In cell N5, calculate the average year built for houses where the external condition is "TA".
5. Play around with other conditional aggregation function in cells N4 and N5, such as SUMIF and COUNTIF.

## Chapter 5: Connecting Worksheets

Many of you have probably heard of the famous VLOOKUP function. This function is well-known due to its widespread use and power in bringing together data from different sources.

For these exercises, we will be making use of two supplemental sheets:

1. The "Current Population lookup" tab contains the current population for each neighborhood
2. The "All year private schools lookup" tab contains the number of private schools in each neighborhood in each year, presented in two different formats (long and wide)
3. Use VLOOKUP to find the current population associated with the neighborhood of each house.
4. Repeat the same task, this time using INDEX MATCH instead of VLOOKUP. Confirm that the two methods produce the same solution.
5. Use string concatenation and VLOOKUP to find the number of private schools for each house's neighborhood and built date. (Hint: use the long version of the private school data)
6. Repeat the same task, this time using INDEX MATCH instead of VLOOKUP. Confirm that the two methods produce the same solution. (Hint: use the wide version of the private school data)

## Chapter 6: Filtering and Sorting Data

Oftentimes when working with data, we only want to look at certain subsets of the data at a time. Other times, we'd like to order the data so that it can be viewed in a more digestible fashion. Spreadsheet applications make it easy and intuitive to accomplish such tasks.

1. Filter for rows where SalePrice is over 500,000.
2. Filter for rows where Neighborhood contains "Ames".
3. Sort by ascending SalePrice.
4. Sort by Neighborhood, and then further by SalesPrice within each neighborhood.

## Chapter 7: Pivot Tables

Pivot Tables are another well-known functionality of spreadsheets. To transform from raw data into useful, digestible information on which decisions can be based, we often need to aggregate the data in some fashion. Pivot Tables allow us to aggregate the data into views and groupings that we'd like to explore, and are an invaluable tool for data analysis.

1. Create a Pivot Table that shows the average SalePrice by neighborhood. Sort the Pivot Table to find the most expensive neighborhood.
2. Create another Pivot Table that shows the average SalePrice by Exter Cond.
    * Then bin together Year Built in groups of ten years to view average SalesPrice by Year Built group and Exter Cond.
    * Finally, bring in the count of Exter Cond so we can see how many values make up each of the averages.

## Chapter 8: Spreadsheet Charts

You may have recognized that Pivot Tables do not always tell the story as quickly or deliver the impact as strongly as we'd prefer. An incredibly powerful strategy to help us accomplish these goals is to organize and present the data using charts.

1. Create a bar chart that shows the average SalePrice by neighborhood. Identify the most expensive neighborhood. (Hint: Make a copy of the first Pivot Table from Chapter 6)
2. Create a line chart of average SalePrice for each group of ten years. Make use of the "small or big" column to produce two different lines on the line chart: one for big houses and one for small houses. Lastly, allow the chart to be filterable by Exter Cond. (Hint: Create a pivot table first)
3. Create a scatter plot to view the relationship between Lot Area and SalesPrice.
4. Use a histogram to view the distribution of SalePrice.
5. Play around with adding in titles, axis titles, adjusting numbering, etc. within each of these charts

## Chapter 9: Data Cleaning with Spreadsheets

Very often the data we are working with is not clean and needs some adjustments. A few spreadsheet functionalities such as text to column, deduplication, data validation, and conditional formatting, are useful for data cleaning tasks.

1. The Chapter 8 tab contains a list of neighborhood short names and full names. Use Text to Columns to split the data into two columns, so that we can use it as a mapping between short names and full names.
2. The Chapter 8 populations tab contains a copy of the Current Population lookup. Create a new column to the right of the Neighborhood column that uses VLOOKUP to obtain the full name of each neighborhood.
3. Going back to cell D2 of the Chapter 8 tab, use Data Validation to create a drop-down list of all the full names of neighborhoods.
4. In cell E2, use VLOOKUP to return the population corresponding to the chosen neighborhood in cell D2. This way, we can select different values of neighborhood full names and automatically see the corresponding population.
5. Revisiting the data in Chapters 6 and 7, we see that some rows on the bottom are duplicates. Remove the duplicate rows and observe the effect on the refreshed Pivot Tables and charts.
6. In Chapter 7, highlight all values of SalesPrice that are greater than 160000.
