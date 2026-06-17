# Background

The Director of Customer Success at monday.com approaches you with the
following challenge:
_"We onboard thousands of new customers every day, but only have a limited
number of consultants. We need a smart way to decide which accounts should
receive our VIP consulting services."_

# Problem Description

You’re tasked with designing and implementing a binary classification model
( is_suitable ) to help the CS team prioritize which accounts should receive VIP
consulting. The decision should be made within the first two weeks from registration.

# Available Data

Here is a description of the data available and a link to its folder:

### Users:

```
● account_id: Unique identification of the account
● user_id: Unique identification of the user
● email: Email of the user
● name: Full name of the user
● created_at: User registration date
● is_admin: Indication if the user is an admin in the account (admin
privileges)
● pending: Pending invitation (whether the user accepted the
invitation)
● enabled: Enabled to use the platform
● became_active_at: When the user became active
● time_diff: Time diff in relation to UTC
```

```
● city: IP-based city
● region: IP-based region
● country: IP-based country
● serial_number: User registration order in the account (the first user
in the account will be 1, second 2 etc.)
● has_photo: Whether the user uploaded a photo to his profile
● device: User registration device
● os: User registration os
● browser: User registration browser
● language: User system language at registration
● seniority: Seniority of the user (Executive, manager, etc.)
● has_phone: Whether the user added his phone number
```
### Accounts:

```
● account_id: Unique identification of the account
● account_name: Company name
● created_at: Account creation date
● plan_id: If the account is paying, this is the plan identifier
● trial_start: Start of the trial date
● churn_date: When did the account terminate the contract with us
● churn_reason: Cause of termination of the contract with us
● time_diff: Time diff in relation to UTC
● region: Region of the first user
● country: Country of the first user
● subscription_started_at: When did the account first start paying
● paying: Is the account currently paying
● has_logo: Whether the account uploaded a logo
● device: The device associated with the first user
● os: The OS associated with the account
● browser: The browser associated with the account
```

```
● collection_21_days: How much money the account paid in the first
21 days
● company_size: The size of the company by the “know the customer”
survey
● payment_currency: Payment currency
● max_team_size: The size of the company by the “know the
customer” survey
● min_team_size: The size of the company by the“know the
customer” survey
● industry: The kind of industry of the account
● utm_cluster_id: The type of work the account was targeted for
● mrr: Monthly recurring revenue of the account
● user_goal: A user-reported role through a survey
● user_description: A user-reported specific description through a
survey
● team_size: Truncated team size from survey
● is_suitable: Accounts that could use consulting services (yes-1,
no-0) OUR TARGET
```
### Events:

```
● date: The date by which the events were aggregated
● user_id: Unique identification of the user
● account_id: Unique identification of the account
● total_events: Number of events for the user in that day
● column_events: Aggregate of column related events
● board_events: Aggregate of board related events
● num_of_boards: Number of boards the user used that day
● count_kind_columns: Number of column types the user used that
day
● content_events: Aggregate of content modification events
● group_events: Aggregate of group related events
```

```
● invite_events: Aggregate of invites sent that day by the user
● import_events: Aggregate of import related events
● notification_events: Aggregate of events about notifications
● new_entry_events: Number of new sessions by the user that day
● payment_events: Aggregate events that contain data about the
payments
● inbox_events: Aggregate events that contain data about the user
inbox
● communicating_events: Aggregate communication events within
the account
● non_communicating_events: Aggregate events that contain
general usage in the platform
● web_events: Aggregate events that happened in the web interface
● ios_events: Aggregate events that happened in the ios app
● android_events: Aggregate events that happened in the android
app
● desktop_app_events: Aggregate events that happened in the
desktop app
● empty_events: Aggregate of general events with no specific
category
```
# Tasks

Your assignment includes both analysis and implementation. Please address the
following:

1. **Segment Analysis**
    Identify 3 meaningful business segments based on the data (e.g., company
    size, industry, region, etc.). These should be relevant and helpful for the CS
    team to better understand and act on the model’s results. Support your choice
    with data-driven insights.


2. **Modeling Approach**
    Based on your understanding of the data and problem, propose 2 modeling
    approaches (e.g., supervised classification, unsupervised clustering,
    regression-based ranking). Explain your reasoning and when each approach
    might be preferable.
3. **Performance Metrics**
    Define how you would evaluate the model's performance. Justify your choice
    of metrics based on the business goal, and explain any trade-offs you
    consider important.
4. **Implementation**
    Implement the models you proposed using Python. Include all relevant ML
    development steps: data preprocessing, feature engineering, training,
    evaluation, and model selection. Based on your defined metrics, choose the
    best-performing model and briefly summarize the results.
Please share:
● Your working notebook (code + comments)
● A short presentation (3–5 slides) highlighting your approach and key findings

## Notes:

● Document your steps clearly and explain your reasoning throughout.
● You’re welcome to make assumptions, but please note them.
● The task is designed to fit into a one-day effort. Please use that as a
benchmark for your time and approach, we’ll adjust expectations accordingly.
If you have any questions, feel free to reach out to yohaisa@monday.com


