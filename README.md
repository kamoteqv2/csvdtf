# csvdtf

This script, named csvdtf.exe, is designed to process a CSV file that contains a column for the timestamp (in seconds since the epoch). 

The script will read in the data from the specified CSV file, convert the timestamp column to a formatted datetime column, and then add the converted datetime as a new column to the data. The script will then export the processed data to a new CSV file with the added datetime column. 

To use the script, the user must run it from the command line and specify the input CSV file as a command line argument, for example:
 
**How to use:**

```
csvdtf.exe <inputfile.csv> <output.csv>
```
Note that the script is only able to process CSV files that contain a column with the header "timestamp" in seconds since the epoch.
 
