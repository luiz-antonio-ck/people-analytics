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

Importing an excel table to PowerBi may require changing the encoding or program language to recognize decimals, dates, and names correctly. 
The first excel table only has information about dismissal in the period. There wasn't missing data, it had variations of the same thing, as area labels like "Operation" and "Operations".

We received two fact tables that are not in the usual database format, for example, areas aren't represented by area ID (foreign key) and a dimension table describing this area id (now primary key). To link both tables, it was built a calendar table using the dismissal tables and a single-column table with areas to be the link between fact tables.

There was also a third table received that indicated turnover by year which was used as a calculus reference.

The schema can be seen as follows:

<a><img src="https://github.com/luiz-antonio-ck/people-analytics/blob/main/Schema.png" /></a>

## Results found
Dismissal over time, area with most resign, 2020 it was the good bye of old workers
### Dismissal over time
The year 2020 was the hardest year, especially the second trimester with 70 dismissals. For reference, combining the entire years of 2019 and 2021, there are **92** dismissals.

Employees:
|Start|Finish|***Dismissal***|Admission|
|-----|------|---------|---------|
|719|632|***110***|23|

Graphically we can see this:

<a><img src="https://github.com/luiz-antonio-ck/people-analytics/blob/main/Dismissal_over_time.png" /></a>

First trimester -> 21 dismissals
Second trimester -> 70 dismissals

It also breaks down the hypothesis that in 2022 the enterprise was firing up too much, and there is no significant increase in the line.

### Business A, the most resigned area

After knowing the ‘business A’ is the most key area of the company, it is a bad sign to see as the most resigned area. This area has 21 of 56 (37,5%) resign within this period, even having only an average of 23% of the company's employees. This is a strong alert to check why people are resigning.

<img src="https://github.com/luiz-antonio-ck/people-analytics/blob/main/Business_A.gif" alt="" style="max-width: 100%; display: inline-block;" data-target="animated-image.originalImage">

### Pandemic impact
First, let’s define here 2020 and 2021 as pandemic years. In the year 2021, dismissals numbers are less than number of years of 2019, so there isn’t a significant impact perceived.  There were 44 dismissals and 49 admissions, it may indicate a good year and a good adaptation to the pandemic.

In the year 2020, it is clear a great impact in company operations; company may had achieved a new record in dismissals.  Aggregating employees by years in company in group, we found out that the group with “more than 10 years” was the most affected. Perhaps, forced retirement or decrease in paycheck costs, but no data to support any hypothesis about company’s taken(achieved) strategy.

<img src="https://github.com/luiz-antonio-ck/people-analytics/blob/main/Turnover_2020.gif" alt="" style="max-width: 100%; display: inline-block;" data-target="animated-image.originalImage">

## What to do with all these metrics and findings?

After a group discussion in class, a plan was prepared to reduce company’s dismissals.
This plan was prepared to improve human resources process that it didn't exist or was outdated. As only a few persons work at this company the plan was summarized to these actions:

<ul>
<li> Implement discussed was to ask those who are resigning why there are doing formally as process; </li>
<li> Learn best practices for employee journey; </li>
<li> Train employees and leadership for these best practice; </li>
<li> Build a ‘persona’ for each area;  </li>
<li> Research and to define area culture; </li>
<li> Train leadership to improve cultural fit recognition. </li>
</ul>

The first area to receive these actions is ‘Business A’ due to company’s importance.

## What's next?

Monitoring turnover, especially in targeted area is key to check plan’s effectiveness.
It was established to review the turnover every three months.
