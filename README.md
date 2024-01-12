# Football-Transfers-Analysis-in-Excel-Project
This project is a detailed analysis of international football transfers, delving into the economic patterns that characterize player movements between associations. It offers an exhaustive look at the financial dynamics of the global football scene, also known to those in the US as soccer.

## Task Description
In this project, I was given a comprehensive dataset ([project-files-football-transfers-analysis-in-excel (1).zip](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/files/13923735/project-files-football-transfers-analysis-in-excel.1.zip)) that spans the football seasons of 2021/2022 and 2022/2023. My role involved conducting a variety of essential tasks within Excel. This included data preprocessing and manipulation, applying filters, demonstrating proficiency with Excel functions, and creating visual representations of the data.

I mapped out the transfer of players between countries and across various football associations. My work also involved creating summary tables to visualize these transfers, calculating the net transfer movements, and ascertaining the total financial amounts of these transactions.

This project presented me with a unique opportunity to combine my passion for football with my interest in data analysis, leading to a deeper appreciation of the football economy on a global scale. Whether as a football enthusiast, a data analysis student, or both, I found this Excel project to be quite enlightening. It provided me with intriguing insights and a new perspective on the beautiful game. It was the perfect project to apply and validate the Excel skills I had learned in my Introduction to Excel course.

# Solution
## Part 1: Database Review
Start by splitting the data in the Countries sheet using Excel’s Text-to-Columns tool. Choose the Delimited file type and select 'comma' as your delimiter.
![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/f4ddd686-be53-4266-b5de-a0cc1672f3af)

Next, clean up the continent names in the list by removing any extra spaces. Start by making a copy of the list and then removing any duplicate values.
![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/62e0db49-d610-4c9b-b112-449c3501c67f)

Use Excel's Find and Replace tool to remove spaces at the start of every continent name.
![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/76fc0c93-b9e2-4f90-bad9-6a4b81815cd5)

Now, switch to the Database sheet. Apply a filter at the top of the table and open the filter for the Season column.
![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/0e11cdb7-dd57-4f82-bdcb-6c88d028ab8c)

Look for entries that read 2022/2028 and replace 2028 with 2023 using Find and Replace.
![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/f3ff4f60-7dc4-4556-8cb2-55769d7eae64)
Note: Select the Season column before using Find and Replace. If you don't specify a range, Excel will make changes throughout the entire sheet, which could result in unintended changes.

Finally, fill in the Continent columns in the Database sheet. You can use Excel’s VLOOKUP or XLOOKUP function to do this.

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/b9d8ca16-5a96-4690-a105-619c5f208788)

## Part 2: Analyze the Aggregate Number of European Transfers
For the project’s next phase, we'll need to create a table whose layout should look like the following:

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/ed4d842a-0ed6-488e-a05e-e2dd396c5465)

To populate this table, we'll use Excel’s SUMIFS function to add data based on multiple criteria. Our criteria include the following:

- The season (2021/2022 and 2022/2023)

- The continent (Europe)
  ![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/e7bad16b-fcc6-43ef-a0ab-fb80e9943825)

When filling in the 'Transfers outgoing' row, remember to 1) adjust the database column to correspond with outgoing transfers and 2) place a minus sign in front of the SUMIFS function. This will automatically convert outgoing transfers into negative numbers, making it easier to calculate the net movement of players.

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/9d54acd9-6b38-4547-9b5d-c61079d28575)

## Part 3: Analyze European Transfers by Country
In this portion of the project, we aim to construct a more comprehensive table. This table will illustrate the quantity and the financial worth of player transfers in and out of Europe.

First, we need to set up the structure of our table. After which, we'll use Excel’s SUMIFS function to fill it in.

Navigate to the Countries sheet and apply a filter specifically for European countries. Copy all European countries in the list:

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/6dacf03f-d7f9-49c7-ae5d-cc9d0e48136f)

Create a new sheet called European Transfers by Country. The layout of the table should look like the following:

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/715c10e0-7480-406f-b5f7-4f2c86339032)

When setting up the SUMIFS function, remember how you fix the cell references. This way, you can reuse the function multiple times with ease.

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/cdd47b43-82ee-458f-af8c-b6d1e3e9ce51)

Remember that you'll need to tweak some parameters in the SUMIFS function when you're calculating outgoing transfers and working out the monetary value of transfers.

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/c11a9ec3-2dc1-47c9-80fb-e83da028151b)

Include a minus sign for outgoing transfers, indicating that these transfers reduce the net inflow of players to a particular country.

Adjust the column to be summed accordingly when figuring out the monetary value.

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/6205e6f9-9f79-49cc-b3aa-670158430478)

Once you've calculated all the 2021/2022 season figures, you can apply the exact formulas for the 2022/2023 season. Just paste them in.

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/5ae1ac53-b749-43a2-8bbc-7440a878d5b3)

## Part 4: Visualize Transfer Fees of Top 5 European Countries
In the European Transfers by Country sheet, we'll use the RANK function to identify the five countries with the most significant incoming transfer values.

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/16a9aeb7-01c9-4f53-b5ca-71bd417256b7)

The RANK function needs the following two inputs:

1) Cell to be ranked
2) Range of cells it’s being ranked in
Apply this formula to all cells, and we'll find our top spenders: England, Italy, France, Germany, and Spain.

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/8b34dddf-d6b0-433b-a26e-e3e339943a81)

Next, we'll organize our data for visualization. Create a new sheet named Visualization Top 5 Countries. Set up a table that needs to be filled in.

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/819eb31d-cf7b-4e42-b045-6d0cbd4d90ef)

We can fill this table in using Excel formulas. To get the number of incoming transfers for each country, use a simple SUMIF function. To calculate the average transfer fee, divide the total value of incoming transfers by the number of transfers.

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/92f32f41-b420-4296-8720-e6d6c122c632)

To calculate the average transfer fee, divide the total value of incoming transfers by the number of transfers.

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/299986f0-4260-4133-9d58-c107ee1eae99)

This data shows that English clubs lead the pack in volume and cost, spending more than $2 million on average per transfer.

Let’s create the visualization required.

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/1a47b1ca-c009-4d90-8297-f9bc49ab9c3d)

Then you can drag the ‘average transfer fee’ data to add it to the chart.

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/15390679-109d-4c25-b82d-a08f7d44a156)

Because the two variables have different scales, the ‘average transfer fee’ completely dwarfs the ‘# of incoming transfers,’ so we need to add a secondary axis that shows ‘average transfer fees’ per country separately.

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/68c139a6-5252-4a2d-942a-c5f271a500ed)

Once we’ve opted for the secondary axis, we can change the chart type and choose Line.

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/2971ed70-ca66-461d-8e31-dc5ae7f8c299)

The formatting touches I would perform on this chart include the following:

Change font and font size
Add transparent background (no fill)
Remove the border line
Adjust the gap width from 219% to 70%.
Change the color of the two series in the chart
Smooth line
Add a meaningful title and axis titles

![image](https://github.com/Kelechi-Okezie/Football-Transfers-Analysis-in-Excel-Project/assets/141277019/060ddead-686d-48dc-8732-db59552a25d2)





















