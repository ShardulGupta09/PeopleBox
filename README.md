# PeopleBox Description
Internship Purpose

1. I have imported the pandas, datetime, and numpy libraries.

2. A DataFrame named 'df' was created using the input file path.

3. Then, a user-defined function is being created to convert each column-based employee data to row-based data.

4. # Explanation on User defined function

   1. User defined function will call for the particular table you want to be converted.
   2. To create col1, col2 and col3 I have used for loop which is still in column format data. col1 is for the whole data segregated as per word provided, col2 is for columns without dates of word and col3 is for columns with dates of word.
   3. df1 and df2 uses melt function in pandas is used to transform or reshape a DataFrame from a wide format to a long format.
   4. df2 column names have date in them but df1 doesn't have so i have first removed the date word. Then used left merge to join these column and saved in df3.
   5. 'df4' is utilized to sort values.
   6. 'df5' is the main DataFrame where the first employee code and manager employee code are inserted, along with the values calculated in 'df4'.
   7. The effective date is calculated using the following procedures:
      a. First, a blank DataFrame is created.
      b. Then, a for loop with an if-else condition is used for every employee to order them and handle cases where values are missing.
      c. After the for loop, values are saved in 'dat[]'. The 'insert' function is used to create a new column with those dates.
   8. Specifically for compensation, an additional loop is added to create the 'Last compensation' column. In this loop, if the next value of compensation is found, the previous value is assigned as the answer for the last compensation in front of the next compensation value. When the value is calculated, the 'insert' function is used to create a new column for the last compensation.
   9. The final step is to return the value of 'df5' at the end of the defined function

5. Three new tables were created by transforming columnar-based data to row-wise data (compensation, review, engagement), and they were merged into a new table named 'df_merged_1'.

6. A for loop was implemented wherein, in DataFrame 'df', if a value was identified in the columns ["Review", "Compensation", "Last Compensation", "Engagement"], it was updated in all the subsequent empty cells in the ["Review", "Compensation", "Last Compensation", "Engagement"] columns.
   a. Upon encountering a new value, the procedure of fitting values in subsequent cells was halted, and it restarted with the newly encountered value in that column.
   b. When the loop encountered a new "Employee Code", it ceased for that employee as well, and the entire procedure restarted with the new "Employee Code".
   c. A user-defined function was utilized, and in the parameter of the user-defined function, you need to provide the name of the column you intend to change.

7. 'df_merged_1' has updated the four values, and after rearranging all columns, the only remaining task was to calculate the end date.

8. The effective date was converted into a date format before calculating the end date.

9. The end date was calculated using a user-defined function with the following conditions:
   a. Ensuring that the 'End Date' is set one day before the next 'Effective Date' to avoid overlap.
   b. For the latest record of an employee, a far-future date (e.g., 2100-01-01) was assigned as the 'End Date'.
   c. It was made an iterative procedure for every employee, but for employee 3, a far-future date was set as 2023-12-30.
   d. Finally, the column was added back into the DataFrame to create a new column.

10. 'Final_df' is the dataset required as our output file, and I have also included code to export the DataFrame to an output CSV file.
