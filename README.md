# Establishing a Basic Security Baseline Using SQL
(Basic Fingerprint & Login Event Analysis)
________________________________________
# Overview
This repository contains SQL practice queries and examples focused on learning how to establish a basic security baseline using authentication data such as fingerprint scans and login events.
The exercises was designed to strengthen understanding of SQL fundamentals while applying them to real-world security monitoring scenarios. The focus is on identifying normal behavior patterns, detecting anomalies, and analyzing authentication activity using basic SQL syntax.
________________________________________
# Purpose

• Practice and reinforce foundational SQL skills

• Learn how to analyze fingerprint and login event data

• Establish a basic behavioral baseline for authentication systems

• Prepare for cybersecurity and IT operations roles

• Serve as a personal reference for security-focused SQL patterns
________________________________________
# Topics Covered

• SELECT statements

• Data filtering (WHERE, ORDER BY, LIMIT)

• Aggregate functions (COUNT, AVG, MIN, MAX)

• GROUP BY and HAVING

• JOINs (INNER, LEFT)

• Conditional logic using CASE

• Identifying failed vs successful login attempts

• Detecting unusual login times or frequency

• Basic anomaly detection using SQL
________________________________________
# Example Use Cases

• Count total login attempts per user

• Identify users with excessive failed login attempts

• Determine average login frequency per day

• Detect login attempts outside business hours

• Correlate fingerprint scans with login activity
________________________________________
# Project Structure
/sql-security-baseline

├── fingerprint.txt and login_events.txt                 
#Practice queries for fingerprint & login event analysis

└── README.md                       
#Project documentation
________________________________________
# Requirements

• Notepad

• Basic understanding of SQL syntax
________________________________________
# How to Use
1.	Open the fingerprint.txt and login_events.txt file.
2.	Review the schema and sample data structure.
3.	Attempt to write your own queries by looking at the schema.
4.	Compare your approach with the provided baseline queries.
5.	Modify filters, grouping, and conditions to explore different scenarios.
________________________________________
# Example Queries
Count total login attempts per user:
SELECT user_id, COUNT(*) AS total_logins
FROM login_events
GROUP BY user_id;
Identify failed login attempts:
SELECT user_id, COUNT(*) AS failed_attempts
FROM login_events
WHERE status = 'Failed'
GROUP BY user_id
HAVING COUNT(*) > 5;
Detect logins outside business hours:
SELECT user_id, login_time
FROM login_events
WHERE HOUR(login_time) < 8 OR HOUR(login_time) > 18;
________________________________________
# Notes

• These queries are for educational and practice purposes.

• Baseline results may vary depending on dataset size, naming and structure.

• There are multiple ways to write effective SQL queries — optimization and readability both matter.

• This project bridges SQL fundamentals with real-world security monitoring concepts.
________________________________________
# Future Improvements

• Add different levels (Beginner / Intermediate / Advanced)

• Include deeper explanations for each query

• Potentially add simulated datasets for realistic testing

• Explore performance optimization techniques

• Expand into anomaly detection with more advanced SQL
________________________________________
# License
No license specified. This repository is intended for personal learning and practice.
________________________________________
# Credit
Adam P and ChatGPT
