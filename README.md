# Chat Data Analytics (Customer Care / Call Centre / Helpline)

This is demo project illustrating a real life company problem where we have to build an automatic script which will read, process and save the results to an excel (xlsx format) file in an automatic way.
#
We have a toy dataset for a company's customer care centre (call centre/help centre) focusing on the chat times and responses by the agents as well as bot.

The details/explanation about the different columns is given in 'Chat Data Analystics.xlsx' file in 'Columns Explanation' worksheet. 
#
We have to calculate Chat metrics and Agent Metrics separately in different worksheets in the format as specified in 'Report Format - Chat Data Metrics.xlsx' file.

Explanation for calculating various metrics is given as under:-

#### Chat Metrics:-

1. Incoming Chats - Use RoomCode column to count the number of Incoming Chats
2. Unique Users - Use UserId column & count the distinct number of UserId’s to get the number of Unique Users
3. Closed By Bot - Use ClosedBy column and apply a filter to select only the rows where Closed by is an 'Automated System'
4. Bot Deflection % - Formula for this is Closed By/ Incoming Chats
5. Closed By Agents - Use ClosedBy column and apply a filter to exclude all the rows where Closed by is 'Automated System' i.e. it should be closed by a human

#### Agent Metrics:-

Agents are the unique values, apart from Bot & System, in the ClosedBy column. Basically, names of people. For each agent -

1. Chats Resolved By Agents: Calculate the total chats resolved.
2. Agent First Response Time: Calculate Average First Response Time by using AgentFirstResponseTime column.
3. Agent Chat Resolution Time: Calculate Average Chat Resolution Time by subtracting ChatStartTime from ChatEndTime.
4. Agent CSAT: Find the average CSAT Score.
5. Agent CSAT Business Hours: Business hours are 10AM - 5PM. Find the average CSAT Score in these hours.

#
 
As per the format given in 'Report Format - Chat Data Metrics.xlsx', all data is expected to be in a weekly format as per the dates mentioned there.
Also, the ouput file should be in excel (.xlsx) format and it should have 2 tables in 2 separate worksheets for the required metrics.

#### Note: Details regarding the data analytics process is explained and shown in 'Chat Data Project.ipnyb' file.
#### Before calculating the metrics, we are performing some sanity checks to confirm data integrity.
#### Also for demonstration purpose, we have used 2 different approaches for calculating metrics 1 and metrics 2.
#### For exporting to excel format we have used pandas 'excelWriter' function and are performing some basic to advanced exporting operations (like word-wrap, text centering, adjusting columns widths, merging cells etc) to get the desired output in excel format.
