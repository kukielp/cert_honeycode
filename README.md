# Honeycode certification app and data
How to create a certification website using honeycode

## Requirements: 

```
You have been asked to provide a way to track all your teams from a manager level to show how many have got certified. Your organisation has just decided to invest in your technical teams and are providing training courses, online content and free vouchers in order to uplift your organisation to meet your requirements. 

Your manager has asked you to go and do a PoC (proof of concept), and you have heard of Honeycode as a potential option to do this.
You are already familiar with spreadsheets and forumla's, but you need to enable individuals to track their own details.
```

## Must haves:

1. I need to know who the persons manager is, so i can track their number of people certified in their role. This will enable me to gamify it later when we start the education. The first manager with the most certifications or all their team certified will be put in lights. 
2. I need to know the person name.
3. I need to know what certifications the person has, so i want to get the certification code link to provide evidence they got certified
4. I want to know if the person is a consultant or a contractor in the organisation
5. I want to be able to start with 1 certification, but be able to add more in should i need to. AWS has currently 11 certifications, but this may change, so the requirement will be to add more to it.
6. I want to send out an email to a user when someone gets certified. 

## Setup instructions:

1. Create a honeycode account [Create account](HoneyCodeAccCreate.md). You can also share this with other team members by inviting them to collaborate. Note that there are limitations on the free tier account to 20 people, however this can be implemented with SAML if required, but more on that on FAQ's.
2. Create a honeycode workbook [Create workbook](CreateWorkbook/certificationworkbook.md)
3. Create certification table, explain data setup. [Create certification table](CreateCertTable/certificationtable.md)
4. Create all certification table types, in this example we have AWS certifications we want to track which are Practitioner, Associate Architect, Associate Developer, Associate SysOps, Professional Architect and Professional DevOps. [Create certification table](CreateCertTable/createcertlevel.md)
5. Create a filter which will communicate to the main certification table. [Create filters](CreateCertTable/filtercreation.md)
7. Create some dummy data. 
8. Create main first page listing ALL people in the cerification table
9. Create first hidden button to do a formula on ALL people 
10. Create all certification buttons on main page to only show people who are certified in a specific filter value. 
button which shows all of the people certified
11. Create a link page to another page and allow Inputs to go to new page
12. Create a new button to use the input and a hidden value.
13. Complete all of the lists for all of the voucher versions 
14. Create a Insert new user page into the app
