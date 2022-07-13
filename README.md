# Turnover analysis
Turnover analysis from 2019 to June, 2022 of a Brazillian chemistry industry. 

## Summary
This project was designed to check a hypothesis of an increased company's dismiss over time. To confirm and to find new information, it was gathered employee's dismisses information from company's ERP such as time in company, age in dismiss, sector and initiative. The tool to analyses the data was PowerBi. After modeling and fixing data corrections, a dashboard was created, and some results were found. It was found an increased dismissed caused by COVID-19 and a high resign ration in 'Business A'.

<a><img src="https://github.com/luiz-antonio-ck/people-analytics/blob/main/dashboard.png" /></a>

## Background
This report was made for a task in people analytics subject of an MBA course; therefore, this data is a fraction of the company's lifetime, real and made to be anonymous about the company and companies dismisses. There is no reference that can link to a person or recognize the company.

## Business Case
The main goal of this research was to find out about turnover rates and the causes. The HR team is not looking for individual culprits but problematic areas, leadership, time in company metrics, and age metrics that relate to the rates. 
People Analytics not only involves Human Resources, but also involves Data Analysis and Finance, or at least a business understanding instead of Finance.

### Business understanding
Only a few information was passed on to this data which are:
<ul>
<li> The business is a chemistry industry; </li>
<li> It has around 680 employees; </li>
<li> There are 3 major business sectors, A, B, and C; </li>
<li> Business A is most important sector; </li>
<li> The company has more than 30 years. </li>
</ul>

## Data Analysis
Gathering information from ERP called 'Senior Sistemas', it was able to retrieve dismissal from 2019 to June 2022 by employee's ID with the area, age in dismissal, time in company, initiative, admission date, and dismissal date in an excel table. Furthermore, it was gathered information about employees number by year by area in another excel table.

### Data preparation and modeling

Importing a excel table to PowerBi may require changing the encoding or program languange to recognize decimals, dates and names correctly. No problem wass
The first excel table only have information about dismissal in the period. There wasn't missing data, it had variations of the same thing, as area label like "Operation" and "Operations".
We received two fact tables that are not in usual database format, for examples, area aren't represent by area ID (foreign key) and a dimension table describing this area id (now primary key). To link both tables, it were build a calendar table using the dismissal tables and single column table with areas to be the link between fact tables.
There was also a third table received that indicated turnover by year which it was used as calculus reference.
The schema can be seen as following:
<a><img src="https://github.com/luiz-antonio-ck/people-analytics/blob/main/Schema.png" /></a>


... <em> under construction </em>
