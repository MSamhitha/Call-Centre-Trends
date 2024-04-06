# Call-Centre-Trends
Interactive PWC call center dashboard to tracks key metrics to enhance customer experience and operational efficiency.

## Call Centre Dashboard

### Problem Statement

Experiencing challenges in effectively managing customer inquiries and maintaining high satisfaction levels, PwC's call center confronts issues of increasing call abandonment rates, longer wait times, and inconsistent handling of queries.

These obstacles lead to declining satisfaction and hinder meeting service level agreements. Deeper insights into call center operations are necessary, focusing on key performance indicators such as overall satisfaction, calls handled, average response times, first-call resolution rates, and agent performance. Utilizing Power BI, the objective is to develop a comprehensive dashboard enabling stakeholders to monitor metrics, identify gaps, and make data-driven decisions.

The aim is to optimize service delivery, reduce wait times, enhance first-call resolution, and elevate customer service quality, ultimately improving overall customer experience and satisfaction while driving operational excellence.

### Steps Followed

#### Step 1: Data Collection and Preparation

- Utilized data from the call center's database, including columns such as Call Id, Agent, Date, Time, Topic, Answered (Y/N), Resolved, Speed of answer in seconds, AvgTalkDuration, and Satisfaction rating. The dataset contained 5k observations.

#### Step 2: Data Modeling (Defining Measures)

- Implemented DAX expressions to create new measures:
  - Abandoned calls: `COUNTROWS(FILTER('Sheet1', 'Sheet1'[Answered (Y/N)] = "N"))`
  - Answered calls: `COUNTROWS(FILTER('Sheet1', 'Sheet1'[Answered (Y/N)] = "Y"))`
  - Resolved calls: `COUNTROWS(FILTER('Sheet1', 'Sheet1'[Resolved] = "Y"))`
  - Calculated hour from Time column to identify peak call hours.

#### Step 3: Dashboard Development (Visualizations)

- Implemented the following visualizations to display key metrics:
  - Average Satisfaction Rating
  - Average Speed of Answer in Seconds
  - Agent Performance (Individual and Overall)
  - Proportion of Resolved and Not Resolved Calls
  - Overall Answered Calls
  - Overall Abandoned Calls
####  Snapshot of Call Center Trends Dashboard
  - ![Snapshot of Power BI Dashboard - Call Center Trends](https://github.com/MSamhitha/Call-Centre-Trends/assets/122619470/70f1871b-e72e-473b-8a81-65a432c160ef)

 

