# Creation of the main table, and pulling in data from other tables.

The first thing we need to do is to create a main table. 

This table will be used to hold the main components of a team member, and i have a series of requirements i need to meet. 

1. I need to know who the persons manager is, so i can track their number of people certified in their role. This will enable me to gamify it later when we start the education. The first manager with the most certifications or all their team certified will be put in lights. 
2. I need to know the person name.
3. I need to know what certifications the person has, so i want to get the certification code link to provide evidence they got certified
4. I want to know if the person is a consultant or a contractor in the organisation
5. I want to be able to start with 1 certification, but be able to add more in should i need to. AWS has currently 11 certifications, but this may change, so the requirement will be to add more to it.
6. I want to send out an email to a user when someone gets certified. 

To create the certification table, on your "My Drive" click on certifications and it will create a new table called "Table1". 

![Create workbook](/images/table1.png)

Lets now add the required columns we need based on the above criteria. 

Change the table to look like the following: 
|Current   |New value  |
|---|---|
|Table1    |certifications   |
|Column1   |Name   |
|Column2   |Manager   |
|Column3   |Practitioner   |
|Add columns   |  
|---|
|ArchAss  |   
|DevAss      | 
|SysOpsAss   |  
|DevPro   |  
|ArchPro   |  
|Status   |  


Your Table1 should now be called certifications table, and look like the image below: 

![certification](/images/certification.png)

Congratulations, you have created your first table. Now we need to populate the associated certificate tables

To create a new table click on the table bar and add 6 new tables: 

![certification](/images/newtabcreate.png)

Click ```add a blank table```

You will be doing this a total of 6 new tables. Each table, change its name to the list below, and add columns to it - ``` Name Date Value ```
 
![certification](/images/assarch.png)

- AssArch
- AssDev
- AssSysOps
- Practitioner
- ProDevOps
- ProArch

AssArch will look like : 
![associate architect](/images/assarch.png)

## Filter creation

To do this we will be using a function in the table which will filter out the required row.  This Filter  will be linked to the other tables based on the name. 

![table joins](/images/certs.png)

On the tables bar, click on the certification table. 

Highlight the full column for practioner right click and choose format - 

![format ](/images/format.png)

Put the following formula in the Format field - 
```=FILTER(Practitioner,"Practitioner[Name]=[Name]")```

![formula ](/images/practformula.png)

Continue this for all the other 6 columns : 
| ColumnName | TableName | Formula |  
|---|---|---|
|Practitioner| Practitioner | ```=FILTER(Practitioner,"Practitioner[Name]=[Name]")```
|ArchAss  |  AssArch | ```=FILTER(ProArch,"ProArch[Name]=[Name]")```
|DevAss      | AssDev |```=FILTER(AssDev,"AssDev[Name]=[Name]")```
|SysOpsAss   |  AssSysOps |```=FILTER(ProArch,"ProArch[Name]=[Name]")```
|DevPro   |  ProDevOps |```=FILTER(ProDevOps,"ProDevOps[Name]=[Name]")```
|ArchPro   | ProArch |```=FILTER(ProArch,"ProArch[Name]=[Name]")```

Lets now put in some Data to test that the filter is working. 

Go to the certification tables, and create a new row with your name
