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
