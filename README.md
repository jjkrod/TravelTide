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
Unknown Tide: 0 booking
Freebie Tide Collector: > 80% booking with discount applied
Shoreline: Family (has children, age < 58)
Deep Tide Planners: Early Birds (duration between flight or hotel and booking date > 90 days)
Riptide Rush: Last-Minute (duration between flight or hotel and booking date < 90 days)
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
Quiz: “Where would be your next adventure?” in 4 questions
* Season = summer/winter
* Activity = chill/energetic
* Group = alone/couple/friends/family
* Budget = ranges of budget
Your next destination is: _____ with 15% off on the flight+hotel booking.
On top of giving some traction with that reward through that quizz, the data we collect will be kept for future advertising and tailored offering.
## Additional Data Collection
### 
user.user_id (integer) -- 48629
user.first_name (varchar) -- Jean
user.last_name (varchar) -- Louis
user.email_address (varchar) -- jean.louis@gmail.com
user.phone_number (varchar) -- +49 123 345 3224
user.street_address (varchar) -- Vogelstrasse 6
user.city_address (varchar) -- Dorfstadt
user.country_address (varchar) -- Germany
user.postal_code_address (varchar) -- 12345
user.birthdate (date) -- 1992-08-23 
user.nationality (varchar) -- french
user.preferred_language (varchar) -- english
user.locale (varchar) -- de
user.family_status (varchar) -- married
user.has_children (boolean) -- true
user.signup_date (date) -- 2024-01-25
user.last_interaction_type (varchar) -- email
user.last_interaction_timeframe (date) -- 2024-06-07

marketing.user_segment (varchar)
marketing.acquisition_source (varchar) -- advertisement
marketing.communication_email (boolean) -- true
marketing.communication_sms (boolean) -- false
marketing.communication_in-app (boolean) -- true
marketing.communication_whatsapp (boolean) -- false
marketing.newsletter_list (boolean) -- false
marketing.promotional_list (boolean) -- true
marketing.first_session_date (date) -- 2024-01-20
marketing.number_of_session (integer) -- 43
marketing.avg_duration_session (time) -- 4:04
marketing.first_email_opened ((varchar) -- 'Welcome to TravelTide'
marketing.first_email_opened_date (date) -- 2024-01-25
marketing.email_open_rate (decimal) -- 0.45
marketing.travel_style (varchar) -- adventure
marketing.travel_preferred_season (varchar) -- summer
marketing.travel_budget_class (varchar, 3) -- mid
marketing.travel_situation (varchar) -- business
marketing.travel_preferred_destination (varchar) -- Southern Asia
marketing.travel_yearly_frequency (decimal) -- 5
marketing.travel_frequency_range (varchar) -- occasional traveler
marketing.travel_duration (varchar) -- 21-30 days
marketing.travel_flight_category (varchar) -- eco
marketing.travel_preferred_hotel_category (varchar) -- appartment
marketing.travel_preferred_vacation_package (varchar) -- all-inclusive
marketing.travel_search_terms_saved (varchar) -- (malaysia, thailand, phuket, singapore)

trip.first_booking_date (date) -- 2024-05-02
trip.first_booking_hotel_date (date) -- 2024-05-02
trip.first_booking_flight_date (date) -- 2024-05-02
trip.total_number_of_trips (integer) -- 7
trip.total_amount_spent (decimal) -- 5045.99
trip.total_amount_spent_hotel (decimal) -- 3045.49
trip.total_amount_spent_flight (decimal) -- 2000.50
trip.total_avg_amount_spent (decimal) -- 720.85
trip.travel_insurance_booked (boolean) -- false
trip.number_travel_insurance_booked (integer) -- 0
trip.total_amount_spent_travel_insurance (decimal) -- 0.00
