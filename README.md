# Provide Insights to the Revenue Team in the Hostility Domain

## Overview
This project focuses on AtliQ Grands, a renowned company operating a chain of luxury five-star hotels throughout India. Unfortunately, AtliQ Grands is currently facing fierce competition, and their market share and revenue in the luxury and business hotel sector are declining due to ineffective management decisions. To counter this, the revenue management team is harnessing Business and Data intelligence to identify and bridge the gaps that are affecting their business.

Their immediate goal is to find a skilled Data Analyst who can provide them with valuable insights to address these challenges.

## Tasks
1. Develop essential metrics based on a predefined list.
2. Construct a dashboard according to the specifications provided by stakeholders.
3. Generate insightful findings that go beyond what is outlined in the predefined metric list and mock-up dashboard.


### AtliQ Grands
- AtliQ Grands, a prestigious five-star hotel chain, operates in four major cities.
- Their portfolio comprises seven distinct properties spread across these four cities.
- Their properties offer rooms categorized as Elite, Premium, Presidential, and Standard.
- Booking options encompass six main platforms along with some less effective alternatives.

## Dataset Provided By Codebasics

- **dim_date** – This table contains date-related information, including dates, week numbers, and day types (weekend and weekday).

- **dim_hotels** – This table provides data on property identifiers, property names, categories, and city locations.

- **dim_rooms** – This table details room identifiers and room classifications.

- **fact_aggregated_bookings** – his fact table features property IDs, check-in dates, room categories, successful bookings, and capacity information.

- **metrics list** – This dataset contains a collection of key performance measures, complete with the DAX formulas used to compute them.

- **fact_bookings** – Tnother fact table, it includes supplementary data such as financial details. This data encompasses booking IDs, property IDs, booking dates, check-out dates, check-in dates, guest counts, room categories, booking platforms, ratings, booking statuses, revenue generated, and revenue realized.

The stakeholders have provided a list of visual metrics to be examined:

+ **Trends By Weeks** –
   - Revenue
   - Occupancy %
   - Avg Rating
+ **Split By City** –
   - Revenue
   - Occupancy %
   - Avg Rating
+ **Occupancy By Day Type**
+ **Booking% by Platform**
+ **Filters** –
   - Properties
   - City
   - Status
   - Platform
   - Month
   - Week
+ **Table** –
    - Hotels property id
    - City
    - Revenue
    - Occupancy %
    - Avg rating %
    - Cancellation rate %
+ **Percentage Change vs. the Previous Month**

## Mockup Dashboard
The project's mockup dashboard presents a preview of the AtliQ hospitality data analytics initiative.

## Dashboard Created
Dashboard Link

We have successfully created a comprehensive dashboard using the information and data provided by stakeholders. This dashboard showcases crucial metrics to aid AtliQ Grands' management in improving revenue generation.e.

## Data Model Structure

The data model utilizes a star schema with fact tables at its core, surrounded by dimension tables.

### Data Cleaned
We performed data cleaning and derived relevant information using DAX formulas, such as calculating the week number from the date column and determining the day type. We also calculated the revenue from the available data, including "revenue_generated" and "revenue_realized."

**Derived week number from date column using DAX formula** =
wn = WEEKNUM(dim_date[date])
**Derived day type from date column using DAX formula** =
day_type =
var wkd = WEEKDAY(dim_date[date],1)
return
IF(
    wkd>5,”Weekend”,”Weekday”)
Also, the revenue was not directly provided and it was required to be calculated in the dim_bookings from the column revenue_realized.

The revenue columns provided in the data set are:

**revenue_generated**is the column that contains the amount of money generated by hotels from a customer. (Like cancellation money, no show etc)

**revenue_realized**: This column represents the final amount of money that goes to the hotel based on booking status. If the booking status is cancelled, then 40% of the revenue generated is deducted and the remaining is refunded to the customer. If the booking status is Checked Out/No Show, then the full revenue generated will go to hotels.

**Key Measure Revenue generated using this DAX formula:**
Revenue = SUM(fact_bookings[revenue_realized])

Rest all the data was clean and not many changes were required to do.

### Report Pages
The report offers various pages and views for in-depth analysis:

**Report View**
This consolidated view features financial statistics and hotel performance metrics.

**Financial Stats**
This section includes metrics specific to the hospitality industry, such as revenue, cancellations, and room-level pricing.

Here is a list of these financial metrics used in the hospitality industry.

**Revenue** as we know is the most common metric used in every industry.

**RevPAR** – Revenue generated per available room.

**ADR** – Average Daily Rate is the average daily price per room.

These are the main financial statistics that we need to look at micro to macro level.


**Performance**
The stats related to performance includes the hotel’s occupancy, cancellation %, room availability etc. All these factors directly contribute to the revenue. And some of these factors are controllable by the management whereas some factors are uncontrollable.

Here is the list of metrics:

**DSRN** – Daily Sellable Room Nights is the metric used for available rooms that can be sold. Example: If there are 100 rooms in a hotel and 20 rooms are not available for any XYZ reason, the DSRN here is 80.

**DBRN** – Daily Booked Room Nights are the number of nights booked per night.

**DURN** – Daily Utilized Room Nights are the nights utilized or used by the customers. This can be the checked-in nights.

**Cancellation %** – As the name suggests, it is the percentage of cancelled bookings.

**Avg Rating** – Average rating is the average rating given by a customer per booking.

**Day Type** – Day is the category of days in a week. Weekday and Weekend. In the hospitality sector, the weekend is Friday and Saturday. Most of the customers checkout on Sunday.

**Booking Platforms** – Booking platforms are the modes that are used by customers to book rooms. These include AtliQ’s own booking platform and third-party platforms as well.

**Week Number**– Week number is the number of weeks in a year.

**Property Name** – Property name is the name of individual hotels.

**Property ID** – Property ID is the unique ID given to the properties.

**WoW** – Week on Week is the metric to compare the performance change over the week.


## Filters Used

**Week Number** – To review each week’s performance.

**Month** – To assess monthly performance.

**Property** – This filter provides insights into each property, facilitating decision-making.

**City** – It helps in evaluating the market value of AtliQ.

**Room Class** – This filter allows a detailed examination of room categories, aiding in improving room standards and availability.

**Booking Platforms** – By selecting booking platforms, the marketing team can target their efforts more effectively.


## Finance View
The finance view provides financial analysis by applying various filters, excluding performance metrics. It focuses on micro and macro-level financial performance, including realization, RevPAR, ADR, and more.

This report is for financial analysis of the business.

**Realization** – Utilized Room Nights / Booked Room Nights

**RevPAR** – Revenue Per Available Room

**ADR** – Average Daily Rate

**DBRN** – Daily Booked Room Nights

**DSRN** -  Daily Sellable Room Nights

**DURN** -  Daily Utilized Room Nights

**Revenue WoW change %** - Revenue Week Over Week Change


## Learnt things from this Project
- We acquired the skill to create a new visual, such as a calendar visual, using a matrix table for diverse analytical purposes.
- By examining different cancellation policies employed by various hotels, we learned that most hotels charge zero fees for cancellations made three months before the booking date.
- For cancellations after this period, charges typically range from 60% to 90% of the booking cost.

## Some Important insights from the Dashboard
- Mumbai leads in revenue generation, amassing a substantial 669 million, with Bangalore, Hyderabad, and Delhi following suit.
- Among the seven types of properties, AtliQ Exotica stands out with remarkable performance, raking in 320 million in revenue, boasting a solid rating of 3.62, achieving an impressive occupancy rate of 57%, and experiencing a cancellation rate of 24.4%.
- AtliQ Bay takes the crown for the highest occupancy rate, reaching an impressive 66%.
- Week 24 emerges as the most profitable week of all, with revenue soaring to 139.6 million.
- In terms of both occupancy and rating, Delhi takes the lead, closely trailed by Hyderabad, Mumbai, and Bangalore.
- Unfortunately, AtliQ incurred significant losses, totaling around 298 million, due to cancellations.
- Elite type rooms witness the highest booking rates, but they also experience a comparatively elevated rate of cancellations.
