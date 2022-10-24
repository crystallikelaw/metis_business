Analyze actual sales trends for the Russian software company 1C using 2014 sales data provided by [Kaggle](https://www.kaggle.com/c/competitive-data-science-predict-future-sales).

Begin with the raw data workbook, either by directly opening it in Excel or by uploading it to Google Drive and opening with Google Sheets. Note: The workbook will not load within this interface; you have to click the download button on the top right. Additionally, use the link to data in this paragraph, which uses data that has been modified to work well with sheets, rather than the data from Kaggle. However, please feel free to learn more about the data using the Kaggle link.

After you download the workbook, then perform the following analysis steps:

1. Create a column for revenue, which is item_price multiplied by item_cnt_day
2. Split the category names at the dash, using the text to the left of the dash to get broader categories
3. Bring the broader categories into the "All data" sheet by running necessary VLOOKUPs (may take more than 1)
4. If the last letter of the broader category is "s", remove that letter using the if function, left function, right function, and len function--this will consolidate plural and singular versions of the same broader category
5. Create a pivot table that breaks down revenue by cleaned broader category (rows), for each month and year (columns), and convert the values displayed into currency format. Create a grand total column that shows total revenue for each category across all months
6. Freeze panes so that you can scroll to look at totals for the different categories and still have labels available
7. Create a bar chart to see which broader categories had the highest total sales for the year
8. Create a line chart to see monthly trends throughout the year across all broader categories
