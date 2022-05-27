# Numpy

1. Data Types

   - Data Types in Numpy

     | Sign | Type |
     | :--: |:--:|
     | i | integer |
     | b | boolean |
     | u | unsigned integer |
     | f | float |
     | c | complex |
     | m | timedelta |
     | M | datetime |
     | O | object |
     | S | string |
     | U | unicode string |
     |  V | fixed chunk of memory for other type(void) |
     
   - `dtype` : return the data type of the array
   	
   	- For `i`, `u`, `f`, `S`define the size
   		for example : `dtype='i4'` which means create an array with data type 4 bytes integer
   - Converting Data Type on Existing Arrays

     - `astype` : creates a copy of the array, and allows you to specify the data type as a parameter

2. Copy and View

   - The DIfference Between Copy and View
     - The copy is a new array, and the view is just a view of the original array.
     - The copy *owns* the data and any changes made to the copy will ==not affect== original array, and any changes made to the original array will not affect the copy
     - The view *does not own* the data and any changes made to the view will ==affect== the original array, and any changes made to the original array will affect the view
   - Check that copies *owns* the data, and views *does not own* the data.
     - Every NumPy array has the attribute `base` that returns `None` if the array owns the data. Otherwise, the `base` attribute refers to the original object

3. Numpy Array Reshaping

   - Return Copy or View ?

     - reshape returns the original array, so it is a **view**

   - Unknown Dimension

     - Pass `-1` as the value, and NumPy will calculate this number for you

       *We can not pass `-1` to more than one dimension*

   - Flattening the arrays
     - use `reshape(-1)` to flatten array which means converting  a multidimensional array into a 1-D array

4. Numpy Array Iterating

   - Iterating Arrays Using Function `nditer()`
     - `np.nditer(arr)` :  iterating through each scalar of an array
   - Iterating Array With Different Data Types
     - Use `op_dtypes` argument and pass it the expected datatype to change the datatype of elements while iterating. Numpy does ==not change== the data type of element in-place(where the elements is in array)
     - It needs some other space to perform this action, that **extra space** is called `buffer`, 
     - and in order to enable it in `nditer()` we pass `flag=['buffered']`
   - Iterating WIth Different Step Size
     - `np.nditer(arr[:, ::2])` : step size = 2
   - Enumerated Iteration Using `ndenumerate()`
     - Get corresponding index of the element while iterating
     - `for idx, x in np.ndenumerate(arr):` : Enumerate on ND array's elements

5. Numpy Joining Array

   - **means** : putting contents of two or more arrays in a single array
   - in NumPy we join arrays by ==axes==
   - We pass a sequence of arrays that we want to join to the `concatenate()` function, along with the ==axis.== If axis is not explicitly passed, it is taken as 0
     - `np.concatenate((arr1, arr2), axis=0)`
   - Joining Array Using Stack Functions
     - Stacking is same as concatenation, the only difference is that stacking is done along a new axis
     - We pass a sequence of arrays that we want to join to the `stack()` method along with the axis. If axis is not explicitly passed it is taken as 0
     - Stacking Along Rows
       - `np.hstack((arr1, arr2))`
     - Stacking Along Columns
       - `np.vstack((arr1, arr2))`
     - Stacking Along Height (depth)
       - `np.dstack((arr1, arr2))` : *like `np.stack((arr1, arr2), axis=1)`*

6. Numpy Splitting Array

   -  Splitting breaks one array into multiple

   - We use `array_split()` for splitting arrays, we pass it the array we want to split and the **number** of splits

     - `np.array_split(arr, 3)`

       *The return value is an array containing three arrays*

     - If the array has **less elements than required**,  it will **adjust from the end **accordingly

       *We also have the method `split()` available but it will not adjust the elements when elements are less in source array for splitting.  `array_split()` worked properly but `split()` would fail*

   - Split Into Arrays

     - The return value of the `array_split()` method is an array containing each of the split as an array.you can access them from the result just like any array element

       ```
       newarr = np.array_split(arr, 3)
       newarr[0]
       newarr[1]
       newarr[2]
       ```

     - In addition, you can specify which axis you want to do the split around

       `newarr = np.array_split(arr, 3, axis=1)`

     - An alternate solution is using `hsplit()` opposite of `hstack()`

       `newarr = np.hsplit(arr, 3)`

7. Numpy Searching Arrays

   - Searching Arrays

     - search an array for a certain value and return the indexes that get a match

     - To search an array, use the `where()` method

       - `x = np.where(arr == 4)`

         *return the **tuple** which is present at ==indexes==*

   - Search Sorted

     - `searchsorted()` which performs a binary search in the array, and returns the index where the specified value would be ==inserted== to **maintain the search order**

       - `x = np.searchsorted(arr, 7)`

       *The `searchsorted()` method is assumed to be used on **sorted arrays***

       *By default the left most index is returned, but we can give `side='right'` to return the right most index instead*

       - `x = np.searchsorted(arr, 7, side='right')`

     - Search Multiple Values

       - To search for more than one value, use an array with the specified values

         - `x = np.searchsorted(arr, [2, 4, 6])`

           *The return value is an array containing the three indexes where 2, 4, 6, would be inserted in the original array to maintain the order*

8. Numpy Sorting Arrays

   - Sorting Arrays

     - `np.sort(arr)`

       *This method returns a copy of the array, leaving the original array unchanged*

       *If you use the `sort()` method on a 2-D array, both arrays will be sorted*

9. Numpy Filter Array

   - Filtering : Getting some elements out of an existing array and creating a new array out of them

     *filter an array using a **boolean** index list*

     *If the value at an index is `True` that element is contained in the filtered array, if the value at that index is `False` that element is excluded from the filtered array*

   - Creating Filter Directly From Array

     - ```
       filter_arr = arr > 42
       
       new_arr = arr[filter_arr]
       ```

       
