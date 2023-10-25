# Provide Insights to the Revenue Team in the Hospitality Domain
## Live Interactive Dashboard : [Link to Dashboard](https://app.powerbi.com/view?r=eyJrIjoiZjFhMmY2MmEtNzVjOC00NDM4LTg2YTQtMDVjZjJhYzI2OWIzIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)
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


**Performance**
The stats related to performance includes the hotel’s occupancy, cancellation %, room availability etc. All these factors directly contribute to the revenue. And some of these factors are controllable by the management whereas some factors are uncontrollable.

Here is the list of basics:

**Day Type** – Day is the category of days in a week. Weekday and Weekend. In the hospitality sector, the weekend is Friday and Saturday. Most of the customers checkout on Sunday.

**Booking Platforms** – Booking platforms are the modes that are used by customers to book rooms. These include AtliQ’s own booking platform and third-party platforms as well.

**Week Number**– Week number is the number of weeks in a year.

**Property Name** – Property name is the name of individual hotels.

**Property ID** – Property ID is the unique ID given to the properties.

**WoW** – Week on Week is the metric to compare the performance change over the week.

Here is the list of measures:

| Measures | Description |
| ------ | ---------- |
| Revenue | It is the most common metric used in every industry to get the total revenue_realized | 
| Total Bookings  | To get the total number of bookings happened | 
| Total Capacity | To get the total capacity of rooms present in hotels | 
| Total Succesful Bookings  | To get the total succesful bookings happened for all hotels | 
| Occupancy %  | Occupancy means total successful bookings happened to the total rooms available(capacity) | 
| Average Rating  |  Get the average ratings given by the customers |
| No of days  | To get the total number of days present in the data.In our case, we have data from May to July. So 92 days.|
| Total cancelled bookings | To get the"Cancelled" bookings out of all Total bookings happened  |
| Cancellation % |  calculating the cancellaton percentage. |
| Total Checked Out |  To get the successful 'Checked out' bookings out of all Total bookings happened |
| Total no show bookings  | "No show" means those customers who neither cancelled nor attend to their booked rooms |
| No Show rate %  | calculating the no show percentage.  |
| Booking % by Platform  |  To show the percentage contribution of each booking platform for bookings in hotels. |
| Booking % by Room class  |  To show the percentage contribution of each room class over total rooms booked. |
| ADR  |  Calculate the ADR(Average Daily rate). It is the ratio of revenue to the total rooms booked/sold. It is the measure of the average paid for rooms sold in a given time period |
|  Realisation % |  calculate  the realisation percentage.It is nothing but the succesful "checked out" percentage over all bookings happened.|
| RevPAR  |  Calculate the RevPAR(Revenue Per Available Room) RevPAR represents the revenue generated per available room, whether or not they are occupied. RevPAR helps hotels measure their revenue generating performance to accurately price rooms. RevPAR can help hotels measure themselves against other properties or brands. |
| DBRN  |  calculate DBRN(Daily Booked Room Nights). This metrics tells on average how many rooms are booked for a day considering a time period |
| DSRN   |  calculate DSRN(Daily Sellable Room Nights). This metrics tells on average how many rooms are ready to sell for a day considering a time period. |
| DURN | calculate DURN(Daily Utilized Room Nights). This metric tells on average how many rooms are succesfully utilized by customers for a day considering a time period |
| Revenue WoW change % | To get the revenue change percentage week over week. Here, revcw  for current week, revpw for previous week |
|  Occupancy WoW change % | To get the occupancy change percentage week over week.Here, revcw  for current week ,revpw for previous week  |
| ADR WoW change %  | To get the ADR(Average Daily rate) change percentage week over week.Here, revcw  for current week, revpw for previous week  |
| Revpar WoW change % |  To get the RevPar(Revenue Per Available Room) change percentage week over week. Here, revcw  for current week, revpw for previous week |
| Realisation WoW change %  |  To get the Realisation change percentage week over week. Here, revcw  for current week, revpw for previous week |
| DSRN WoW change % | To get the DSRN(Daily Sellable Room Nights) change percentage week over week.Here, revcw  for current week, revpw for previous week  |

## Filters Used

**Week Number** – To review each week’s performance.

**Month** – To assess monthly performance.

**Property** – This filter provides insights into each property, facilitating decision-making.

**City** – It helps in evaluating the market value of AtliQ.

**Room Class** – This filter allows a detailed examination of room categories, aiding in improving room standards and availability.

**Booking Platforms** – By selecting booking platforms, the marketing team can target their efforts more effectively.

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
