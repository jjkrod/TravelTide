# TravelTide
Masterschool Project: Segmenting Customers To Assign Perks and Rewards.
## Introduction
TravelTide is a hot new player in the online travel industry. It has experienced steady growth since it was founded at the tail end of the COVID-19 pandemic (2021-04) on the strength of its data aggregation and search technology, which is best in class. Feedback from the customers has shown - and industry analysts agree - that TravelTide customers have access to the largest travel inventory in the e-booking space!
## Objective
Elena’s mission (Marketing) is to design and execute a personalized rewards program that keeps customers returning to the TravelTide platform. This project aims to analyze the current data we have from TravelTide customers (in particular the behavior, travel style and other preferences) in order to define the proper rewards for each groups.
## Work Breakdown Structure 
* Exploratory Data Analysis (EDA)
* Creating Customer Metrics
* Cohort Definition
* Marketing Competitive Analysis
* Decision-Tree
* Customer Segmentation
* Out of Scope Ideas for Marketing
* Additional Data Collection
* Presentation
## Suggested Cohort
User who signed up after 2023-01-04 and with more than 7 sessions. 
## Tools
* **SQL** (on Beekeeper and Google Colab) : EDA, Cleaning Data
* **Python** (on Google Colab) : EDA, Data Structure, Data Quality Check, Data Anomalies + Histograms
* **Lucidcharts** :  Decision Tree, Initial Customer Groups
* **Tableau** :  Visualizations, Confirm Customer Groups, Check Outliers
* **Canva** : Presentation of the project
* **Jupyter Notebook** (this very document)
## Segmentation by bahavior and demographic
### Behavior segmentation
Use of the RFM Analysis (Recency, Frequency, Monetary) to score the loyalty. Based on data from purchase history, we score as follow:
* Recency = last 30 days (5) ; 31-60 days (4) ; 61-90 days (3) ; 91-120 days (2) ; more than 120 days (1)
* Frequency = > 9 bookings (5) ; 5-9 bookings (4) ; 4-5 bookings (3) ; 2-3 bookings (2) ; 1 booking (1)
* $ Value = > 3,000$ (5) ; 1,500-3,000$ (4) ; 1,000-1,500$ (3) ; 500-1,000$ (2) ; < 500$ (1)
+ Group with no booking at all
+ Group with high sensibility to discount
+ Group based with time: early birds and last-minute planners
### Demographic segmentation
* Group categorized as family
### Examples of groups and metrics
*Unknown Tide*: 0 booking
<br>*Freebie Tide Collector*: > 80% booking with discount applied
<br>*Shoreline*: Family (has children, age < 58)
<br>*Deep Tide Planners*: Early Birds (duration between flight or hotel and booking date > 90 days)
<br>*Riptide Rush*: Last-Minute (duration between flight or hotel and booking date < 90 days)
### Table of groups (+ Perks)
| Group Name | Perks |
| --- | --- |
| Unknown Tide | 15% off the first order |
| Freebie Tide Collector | Exclusive offers | 
| Shoreline (Family) | Free breakfast, Access to Kids Club, Free Checked Bags | 
| Deep Tide Planners | Promotional Offer on full packages | 
| Riptide Rush | Free Cancellation, Free Lounge Access, Free Upgrade | 
### Reward Table
| Group Name | Score | Reward |
| --- | --- | --- |
| Low Tide | 3-7 | 10% off on selected fights and hotels |
| High Tide | 8-12 | 15% off on selected flights and hotels <br> Customer support within 1 working day |
| King Tide | 13-15 | 20% off on selected flights and hotels <br> Customer support within 2 hours |
## Marketing Project - Out of Scope
For any user who lands on the website, we would attract them with a small quiz.
<br>Quiz: “Where would be your next adventure?” in 4 questions
* Season = summer/winter
* Activity = chill/energetic
* Group = alone/couple/friends/family
* Budget = ranges of budget
<br>Your next destination is: _____ with 15% off on the flight+hotel booking.
<br>On top of giving some traction with that reward through that quizz, the data we collect will be kept for future advertising and tailored offering.
## Additional Data Collection
`user.user_id (integer) -- 48629`
<br>`user.first_name (varchar) -- Jean`
<br>`user.last_name (varchar) -- Louis`
<br>`user.email_address (varchar) -- jean.louis@gmail.com`
<br>`user.phone_number (varchar) -- +49 123 345 3224`
<br>`user.street_address (varchar) -- Vogelstrasse 36`
<br>`user.city_address (varchar) -- Dorfstadt`
<br>`user.country_address (varchar) -- Germany`
<br>`user.postal_code_address (varchar) -- 12345`
<br>`user.birthdate (date) -- 1990-05-23`
<br>`user.nationality (varchar) -- french`
<br>`user.preferred_language (varchar) -- english`
<br>`user.locale (varchar) -- de`
<br>`user.family_status (varchar) -- married`
<br>`user.has_children (boolean) -- true`
<br>`user.signup_date (date) -- 2024-01-25`
<br>`user.last_interaction_type (varchar) -- email`
<br>`user.last_interaction_timeframe (date) -- 2024-06-07`
<br>`marketing.user_segment (varchar)`
<br>`marketing.acquisition_source (varchar) -- advertisement`
<br>`marketing.communication_email (boolean) -- true`
<br>`marketing.communication_sms (boolean) -- false`
<br>`marketing.communication_in-app (boolean) -- true`
<br>`marketing.communication_whatsapp (boolean) -- false`
<br>`marketing.newsletter_list (boolean) -- false`
<br>`marketing.promotional_list (boolean) -- true`
<br>`marketing.first_session_date (date) -- 2024-01-20`
<br>`marketing.number_of_session (integer) -- 43`
<br>`marketing.avg_duration_session (time) -- 4:04`
<br>`marketing.first_email_opened ((varchar) -- 'Welcome to TravelTide'`
<br>`marketing.first_email_opened_date (date) -- 2024-01-25`
<br>`marketing.email_open_rate (decimal) -- 0.45`
<br>`marketing.travel_style (varchar) -- adventure`
<br>`marketing.travel_preferred_season (varchar) -- summer`
<br>`marketing.travel_budget_class (varchar, 3) -- mid`
<br>`marketing.travel_situation (varchar) -- business`
<br>`marketing.travel_preferred_destination (varchar) -- Southern Asia`
<br>`marketing.travel_yearly_frequency (decimal) -- 5`
<br>`marketing.travel_frequency_range (varchar) -- occasional traveler`
<br>`marketing.travel_duration (varchar) -- 21-30 days`
<br>`marketing.travel_flight_category (varchar) -- eco`
<br>`marketing.travel_preferred_hotel_category (varchar) -- appartment`
<br>`marketing.travel_preferred_vacation_package (varchar) -- all-inclusive`
<br>`marketing.travel_search_terms_saved (varchar) -- (malaysia, thailand, phuket, singapore)`
<br>`trip.first_booking_date (date) -- 2024-05-02`
<br>`trip.first_booking_hotel_date (date) -- 2024-05-02`
<br>`trip.first_booking_flight_date (date) -- 2024-05-02`
<br>`trip.total_number_of_trips (integer) -- 7`
<br>`trip.total_amount_spent (decimal) -- 5045.99`
<br>`trip.total_amount_spent_hotel (decimal) -- 3045.49`
<br>`trip.total_amount_spent_flight (decimal) -- 2000.50`
<br>`trip.total_avg_amount_spent (decimal) -- 720.85`
<br>`trip.travel_insurance_booked (boolean) -- false`
<br>`trip.number_travel_insurance_booked (integer) -- 0`
<br>`trip.total_amount_spent_travel_insurance (decimal) -- 0.00`
