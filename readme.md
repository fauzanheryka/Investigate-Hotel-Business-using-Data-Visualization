## Investigate Hotel Business using Data Visualization
- - - 
**Tool** : Jupyter Notebook <br>
**Programming Language** : Python <br>
**Libraries** : Pandas, NumPy, Seaborn, Matplotlib <br>
**Dataset** : Hotel booking from Rakamin Academy <br>

**Table of Contents**
- [STAGE 0: Problem Statement](#stage-0-problem-statement)
    - [Data overview](#data)
    - [Background](#background)
    - [Objective](#objective)
- [STAGE 1: Data Preprocessing](#stage-1-data-prepocessing)
    - [Handling Data](#stage-1-data-prepocessing)
- [STAGE 2: Data Analysis](#2-data-analysis)
    - [Monthly Hotel Booking Analysis Based on Hotel Type](#1-monthly-hotel-booking-analysis-based-on-hotel-type)
    - [Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rates](#2-impact-analysis-of-stay-duration-on-hotel-bookings-cancellation-rates)
    - [Impact Analysis of Lead Time on Hotel Bookings Cancellation Rates](#3-impact-analysis-of-lead-time-on-hotel-bookings-cancellation-rates)
- [STAGE 3: Business Recommendation](#stage-3-business-recomendation)

## Stage 0 Problem Statement

## Data
The data used in this project consists of 29 columns and 119390 rows. Data can be accessed, This project's creation makes the assumption that the data is either from an order placed in 119390 or that there are no duplicates.  The following is a description of each column in the data set.
| Column        | Description |
|:-------------|:-----|   
|hotel|  The datasets contains the booking information of two hotel. One of the hotels is a resort hotel and the other is a city hotel|
|is_canceled|  Value indicating if the booking was canceled (1) or not (0)
|lead_time|  Number of days that elapsed between the entering date of the booking into the PMS and the arrival date
|arrival_date_year|  Year of arrival date
|arrival_date_month|  Month of arrival date with 12 categories: “January” to “December”
|arrival_date_week_number|  Week number of the arrival date
|arrival_date_day_of_month|  Day of the month of the arrival date
|stays_in_weekend_nights|  Number of weekend nights (Saturday or Sunday) the guest stayed or booked to stay at the hotel
|stays_in_weekdays_nights|  Number of week nights (Monday to Friday) the guest stayed or booked to stay at the hotel BO and BL/Calculated by counting the number of week nights
|adults|  Number of adults
|children|  Number of children
|babies|  Number of babies
|meal|  Meal menu
|city|  City of origin
|market_segment|  Market segment designation. In categories, the term “TA” means “Travel Agents” and “TO” means “Tour Operators”
|distribution_channel|  Booking distribution channel. The term “TA” means “Travel Agents” and “TO” means “Tour Operators”
|is_repeated_guest|  Value indicating if the booking name was from a repeated guest (1) or not (0)
|previous_cancellations|  Number of previous bookings that were cancelled by the customer prior to the current booking
|previous_bookings_not_canceled|  Number of previous bookings not cancelled by the customer prior to the current booking
|booking_changes|  Number of changes/amendments made to the booking from the moment the booking was entered on the PMS until the moment of check-in or cancellation
|deposit_type|  No Deposit – no deposit was made; Non Refund – a deposit was made in the value of the total stay cost; Refundable – a deposit was made with a value under the total cost of stay
|agent|ID of the travel agency that made the booking
|company|ID of the company/entity that made the booking or responsible for paying the booking. ID is presented instead of designation for anonymity reasons
|days_in_waiting_list| Number of days the booking was in the waiting list before it was confirmed to the customer
|customer_type| Group – when the booking is associated to a group; Transient – when the booking is not part of a group or contract, and is not associated to other transient booking; Transient-party – when the booking is transient, but is associated to at least other transient booking
|adr| Average Daily Rate (Calculated by dividing the sum of all lodging transactions by the total number of staying nights)
|required_car_parking_spaces| Number of car parking spaces required by the customer
|total_of_special_requests| Number of special requests made by the customer (e.g. twin bed or high floor)
|reservation_status| Check-Out – customer has checked in but already departed; No-Show – customer did not check-in and did inform the hotel of the reason why  
<br>

## Background
It is critical for a company to constantly assess its business performance. The company can take appropriate action to deal with a problem by analyzing business performance.

On this occasion, we will examine the hotel industry's performance. The primary goal of this project is to identify the customer actors involved in hotel bookings and their relationship to hotel cancellation rates. So three things will be analyzed in this project:

## Objective
1. Monthly Hotel Booking Analysis Based on Hotel Type
2. Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rates
3. Impact Analysis of Lead Time on Hotel Bookings Cancellation Rate

Based on the results of the insights obtained, visualization will be carried out so that they can be easily understood.

## Stage 1 Data Prepocessing
- Handling missing values
- handling Duplicated Data
- Incorrect values from numerical and categorical data

**For the detail kindly to check notebook :)**


## 2. Data Analysis

### 1. Monthly Hotel Booking Analysis Based on Hotel Type
<p align="center">
    <kbd><img width="600" alt="Rasio Tipe Hotel" src="https://github.com/fauzanheryka/Project-Portofolio/assets/141212116/773e8670-955e-422d-934f-c8598012b4ec"></kbd><br>
    Figure 1 - Percentage Ratio of City Hotels and Resort Hotels
</p>

### Insight : 
- Tourists prefer staying at city hotels over resort hotels. The pie chart above illustrates this, showing that compared to resort hotels, city hotels have about 66% more customers overall.
- City hotels are more popular because they offer a number of benefits. For example, being in the heart of the city makes them the most visible to foreign visitors, and since some of their patrons are there on business rather than for pleasure, they appear cozier and more convenient. for foreigners arriving outside of the city.
- The benefit of resort hotels, which are typically found on the outskirts of towns, is that they provide the typical tourist with a vacation spot where they can enjoy views of the mountains, sea, and forest.

Source [Article](https://www.littlehotelier.com/blog/running-your-property/difference-between-hotel-resort/)
<br>

<p align="center">
    <kbd> <img width="1500" alt="hotel type" src="https://github.com/fauzanheryka/Project-Portofolio/assets/141212116/c702fc40-33ca-4bbf-8a8c-39b48475cf51"
">
 </kbd> <br>
    Figure 2 — City Hotel and Resort Hotel Booking Numbers by Month
</p>

### Insight : 
- Due to the fact that most visitors travel with their children during school breaks, which occur during the months of February through March and August through September, there is a decrease in both types of hotels during these school-related periods. Overall, though, hotel reservations peaked in February and March, when they were **lowest**. This could have been because Indonesia kids are starting a new school year. [Source Article](https://nasional.kontan.co.id/news/musim-libur-berakhir-tingkat-hunian-kamar-hotel-turun-1204-pada-januari-2023)
- A marketing plan is required to boost hotel reservations in order to overcome Providing restaurant and ballroom services in partnership with EO/WO is one of the few suggested approaches. For loyal customers who frequently visit throughout the holidays, provide loyalty programs. For example, send emails informing them of exclusive deals and award points to attract their curiosity. [Link article](https://www.ezeeabsolute.com/blog/increase-low-season-hotel-occupancy/)
- A few strategies that might be suggested to boost hotel reservations during the second holiday season. Hotels could plan a number of entertaining activities for the Christmas and New Year holidays, such as crafting unique Christmas gifts like letters with good wishes. Customers may get the impression that the hotel values them in this way, which could have a long-term good impact such as making them loyal customers and possibly turning into a free advertisement for the hotel. A very satisfied customer is likely to post about their activities on social media. [Link Article](https://prenohq.com/blog/11-christmas-marketing-strategies-for-hotels-to-try-in-2022/)
- **For the detail insight kindly to check notebook**
<br>

### 2. Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rates
<p align="center">
    <kbd> <img width="600" alt="cancel rate hotel type" src="https://github.com/fauzanheryka/Project-Portofolio/assets/141212116/eed73dd9-7e02-4e61-80d6-5fa230826578"></kbd> <br>
    Figure 3: Cancellation Percentage Graph for Hotel Type
</p>

### Insight :
The two hotels have differing cancellation rates: the resort hotel has a rate of 28%, while the city hotel has a rate of 42%. It's shown in the diagram that these two hotels' cancellation rates are different for the resort hotel and the city hotel. We will look at the typical duration of stay for customers that cancel in order to conduct the further analysis required to make sure this doesn't happen again.
<br>

<p align="center">
    <kbd><img width="1000" alt="hotel resort" src="https://github.com/fauzanheryka/Project-Portofolio/assets/141212116/2d6265e9-697d-4a66-99af-0e9e720e7e8e"></kbd> <br>
    Figure 4 - Trends of Hotel Reservation Cancellations by Duration of Stay
</p>

### Insight : 
- The graph illustrates that the higher the cancellation rate, the longer the period of stay when placing an order. It is known that 95% of order cancellations for stays longer than one month occur in city hotels.
- Especially compared to city hotels, resort hotels generally have lower cancellation rates.
- If you look closely, you will see that the guest cancellation rate is rising after more than two weeks.
- If a guest rents a room with a stay duration of more than a week, it is preferable for them to make a hotel reservation for successive bookings before 7 days to avoid the high cancellation charge. The lowest cancellation rate is only available for bookings of less than a week.
- **For the detail insight kindly to check notebook**

### 3. Impact Analysis of Lead Time on Hotel Bookings Cancellation Rates
<p align="center">
    <kbd><img width="1500" alt="tren lead" src="https://github.com/fauzanheryka/Project-Portofolio/assets/141212116/4cce729f-d1d6-427a-ae5a-44e1d1c72c23"></kbd> <br>
    Figure 5 — Hotel Booking Cancellation Trends Based on Lead Time
</p>

### Insight : 
- The graph illustrates that, within a month of arrival, these two categories of hotels have the lowest cancellation rates.
- Waiting for customers who have more than a 10-month arrival date isn't recommended since the above graph illustrates that the city hotel cancellation rate may go over 73%.
- When it comes to cancellation rates, resort hotels have the most consistent rate, at about 40% per month.
- The maximum waiting period for reservations should be set at one month by hotel management as a measure against consumers who could forget whether they have ever booked a hotel with an extremely long waiting period. Setting a maximum waiting period limit for guests is highly suggested, as it can be observed that a one-month waiting period has the lowest cancellation rate.
<br>

## Stage 3 Business Recomendation

The following businesses can be recommended based on the visualization and insights obtained:
1. To lower the rate of cancellations, hotels may set a policy on visitors who cancel their reservations through the penalty system.
2. To lower cancellation rates, hotels can set up a maximum time period or booking interval of no more than one month.
3. Provide a system of message reminders for orders that need a lengthy ordering process.
4. Hotel management can hold events at specific times during the year, such as in June and November/December.
5. In order to increase revenue during school days, hotel staff can collaborate with EO/WO to host events and provide a ballroom and restaurant for enthusiastic guests who frequently visit the hotel.