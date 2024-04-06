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

 ## Call Centre Trends Analysis Report

### Insights

#### Key Metrics:
- Average Satisfaction Rating: 3.4
- Average Speed of Answer (seconds): 67.52

#### Agent Performance:
| Agent   | Count of Answered (Y/N) | Resolved Calls | Average Satisfaction Rating | Average Speed of Answer (seconds) |
|---------|-------------------------|----------------|-----------------------------|-----------------------------------|
| Becky   | 631                     | 462            | 3.37                        | 65.33                             |
| Stewart | 582                     | 424            | 3.40                        | 66.18                             |
| Diane   | 633                     | 452            | 3.41                        | 66.27                             |
| Jim     | 666                     | 485            | 3.39                        | 66.34                             |
| Dan     | 633                     | 471            | 3.45                        | 67.28                             |
| Greg    | 624                     | 455            | 3.40                        | 68.44                             |
| Martha  | 638                     | 461            | 3.47                        | 69.49                             |
| Joe     | 593                     | 436            | 3.33                        | 70.99                             |
| Total   | 5000                    | 3646           | 3.40                        | 67.52                             |

#### Maximum Call Time:
- Maximum calls are observed at 1:00 p.m.

#### Proportion of Resolved and Not Resolved Calls:
- Proportion of Resolved Calls: 72.92%
- Proportion of Not Resolved Calls: 27.08%

#### Overall Call Handling:
- Overall Abandoned Calls Proportion: 18.92%
- Overall Answered Calls Proportion: 81.08%

- Total Answered Calls Count: 4054
- Total Abandoned Calls Count: 946

### Suggestions to PWC

Based on the analysis, here are some suggestions to improve call center performance:

1. **Agent Training:** Provide additional training to agents with lower satisfaction ratings to improve customer interactions and satisfaction levels.

2. **Call Handling Efficiency:** Implement strategies to reduce the average speed of answer, such as optimizing staffing levels during peak call times or improving call routing algorithms.

3. **Resolution Rate Improvement:** Focus on enhancing the resolution rate to reduce the proportion of unresolved calls, ultimately improving overall customer satisfaction.

4. **Abandoned Call Management:** Develop strategies to minimize abandoned calls, potentially by offering alternative contact methods or improving call queue management.

5. **Performance Recognition:** Recognize and reward agents with consistently high performance to motivate and retain top talent within the call center.

By addressing these areas, PWC can enhance customer experience, increase operational efficiency, and drive overall business success.



