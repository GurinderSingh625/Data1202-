# Data1202
The code starts by importing necessary libraries such as NumPy, Pandas, SQLAlchemy, and PyMySQL. 
It then proceeds to read a CSV file ('youtube_dataset.csv') and creates a Pandas DataFrame ('df_youtube') using the 'read_csv' function. 
The first 5 rows of the DataFrame are previewed using the 'head' function, and the 'info' function is used to show details about the DataFrame's column names, data types, and non-null count.
The code creates a new DataFrame ('df_first_1000_rows') by selecting the first 1000 rows of 'df_youtube'. 
It defines a function ('distribution') to get the distribution of a specific column in a DataFrame and uses it to create a new DataFrame ('df_dist') by calling the function with the 'df_first_1000_rows' DataFrame and the 'channeltype' column name.
The 'df_first_1000_rows' DataFrame is saved to a CSV file named 'youtube_top_1000.csv'. 
It then creates an SQLAlchemy engine with the database connection details using 'create_engine' function.
The code selects the first 10 rows of 'df_first_1000_rows' to create a new DataFrame ('df_10') and writes it to a MySQL database table named 'df_10' using the 'to_sql' function. 
The column data types are specified using the 'dtype' parameter, and if the 'if_exists' parameter is set to 'replace', it replaces the existing table with the same name, if any.
