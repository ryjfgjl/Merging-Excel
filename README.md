
# Merging data from multiple Excel files

In our work, we often receive Excel tables with data in the same format. If we want to analyze these data, it can be difficult to analyze them because the data is spread across multiple Excel files or multiple sheets.  At this point, we need to merge them into one Excel file or into a database for analysis and processing.

## Example
As shown in the figure, we need to merge the data from four Excel files into one.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/16aqpjpusrj2ylxy4ic3.png)



The headers of the files are the same, except for the data.  Even if the headers are different, you can choose to ignore or add different columns

## Using the ExcelToDatabase tool
Select the files to be merged, manually specify the target table, and enter the table name or select a table that already exists in the database

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/yta4xovrhh2g1jwpw67k.png)



Wait a moment, and you can view the merged data in the database

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/0tr959d5cm0016un4l77.png)


Although the data is merged here, how can we distinguish which file each row of data comes from?
Select the Overwrite option in the import mode, switch to the database options interface, and fill in the Excel file name to be saved to the field

After re-importing the data, you can see that a new field has been added to the table

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/san0k8bfusuc1l8prkob.png)


Here, the full name of the Excel file is added to the end of each row of data.  What if you only want to save the date inside the file name?
Select the import mode as "reconstruction", save the Excel file name (which can be extracted using regular expressions) to the column, select the date (YYYYMMDD), and fill in the field name with the date.  If you want to extract other characters, you can write your own regular expression to extract them.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/u5g5td49c5p9f885ic9c.png)


View the data again

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/0jz5j0a14szrfsgyv7dq.png)


## Introduction and Download of ExcelToDatabase

- 
[ExcelToDatabase - Automation tool for batch importing Excel files into database](https://github.com/ryjfgjl/ExcelToDatabase/blob/master/README.md)
 
