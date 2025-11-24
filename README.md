Bright.TV Viewing Data Analysis
Overview
This project analyzes Bright.TV user viewing data to uncover trends in daily activity, peak viewing hours, and channel popularity. The goal is to provide actionable insights for improving content scheduling and user engagement.
Dataset
USERID: Unique user identifier
CHANNEL2: Channel watched
RECORDDATE2: Timestamp (UTC)
DURATION2: Session duration (HH:MM:SS)
Cleaned table (tvdata_clean) includes:
RECORD_TS_SA (local time)
DAY_NAME (Mon–Sun)
WATCH_DATE
WATCH_MONTH / MONTH_NUM
WATCH_HOUR
DURATION_SECONDS / HOURS_WATCHED
Analysis Steps
Data Cleaning: Convert timestamps, adjust timezone, calculate duration in seconds/hours.
Exploratory Analysis:
Daily active users & total viewing hours
Peak viewing hours & days
Top channels & session patterns
Insights Extraction: Identify trends for user engagement and content optimization.
Example Queries
---Daily active users & total hours
SELECT DATE(RECORD_TS_SA) AS DAY.
COUNT(DISTINCT USERID) AS DAILY_ACTIVE_USERS,
SUM(DURATION_SECONDS)/3600 AS HOURS_CONSUMED
FROM brighttv1.data2.tvdata_clean
GROUP BY 1
ORDER BY 1;


---Viewing patterns by day
SELECT DAY_NAME,
AVG(DURATION_SECONDS) AS AVG_WATCH_TIME,
COUNT(*) AS SESSION_COUNT
FROM brighttv1.data2.tvdata_clean
GROUP BY 1
ORDER BY SESSION_COUNT;

---Hourly watching patterns
SELECT WATCH_HOUR,
COUNT(*) AS SESSION_COUNT,
AVG(HOURS_WATCHED) AS AVG_HOURS_WATCHED
FROM brighttv1.data2.tvdata_clean
GROUP BY 1
ORDER BY WATCH_HOUR;

files


Key Insights
Peak Days: Friday to Sunday
Peak Hours: 17h00 to 05h00 am


