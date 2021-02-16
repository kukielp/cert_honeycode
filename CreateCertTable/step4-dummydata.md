# Load up dummy data

There are a two of ways to load up the dummy data:
1. Manual input of data
2. Upload bulk data

## 1. Manual input of data
Go to the ```certification``` table and click on the plus to create a new row, and fill in the fields "Name", "Manager" and "Status" - do this as many items as necessary. 

![certification](/images/certaddrow.png)

Now lets add a row into the "Practitioner table"
![certification](/images/practitioneraddrow.png)

Notice that the "Certification" table now has a value in the filter as the name in the two table match. Click on the filter with the 1 in it and it show the values associated. 

![certification](/images/filter.png)

To upload many rows, you can import a CSV file. 
An Example of this is below: 

``` bash
Fred Flinstone, Barny Rubble,,,,,,,Permanent
```
Click on the certication table, and the ... button and import data into this table. 

![certification](/images/import.png)

Choose the "csv" comma delimeted file to load.
![certification](/images/csv.png)

Click open, and untick "First row of imported data is column headers"
![certification](/images/columns.png)

This will not have inserted one row into the certification table. 
![certification](/images/fred.png)

Now lets insert dummy data into all the other tables and certification table as well.