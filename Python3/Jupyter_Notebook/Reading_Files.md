## Reading Files with Python

This section covers Reading in Files using the Pandas Python library on Jupyter Notebook.

When importing the Pandas library, most people assign the alias 'pd' like this:

```
import pandas as pd
```

By using the pd.read_csv() function, the data is read from the file and formatted into a data frame. We use the "r" prefix before the path to make sure that it reads the data in quotes as raw data instead of getting tripped up by the periods and backslashes.

```
pd.read_csv(r"C:\Users\lizzy\JupyterNotebook\Files_to_Read\countries of the world.csv")
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/decbc7ae-e768-4023-9fc3-df7fedac42d9)



By right-clicking the copied path and Shift+Tab, you can see all the possible arguments for this read function:


![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/3b471bfb-8d21-4f59-8a38-19224073a154)

Because this is function specifics the file type is "csv", it will assume the file is separated by commas, but if we wanted to change that separator the "sep" condition would apply.
Headers, index columns, prefixes and much more can be specified by looking at the possible arguments with Shift+Tab.

To reference that file that we read in, you need to assign the read function result to a variable. 
Most people use 'df' which is commonly used to describe data frames.
By calling the 'df' variable, you can now see the values stored in the data frame.

![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/323ae802-dd0e-4f10-95f3-c95378af98f7)

When reading a text file, you can actually use the same function although you have to add conditions to avoid formatting issues like the ones below:

![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/77c054d0-164c-410d-b922-a0e58ff20c1d)

As you can see, there is a backslash separating the headers and "\t" separating the countries. This is where the separator argument comes into play.

![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/d6af5b8f-802d-46c4-a2ac-762c52ff142d)

While this method works, there is a proper way to deal with text files as well. 
The function to use is: pd.read_table() which is very versatile and works with many different file types (not just txt files).

![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/86256e38-cf53-47aa-a162-eee4f908dc40)

For JSON files, you can use the pd.read_json() function like so:

![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/c0f92870-5e06-4428-b370-32a66fe63ab2)

Excel files are a bit trickier because of the accumulation of multiple sheets per file. By default, it will only store the data on the first sheet in the data frame.

![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/0c3cb0fd-9ac4-4192-8aa1-65df3e9158c7)

To change which sheet is read, we can use the "sheet_name" condition which allows you to choose the name.

![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/5ab20526-ab66-459d-8a11-f81e3f208660)

To change the max number of rows pulled and displayed, we can use the pd.set_option() function which will make changes to the previous data frame.

```
pd.set_option("display.max.rows", 235)
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/159fcd2f-17a7-44d1-a6f4-a650e460bb92)

```
df4.info()
```
The above function shows the basic details regarding the data frame.

![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/df841511-3e7f-4984-94ab-e22e1c3f8d17)

```
df4.shape
```
Displays the number of rows and columns respectively:
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/65d498f3-70f4-4875-ae8d-b49a3fb4cbb9)


```
df4.head(<number of rows>)
```
The above function shows the top number of rows specified:
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/28bd73ec-3965-4a3f-97ac-a3f1a28fe7a5)


```
df4.tail(<number of rows>)
```
The above function is the exact opposite of head() so it shows the last number of rows:
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/f1cda9b9-d014-4ca9-ae54-0139ef424084)


```
df4['Column Name']
```
The above function displays the entire column in the data frame with a bit of info at the bottom:
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/8c6591ba-d04b-40ac-869a-dd7a87c48fec)

```
df4.loc[<row num>]
```
The above function pulls a single record from the data frame and provides the information in each column. It can also be used with string/char values:
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/34fe3896-741b-43eb-8dbb-d61df7facfa7)


```
df4.iloc[<row num>]
```
The above function is better than loc() function because whether the index changes or not, it will pull the integer value of the row num:
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/053d7e6c-5418-4028-8299-467e953f0979)
