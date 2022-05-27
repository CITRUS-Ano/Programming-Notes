# Pandas

1. Pandas Getting Started

   - ```
     import pandas
     
     mydataset = {
     	'cars': ['BMW', 'Volvo', 'Ford'],
     	'passings': [3, 7, 2]
     }
     
     myvar = pandas.DataFrame(mydataset)
     ```

2. Pandas Series

   - Series

     - A Pandas Series is like a column in a table. It is a one-dimensional array holding data of any type

     - ```
       a = [1, 7, 2]
       myvar = pd.Series(a)
       ```

   - Labels

     - If nothing else is specified, the values are labeled with their index number. First value has index 0, second value has index 1 etc

       `myvar[0]`

   - Create Labels

     - `myvar = pd.Series(a, index=["x", "y", "z"])`
     - `myvar["y"]`

   - Key/Value Objects as Series

     - ```
       calories = {"day1": 420, "day2": 380, "day3": 390}
       myvar = pd.Series(calories)
       ```

       *The keys of the dictionary become the labels*

       *To select only some of the items in the dictionary, use the `index` argument and specify only the items you want to include in the Series*

     - `myvar = pd.Series(calories, index = ["day1", "day2"])`

   - DataFrames

     - Data sets in Pandas are usually multi-dimensional tables

       *Series is like a column, a DataFrame is the whole table*

       ```
       data = {
       	"calories": [420, 380, 390],
       	"duration": [50, 40, 45]
       }
       
       myvar = pd.DataFrame(data)
       ```

3. Pandas DataFrames

   **A Pandas DataFrame is a ==2 dimensional== data structure, like a 2 dimensional array, or a table with rows and columns**

   - Locate Row

     - Pandas use the `loc` attribute to return one or more specified ==row(s)==

       `df.loc[0]`

       *This example returns a Pandas **Series***

       `df.loc[[0, 1]]`

       *When using `[]`, the result is a Pandas **DataFrame***

   - Named Indexes

     - With the `index` argument, you can name your own indexes

       `df = pd.DataFrame(data, index = ['day1', 'day2', 'day3'])`

   - Locate Named Indexes
     - `df.loc["day2"]`

   - Load Files Into a DataFrame

     - If your data sets are stored in a file, Pandas can load them into a DataFrame

       `df = pd.read_csv('data.csv')`

4. Pandas Read CSV

   - Read CSV Files

     - use `to_string()` to print the entire DataFrame

       ```
       df = pd.read_csv('data.csv')
       
       print(df.to_string())		# to_string will show all data
       # print(df)
       ```

   - max_rows

     - check your system's maximum rows with the `pd.options.display.max_rows` statement

       `print(pd.options.display.max_rows)`

       *In my system the number is 60, which means that if the DataFrame contains more than 60 rows, the `print(df)` statement will return only the headers and the first and last 5 rows*

5. Pandas Read JSON

   - Read JSON

     - Big data sets are often stored, or extracted as JSON

       `df = pd.read_json("data.json")`

   - Dictionary as JSON

     - JSON objects have the same format as Python dictionaries

     - If your JSON code is not in a file, but in a Python Dictionary, you can load it into a DataFrame directly

       ```
       data = {
         "Duration":{
           "0":60,
           "1":60,
           "2":60,
           "3":45,
           "4":45,
           "5":60
         },
         "Pulse":{
           "0":110,
           "1":117,
           "2":103,
           "3":109,
           "4":117,
           "5":102
         },
         "Maxpulse":{
           "0":130,
           "1":145,
           "2":135,
           "3":175,
           "4":148,
           "5":127
         },
         "Calories":{
           "0":409,
           "1":479,
           "2":340,
           "3":282,
           "4":406,
           "5":300
         }
       }
       
       df = pd.DataFrame(data)
       ```

6. Pandas - Analyzing DataFrames

   - Viewing the Data

     - One of the most used method for getting a quick overview of the DataFrame, is the `head()` method

     - The `head()` method returns the headers and a specified number of rows, starting from the top

       - `df.head(10)`

         *Get a quick overview by printing the first 10 rows of the DataFrame*

       - `df.head`

         *Get a quick overview by printing ==all== rows of the DataFrame*

       - `df.head()`

         *if the number of rows is not specified, the `head()` method will return the ==top 5== rows*

     - There is also a `tail()` method for viewing the *last* rows of the DataFrame

       `df.tail()`

     

     

     
