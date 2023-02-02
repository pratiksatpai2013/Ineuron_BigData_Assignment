# PandasAssignment

Q1. How do you load a CSV file into a Pandas DataFrame?
Ans 1. CSV files contains plain text and is a well know format that can be read by everyone including Pandas.
```python
import pandas as pd

df = pd.read_csv('data.csv')

print(df)
```

Q2. How do you check the data type of a column in a Pandas DataFrame?
Ans 2. To check the data type in pandas DataFrame we can use the “dtype” attribute. The attribute returns a series with the data type of each column.
```python
result = df.dtypes
print(result)
```

Q3. How do you select rows from a Pandas DataFrame based on a condition?
Ans 3. The rows from a Pandas dataframe can be selected using various methods, one f the method is to use the function ".loc".
For example let's say in 'data.csv' there are two columns 'Student' & 'Marks', and we want all the rows that have Marks>60 -
```python
df_new = df.loc[df[Marks]>60]
df_new
```

Q4. How do you rename columns in a Pandas DataFrame?
Ans 4. Columns can be renamed inplace in the original dataframe using ".rename" function. For example in our case, if we want to change 'Marks' to 'MarksObtained' it can be done using
```python
df.rename(columns = {'Marks':'MarksObtained'},inplace = True)  --changed in the original dataframe
```

Q5. How do you drop columns in a Pandas DataFrame?
Ans 5. Columns can be dropped in Pandas dataframe using the ".drop" function.
```Python
df.drop(['MarksObtained'], axis = 1)  ---axis = 1 is for vertical i.e columns
```

Q6. How do you find the unique values in a column of a Pandas DataFrame?
Ans 6. To find unique values in columns of dataframe, we can use the ".unique" method.
```python
print(df["Students"].unique())
```

Q7. How do you find the number of missing values in each column of a Pandas DataFrame?
Ans 7. The number of missing values 'NaN' can be found in Pandas dataframe using "isna" function.
```python
count = df['MarksObtained'].isna().sum()
print(count)
```

Q8. How do you fill missing values in a Pandas DataFrame with a specific value?
Ans 8. The "fillna" method replaces the NULL values with a specified value.
```python
df = df.fillna(60)  ---The NaN values are filled with data '60'
```

Q9. How do you concatenate two Pandas DataFrames?
Ans 9. The "concat" function in pandas is used to append either columns or rows from one DataFrame to another.
```python
dataframe = [df1, df2]

result = pd.concat(dataframe)
display(result)
```

Q10. How do you merge two Pandas DataFrames on a specific column?
Ans 10. Two dataframes can be mergerd in pandas similar to how joins work in sql. The ".merge" heps to merge two dataframes and t can be mereged in three ways, either after merge the common elemenst of both the dataframes will be displayed, or either all in the left dataframe and matching ones in the right one can be displayed or vice versa.
For example, if I want to join two dataframes df1 and df2 based on a specific columns and the result will have an intersection of both the dataframes.
```python
df1.merge(df2[['Student', 'marks', 'Rank']])  ---merged based on the three columns mentioned
```

Q11. How do you group data in a Pandas DataFrame by a specific column and apply an aggregation function?
Ans 11. Dataframe.aggregate() function is used to apply some aggregation across one or more column. Aggregate using callable, string, dict, or list of string/callables. Most frequently used aggregations are:
sum: Return the sum of the values for the requested axis
min: Return the minimum of the values for the requested axis
max: Return the maximum of the values for the requested axis

Q12. How do you pivot a Pandas DataFrame?
Ans 12. The "pivot()"" function is used to reshaped a given DataFrame organized by given index / column values.
```python
df.pivot(index ='A', columns ='B', values =['C', 'A'])  ----index,values and columns are parameters for the pivot function
```

Q13. How do you change the data type of a column in a Pandas DataFrame?
Ans 13. The function ".astype" method is used to cast pandas object to a specified dtype. This function also provides the capability to convert any suitable existing column to a categorical type.
```python
# converting all columns to string type
df = df.astype(str)
print(df.dtypes)
```

Q14. How do you sort a Pandas DataFrame by a specific column?
Ans 14. We can sort the dataframe in ascending or descending order of the column values. To sort the rows of a DataFrame by a column, use ".sort_values()" method with the argument by=column_name. For example
```python
sorted_df = df.sort_values(by='MarksObtained', ascending=False)   ----ascending 'True' is sorting in ascending order and 'False' is vice versa
print(sorted_df)
```

Q15. How do you create a copy of a Pandas DataFrame?
Ans 15. Using the ".copy()" method, a dataframe can to copied into a new dataframe.
```python
newdf = df.copy()
print(newdf)
```

Q16. How do you filter rows of a Pandas DataFrame by multiple conditions?
Ans 16. Rows can be filtered in a pandas dataframe using the ".loc()" method, in this we can specify the conditions of filteration.
For example if we want to filter rows based on the fact that which student got marks more than 50, we can use,
```python
display(df.loc[(df['MarksObtained']>50)])
```

Q17. How do you calculate the mean of a column in a Pandas DataFrame?
Ans 17. The mean of a numerical value column can be calculated in pandas using the method ".mean()"
```python
df2 = df["MarksObtained"].mean()
```

Q18. How do you calculate the standard deviation of a column in a Pandas DataFrame?
Ans 18. can use the ".std()" function to calculate the standard deviation of values in a pandas DataFrame.
```python
df['MarksObtained'].std()
```

Q19. How do you calculate the correlation between two columns in a Pandas DataFrame?
Ans 19. Correlation is used to summarize the strength and direction of the linear association between two quantitative variables. It is denoted by r and values between -1 and +1. A positive value for r indicates a positive association, and a negative value for r indicates a negative association.
```python
# correlation between column 1 and column2
print(data['column1'].corr(data['column2']))
```

Q20. How do you select specific columns in a DataFrame using their labels?
Ans 20. To access specific columns of a DataFrame with their columns labels, directly use DataFrame[~] or use the DataFrame.loc property.


Q21. How do you select specific rows in a DataFrame using their indexes?
Ans 21. If you’d like to select rows based on integer indexing, you can use the .iloc function.
```python
df.iloc[[4]]  ----select the 5th row of the DataFrame
```

Q22. How do you sort a DataFrame by a specific column?
Ans 22. Pandas sort_values() method sorts a data frame in Ascending or Descending order of passed Column. It’s different than the sorted Python function since it cannot sort a data frame and particular column cannot be selected.
```python
rslt_df = df.sort_values(by = 'Name')
```

Q23. How do you create a new column in a DataFrame based on the values of another column?
Ans 23. can add/append a new column to the DataFrame based on the values of another column using df.assign(), df.apply(), and, np.where() functions and return a new Dataframe after adding a new column.

Q24. How do you remove duplicates from a DataFrame?
Ans 24. Pandas "drop_duplicates()"" method helps in removing duplicates from the Pandas Dataframe In Python.
```python
df.drop_duplicates(subset=None, keep=’first’, inplace=False)
```
Q25. What is the difference between .loc and .iloc in Pandas?
Ans 25. The main distinction between the two methods is:
loc gets rows (and/or columns) with particular labels.
iloc gets rows (and/or columns) at integer locations.
