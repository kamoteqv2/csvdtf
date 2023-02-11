# csvdtf

This script, named csvdtf.exe, is designed to process a CSV file that contains a column for the timestamp (in seconds since the epoch). 

The script will read in the data from the specified CSV file, convert the timestamp column to a formatted datetime column, and then add the converted datetime as a new column to the data. The script will then export the processed data to a new CSV file with the added datetime column. 

To use the script, the user must run it from the command line and specify the input CSV file as a command line argument, for example:
 
**How to use:**

```
csvdtf.exe <inputfile.csv> <output.csv>
```
Note that the script is only able to process CSV files that contain a column with the header "timestamp" in seconds since the epoch.

**Sample CSV**


```
c:\csvdtf>type sample.csv
timestamp,temperature,humidity
1675950780,20.5,45
1675951140,21.0,47
1675951200,20.8,46
1675951260,20.7,48
1675951680,20.3,44
```

```
c:\csvdtf>***csvdtf.exe*** --input sample.csv  --output sample_out.csv
```

```
c:\csvdtf>type sample_out.csv
timestamp,temperature,humidity,datetime
1675950780,20.5,45,2023-02-09 13:53:00
1675951140,21.0,47,2023-02-09 13:59:00
1675951200,20.8,46,2023-02-09 14:00:00
1675951260,20.7,48,2023-02-09 14:01:00
1675951680,20.3,44,2023-02-09 14:08:00
``` 
