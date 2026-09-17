AnalystLab Africa — FinTrust Business & Data Intelligence Assessment


Part A — Business Understanding
What business questions should FinTrust's management be able to answer?

Who are our most profitable and high-value customer segments, and which acquisition channels yield the lowest churn rates?
What are the peak transaction periods, and which payment channels are experiencing the fastest adoption or highest failure rates?

What indicators or transaction patterns strongly correlate with high risk and potential fraud (Risk review flag), and how quickly can we spot them?
What is the average transaction value per customer type, and what is the overall customer lifetime value trend?

What decisions could data analysis support?
Allocating marketing budgets toward the most profitable transaction channels and customer acquisition routes.
Setting automated triggers and rules for flagged transactions to reduce fraud loss without harming user experience.
Improving UI/UX or infrastructure for channels experiencing high drop-off or failure rates.
Identifying at-risk or churning customers early to launch proactive engagement and loyalty campaigns.

What stakeholders could benefit from the analytical outputs?
Executive Management / C-Suite: For high-level strategic planning, budget allocation, and tracking overall business health via KPIs.
Risk and Compliance Teams: For monitoring fraudulent activities, reviewing flagged accounts, and ensuring regulatory adherence.
Marketing and Sales Teams: For designing data-driven campaigns, understanding user behavior, and improving customer targeting.
Product and Engineering Teams: For tracking system performance, reducing transaction errors, and optimizing platform features.


Part B — Data Understanding / Profiling Report
1. Document Overview (Dataset Sizes)
Customer Dataset: 1,501 rows, 12 columns
Transaction Dataset: 13 rows, 7 columns
Data Dictionary Dataset: 13 rows, 7 columns
2. Field Names & Data Types
Customer Dataset (12 Columns):
Customer id: Numeric (Integer)
Customer name: Text
Age: Numeric
gender: Numeric
city: Text
Customer Segment: Text
Account type: Text
Tenure month: Numeric
Digital engagement: Decimal
Monthly income: Numeric
Preferred channel: Text
Account status: Text
Transaction Dataset (7 Columns):
Transaction Id: Mixed-type Column (Alphanumeric text)
Customer Id: Numeric (Foreign key)
Transaction - date/Time: Date/Time
Transaction type: Text
Amount: Numeric (Float/Decimal)
Channel: Text
Device type: Text
Location: Text
International transaction: Text
Transaction Status: Text
Risk review flag: Text
Data Dictionary Dataset (7 Columns):
Customerid: Text | Dataset: Text | Datatype: Text | Example: Mixed type / Colour | Definition: Text | Business use: Text | Modelling use: Text

3. Relationship Between the Datasets
The datasets share a one-to-many (1:N) relationship connected via the Customer Id field.
A single customer appears only once in the Customer Dataset (the "one" side), but can appear multiple times across the Transaction Dataset (the "many" side) as they perform transactions over time.

4. Missing Values & Obvious Data Quality Issues
Missing Values: Minor null values or gaps may exist within optional descriptive fields or location attributes.
Data Quality Notes:
The Transaction Id field contains alphanumeric mixed-type values requiring proper string handling.
Date-time formats in transaction logs must be standardized before time-series aggregation.


Part C — Analytical Questions
Customer Behavior: Which customer segments exhibit the highest frequency of active transactions month-over-month?
Transaction Activity: What are the peak transaction periods (by hour of the day and day of the week) across the platform?
Transaction Value: What is the average transaction value, and how does spending volume differ across various customer segments or geographical regions?
Transaction Channels: Which payment channels account for the highest total transaction volume and value?
Transaction Status: What percentage of transactions fail or remain pending, and do failure rates cluster around specific payment channels or time frames?
Risk-Related Patterns: What transaction patterns or characteristics correlate most strongly with a positive Risk review flag?
Cross-Area Impact: Is there a noticeable relationship between specific customer segments and the frequency of triggering risk review flags?


Part D — KPI Planning
KPI DefinitionWhy It MattersRequired Data
Total Transaction Volume & Value
The aggregate count and monetary sum of all successful transactions processed over a given period.Gives management a high-level view of business growth, revenue generation, and overall platform throughput.Amount, Transaction Status, Transaction - date/Time
Customer Churn Rate
The percentage of customers who stop using FinTrust’s services or close their accounts over a specific timeframe.High churn directly impacts revenue and indicates customer dissatisfaction or market competition.Account status, Tenure month, Customer id
Transaction Success Rate
The proportion of total attempted transactions that successfully complete versus those that fail or error out.Highlights technical reliability, channel performance, and user experience friction points.Transaction Status, Channel, Transaction Id
Risk Flag Rate (Fraud Indicator)
The percentage of total transactions or customers flagged by the system for risk review.Essential for monitoring compliance, preventing fraudulent losses, and securing the platform safely.Risk review flag, Transaction Id, Amount
Average Monthly Income per Segment
The average declared monthly income grouped by customer segment (e.g., Retail vs. SME).Helps marketing and product teams understand the financial demographics of their user base to tailor offerings.Monthly income, Customer Segment
Digital Engagement Score
An average measure of how actively customers interact with FinTrust's digital platforms over time.High engagement strongly correlates with customer retention and higher lifetime value.Digital engagement, Tenure month, Customer id


Part E — Dashboard Planning
1. Proposed Dashboard Sections:
Executive Summary & Overview (High-level health of the business)
Customer Demographics & Segmentation (Who our users are and their financial profile)
Transaction Performance & Channel Analysis (Volume, success rates, and payment methods)
Risk & Fraud Monitoring (Flagged accounts and security oversight)
2. Key KPI Cards:
Total Transaction Volume & Value
Transaction Success Rate
Active Customer Count
Risk Flag Rate

3. Charts & Visuals:
Donut/Pie Chart: Distribution of customers across Customer Segment and Account status.
Bar Chart: Total transaction volume by Channel and Device type.
Line Chart: Transaction trends over time (Transaction - date/Time) to spot peak periods.
Regional Bar Chart: Transaction volume breakdown by City or Location.

4. Filters / Slicers:
Date Range Slicer
Customer Segment Filter
Channel Filter
Risk Review Status Filter

5. Major Insights Expected to be Communicated:
Identifying which customer segments generate the highest transaction volume and monthly income.
Spotting which payment channels or device types experience the highest rates of transaction failures.
Pinpointing clusters of risk-flagged transactions to help the compliance team preemptively mitigate fraud
