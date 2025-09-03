# Serverless-Registration-WebApp

## 🚀 Introduction
A serverless registration form using AWS Lambda, DynamoDB, and API Gateway. This project stores user registration data in Amazon DynamoDB through an AWS Lambda function triggered by an API Gateway endpoint. The system is cost-efficient, scalable, and serverless.

## 🚀 Features
Serverless Architecture: Uses AWS Lambda and DynamoDB, eliminating the need for traditional servers.

Secure Data Storage: Stores user registration details in DynamoDB.

Event-Driven Processing: API Gateway triggers the Lambda function upon form submission.

Cross-Origin Resource Sharing (CORS) Enabled: Allows access from different domains.

Scalable and Cost-Effective: Uses AWS’s pay-as-you-go model.

## 🚀 Project Layout
<img width="815" alt="Screenshot 2025-01-30 at 9 40 18 PM" src="https://github.com/user-attachments/assets/6fed34a5-ecfc-457a-84bd-b256a960894f" />

## 🚀 STEPS
### Step 1: Create a DynamoDB Table
Table Name: table-for-registration
Partition Key: email (String)

<img width="1507" alt="Screenshot 2025-01-30 at 6 45 34 PM" src="https://github.com/user-attachments/assets/6fc4c0fe-e1ee-4bcc-9267-23ab9350c4e0" />


### Step 2: Create IAM Role for Lambda

Role Name: RegistrationFormRole
Choose Lambda for Use Case

Attach the following policies:
AmazonDynamoDBFullAccess,
CloudWatchFullAccess

<img width="1510" alt="Screenshot 2025-01-30 at 6 48 08 PM" src="https://github.com/user-attachments/assets/9722b159-08ed-44b5-bbee-75b6d5d33ba2" />


### Step 3: Create a Lambda Function

Function name: Registration-Form

Runtime: Python 3.9

<img width="1512" alt="Screenshot 2025-01-30 at 6 49 49 PM" src="https://github.com/user-attachments/assets/bf303735-7f07-4c6b-a1a7-cebb89aab6b2" />

### Step 4: Write the Lambda Function

Paste the Lambda python code script in the code source area and deploy.
<img width="1287" alt="Screenshot 2025-01-30 at 6 54 31 PM" src="https://github.com/user-attachments/assets/cfc7da81-5858-4b71-9389-cdf28686f30f" />

### Step 5: Create entries in the DynamoDB Table

Make the follwoing empty entries to the table:
<img width="1510" alt="Screenshot 2025-01-30 at 6 57 11 PM" src="https://github.com/user-attachments/assets/ccaf5fcc-b4f4-4284-9e47-927d5fe0db79" />

### Step 6: Create API Gateway and enable CORS

REST API Name: Registration-API

Create resources further:

A resource: /register

and a POST method to this:
<img width="1503" alt="Screenshot 2025-01-30 at 7 00 12 PM" src="https://github.com/user-attachments/assets/e605596e-0bf1-4e47-b5ad-429afa2ae139" />

Enable CORS from the /register resource and then Deploy the API.

### Step 7: Copy the URL to script.js

<img width="1285" alt="Screenshot 2025-01-30 at 7 03 10 PM" src="https://github.com/user-attachments/assets/39ca9696-c83a-4b99-9377-0e5da203c880" />




