## Create other tables which will FILTER into the main Certification table

With the main table, there are a couple available. In this lab we will explain how we can ```FILTER``` to other tables which will pull in those values. 

As discussed earlier we want to show which certifications the employee has got, so we will now create 6 new tables all with the same details in them. 

We are going to now add 6 new tables each of them with the following columns in. Where Name is employee name, date is date of certification, and value is the unique value provided by the AWS testing centre. 

|Name   |Date   |Value  |

Name will be used as our primary filter.

As an alternative to this, a more scalable solution would be to  create 1 table and have an additional column called CertName and filter based off of this. This would scale better, but in this example we will just do the 6 tables for demonstration purposes. 

To create a new table click on the table bar and click the ```+```: 

![certification](/images/newtabcreate.png)

Click ```add a blank table```
 
![certification](/images/assarch.png)

Call the table AssArch, add in the columns ```Name Data Value```

![associate architect](/images/assarch.png)

Repeat so you now have a total of 6 new tables created with the table names below: 

- AssArch
- AssDev
- AssSysOps
- Practitioner
- ProDevOps
- ProArch

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
