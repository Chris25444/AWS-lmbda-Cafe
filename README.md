# AWS Cafe Sales Analysis – Serverless Project

# Overview
This project demonstrates a serverless sales reporting system built on AWS. It automates the extraction of daily café sales data from a MySQL database hosted on an EC2 LAMP stack instance, processes product order quantities, and delivers formatted email reports to subscribers on a scheduled basis.

The solution uses AWS Lambda functions to query the database, retrieve sales metrics, format the data, and publish reports via Amazon SNS. The workflow is triggered automatically by Amazon EventBridge (CloudWatch Events) every evening, eliminating the need for manual report generation and ensuring stakeholders receive timely insights without managing servers.

# Architecture
- Lambda functions:
  - salesAnalysisReport
  - salesAnalysisReportDataExtractor
- Other services:
  - SNS, EventBridge (CloudWatch Events), Systems Manager Parameter Store, RDS/MySQL or EC2 DB, VPC

# Features
- Daily email sales report via SNS
- Lambda scheduled with EventBridge
- Database data extraction using PyMySQL and Lambda layer

# IAM & Security
- IAM roles for Lambda
- VPC, subnets, security groups

# Diagram
<img width="1159" height="629" alt="image" src="https://github.com/user-attachments/assets/6dbfd408-fc27-4f1a-b3ef-98db7d3087e7" />
