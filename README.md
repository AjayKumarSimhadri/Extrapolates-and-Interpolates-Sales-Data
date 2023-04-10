# Extrapolates-and-Interpolates-Sales-Data
Create a function that Extrapolates and Interpolates Sales Data

The code reads a sales data file ('input.csv'), extrapolates the data by adding x months of data to each existing row, and saves the result to another file ('output_file'). The extrapolation stops at the 'max_date' parameter, which is a string in the format 'YYYYMM'.

It uses the pandas library to work with data frames. It starts by reading the input file into a data frame and converting the 'yearmonth' column into a datetime format. It then creates a new empty data frame to store the extrapolated data.

And then loops through each customer-product combination in the data frame and sorts the corresponding subset by 'yearmonth'. It then loops through each row in the sorted subset and adds it to the new data frame. For each row, it then adds x more rows, each representing a month after the current row's 'yearmonth', up to 'max_date' (or until there is already a row for that customer, product, and month).

Finally, it converts the 'yearmonth' column back to an integer format, drops duplicate rows, and sorts the data frame by 'customer', 'product', and 'yearmonth' before saving it to the output file.

It also includes a warning filter to suppress any warning messages that might arise during the execution.
