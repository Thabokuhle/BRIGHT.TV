# Bright.TV Viewer Behavior Analysis

This project analyzes viewer behavior for Bright.TV using timestamped viewing data. The objective is to understand when users watch, how long they watch, and which channels attract the most engagement. The analysis supports content scheduling, programming decisions, and overall viewer insight development.

## Project Overview
The dataset contains user IDs, channels, timestamps, and viewing duration. The workflow includes converting timestamps to South African time, extracting analytical features, and generating insights through structured analysis.

## Objectives
- Clean and standardize raw viewing logs  
- Convert all timestamps from UTC to Africa/Johannesburg  
- Extract key features: date, month, day of week, and hour of day  
- Calculate viewer watch duration in hours  
- Build pivot tables and charts to identify trends  

## Key Analysis Conducted
- Viewership by hour (0–23)  
- Viewer distribution across days of the week  
- Monthly viewing patterns  
- Channel performance comparisons  
- Total hours watched across time periods and channels  

## Tools Used
- Miro for planing
- Snowflake SQL  
- Excel/google sheet (Pivot Tables & Charts)
- Canva for presantation
- GitHub for version control and documentation

  ## Files
## excel
- Viewing_By_Day_Week.pdf
- Viewing_By_Hour_Of_Day.pdf
- Viewing_By_Month
## Miro
- Flowchart.pdf
## sql
- TV-data_cleaned.sql
## data_cleaned
- BrightTv.csv
## data_raw
- brightTV Case Study
- BrightTV_Viewership.csv

## Repository Structure
BrightTV-Analysis/
│── data_raw/ → Original uncleaned data
│── data_clean/ → Cleaned dataset exported from SQL
│── sql/ → SQL scripts used for cleaning & transformation
│── excel/ → Pivot tables and charts
│── README.md → Project documentation

## Summary
This project transforms raw viewer logs into a structured, analysis-ready dataset. The resulting insights highlight viewer patterns that can help Bright.TV improve scheduling decisions, increase viewer retention, and better understand audience 
