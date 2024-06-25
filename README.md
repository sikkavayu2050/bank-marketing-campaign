# bank-marketing-campaign
The data is related with direct marketing campaigns (phone calls) of a Portuguese banking institution. The classification goal is to predict if the client will subscribe a term deposit.

**Outline:**

A. Attribute Descriptions
I. Bank client data
II. Related with the last contact of the current campaign
III. Other attributes

B. Structuring the data:
I. Overall Analysis of the Data
II. Data Structuring and Conversions

C. Exploratory Data Analysis (EDA)
I. Accepted vs Rejected Term Deposits
II. Distribution Plots

D. Different Aspects of the Analysis:
I. Months of Marketing Activty
II. Seasonalities
III. Number of Calls to the potential client
IV. Age of the Potential Clients
V. Types of Occupations that leads to more term deposits suscriptions

E. Correlations that impacted the decision of Potential Clients. I. Analysis of our Correlation Matrix
II. Balance Categories vs Housing Loans
III. Negative Relationship between H.Loans and Term Deposits

F. Classification Model
I. Introduction
II. Stratified Sampling
III. Classification Models
IV. Confusion Matrix
V. Precision and Recall Curve
VI. Feature Importances Decision Tree C.

G. Next Campaign Strategy
I. Actions the Bank should Consider

A. Attributes Description:
Input variables:

Ai. bank client data:
1 - age: (numeric)
2 - job: type of job (categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown')
3 - marital: marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)
4 - education: (categorical: primary, secondary, tertiary and unknown)
5 - default: has credit in default? (categorical: 'no','yes','unknown')
6 - housing: has housing loan? (categorical: 'no','yes','unknown')
7 - loan: has personal loan? (categorical: 'no','yes','unknown')
8 - balance: Balance of the individual.

Aii. Related with the last contact of the current campaign:
8 - contact: contact communication type (categorical: 'cellular','telephone')
9 - month: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec')
10 - day: last contact day of the week (categorical: 'mon','tue','wed','thu','fri')
11 - duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.

Aiii. other attributes:
12 - campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
13 - pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
14 - previous: number of contacts performed before this campaign and for this client (numeric)
15 - poutcome: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')

Output variable (desired target):
21 - y - has the client subscribed a term deposit? (binary: 'yes','no')
