# PeopleBox Description
Internship Purpose

1. I have imported pandas, datetime and numpy.
2. df named DataFrame was created using input file path.
3. Then a user defined function is being created for converting each row based employee data to column based data.
4. # Explanation on User defined function
   1. User defined function will call for the particular table you want to be converted.
   2. To create col1, col2 and col3 I have used for loop which is still in row format data. col1 is for the whole data segregated as per word provided, col2 is for columns without dates of word and col3 is for columns with dates of word.
   3. df1 and df2 uses melt function in pandas is used to transform or reshape a DataFrame from a wide format to a long format.
   4. df2 column names have date in them but df1 doesn't have so i have first removed the date name from it and then used left merge to merge this column.
   5. 
   
