**ANALYSIS RULES**
* Do not sample the data, use all of the data within the defined boundaries. If boundaries are ambiguous, ask user to provide a date range or member phone number

**Parameters:**
* **CURRENT_YEAR** is the date range from 1st January 2024 and 31 Dec 2024. 
* **PREVIOUS_YEAR** is the date range from 1st January 2023 and 31 Dec 2023

**Instructions**
Create a report that answers the following questions for overall group chat
* How many messages were sent in the CURRENT_YEAR? how does that compare with the number of messages were sent in the PREVIOUS_YEAR
* How many unique members sent messages in the CURRENT_YEAR?
* What is the average number of members that send a message in a 30 day window in the CURRENT_YEAR?
* Top 5 members by messages sent between 1st January 2024 and 31 Dec 2024? compare this with messages sent by top 5 members in the CURRENT_YEAR? How does this compare to the PREVIOUS_YEAR?
* Top 5 members by active days in the CURRENT_YEAR?
* Summary of chat messages in the CURRENT_YEAR?
* Top 5 Dates of highest activity and summary of discussions

**Output format**
Use the template below to format the report

```
  *Chat Insights <CURRENT_YEAR>*
--------------------------------

*Summary*

Messages: <number of messages sent in CURRENT_YEAR> (📉-x% y/y)
Active Members : <number of unique members between START_DATE and END_DATE> (📉-x y/y)
Avg. 30d Retention : <average number of members that send a message in a 30 day window> (📉-x ppts y/y)

*Top members by messages sent*

1. <SENDER 1> : <number of messages sent in CURRENT_YEAR> (📈 +x% y/y)
2. <SENDER 2> : <number of messages sent in CURRENT_YEAR> (📈 +x% y/y)
3. ....

*Left Top 5*

4. <SENDER 13> : <number of message sent in CURRENT_YEAR> (📉 +x% y/y)

Top 5 account for yy% of group messages in CURRENT_YEAR (up from xx% in PREVIOUS_YEAR)

  

*Top members by active days*

1. <SENDER 1> : <number of day active in CURRENT_YEAR> (📈 +x days y/y)
2. <SENDER 2> : <number of day active in CURRENT_YEAR> (📈 +x days y/y)
3. ...

*Left Top 5*

1. <SENDER 3> : <number of day active in CURRENT_YEAR> (📈 +x days y/y)

  

*SUMMARY*
-----------------

<Summary/ description of chat group in 50 words>

<Top 5 dates of highest activity and relevant summary>
```