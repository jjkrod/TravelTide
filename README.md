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
### Table of groups (Perks)
| Group Name | Perks |
| --- | --- |
| Unknown Tide | 15% off the first order |
| Freebie Tide Collector | Exclusive offers | 
| Shoreline (Family) | Free breakfast, Access to Kids Club, Free Checked Bags | 
| Deep Tide Planners | Promotional Offer on full packages | 
| Riptide Rush | Free Cancellation, Free Lounge Access, Free Upgrade | 
### Table of groups (Perks)
| Group Name | Score | Reward |
| --- | --- | --- |
| Low Tide | 3-7 | 10% off on selected fights and hotels |
| High Tide | 8-12 | 15% off on selected flights and hotels <br> Customer support within 1 working day |
| King Tide | 13-15 | 20% off on selected flights and hotels <br> Customer support within 2 hours |
