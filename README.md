# PeopleBox Description
Internship Purpose

1. I have imported pandas, datetime and numpy.

2. df named DataFrame was created using input file path.

3. Then a user defined function is being created for converting each column based employee data to row based data.

4. # Explanation on User defined function
   1. User defined function will call for the particular table you want to be converted.
   2. To create col1, col2 and col3 I have used for loop which is still in column format data. col1 is for the whole data segregated as per word provided, col2 is for columns without dates of word and col3 is for columns with dates of word.
   3. df1 and df2 uses melt function in pandas is used to transform or reshape a DataFrame from a wide format to a long format.
   4. df2 column names have date in them but df1 doesn't have so i have first removed the date name from it and then used left merge to merge this column and saved in df3.
   5. df4 is used to sort values.
   6. df5 is the main dataframe where first employeee code and manager employee code and then inserted values calculated in df4.
   7. Now i have calculated effective date using following procedures:
      a. first making a blank dataframe
      b. Then i have used for loop stating if else condition for every employee and ordered them in order and if we don't have a value it will throw nan value out.
      c. after for loop saving values in dat[], I have used insert function and making a new column with those dates.
   8. Specifically for compensation i have added new loop to make Last compensation column. In that loop if you find next value of compensation you have to have the previous value as the answer for last compensation in front of next compensation value. When the value is calculated insert function is used to make a new column for last compensation.
   9. Last part is to return the value of df5 at the end of def function.
       
5. made three new tables from columnar based to row wise data (compensation, review, engagement) and merge them into a new table(df_merged_1).

6. I made a for loop in which in df if they identify a value in column ["Review", "Compensation", "Last Compensation", "Engagement"] they update that same value in all the next none cells available in["Review", "Compensation", "Last Compensation", "Engagement"] column.
   a. When they encounter a new value they stop the previous procedure of fitting the values and start again with the newly encountered value in that column.
   b. When the loop encounter a new "Employee Code", for loop stops for that employee as well and start the whole procedure with the new "Employee Code".
   c. User defined function is used and in the parameter of user defined function you have to give the name of the column you have to change.

7. df_merged_1 has updated the 4 values and after rearranging all columns, all that was left to calculate was end date.

8. Effective date was converted into date format before calculating End date.

9. End date was calculated using user defined function where following conditions were given:
   a. Ensuring the 'End Date' is one day before the next 'Effective Date' to avoid overlap.
   b. For the latest record of an employee, assign a far-future date (e.g., 2100-01-01) as the 'End Date'.
   c. Made it an iterative procedure for every employee but for employee 3 far future date as 2023-12-30.
   d. Then finally adding the column back in the data frame to make a new column.

10. Final_df is the data set that we need as our output file and i have also added an export file code for the output csv file.
