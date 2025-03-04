# Capstone Project: Real-time Fraud Detection System

## Objective  
Your mission: Build a serverless real-time fraud detection system for e-commerce transactions using TypeScript, AWS Lambda, DynamoDB, and Kinesis.

## Tech Stack  
- **TypeScript** - Strong typing, well-defined interfaces for transaction data modeling.  
- **AWS Lambda** – Process transaction events in real-time, detecting potential fraud.  
- **Amazon Kinesis** – Capture and process streaming transaction data.
- **DynamoDB** – Store transaction records and fraud detection results.

---

## Requirements  
This project focuses on building a serverless fraud detection system that analyzes e-commerce transactions in real-time. Here's what you'll build:  

- **Transaction Processor** – Create a Lambda function that:  
  - Consumes transaction events from Kinesis stream.
  - Applies basic fraud detection rules to each transaction.
  - Flags suspicious transactions based on predefined criteria.

- **Transaction Storage** – Use DynamoDB to:
  - Store transaction records with fraud detection results.
  - Track historical transaction patterns for each user.

- **Basic Logging** – Include simple console logging for important events.

---

## Sample Transaction Data  
To test your fraud detection system, use the following sample dataset.

<details>
  <summary>Click to expand sample data 📂 </summary>

  ```json
  [
    {
      "transaction_id": "t-12345",
      "user_id": "user-789",
      "amount": 129.99,
      "currency": "USD",
      "payment_method": "credit_card",
      "card_last_four": "4242",
      "billing_postal_code": "10001",
      "shipping_postal_code": "10001",
      "ip_address": "192.168.1.1",
      "user_agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7)",
      "timestamp": "2024-03-01T14:23:45Z"
    },
    {
      "transaction_id": "t-12346",
      "user_id": "user-789",
      "amount": 899.99,
      "currency": "USD",
      "payment_method": "credit_card",
      "card_last_four": "4242",
      "billing_postal_code": "10001",
      "shipping_postal_code": "90210",
      "ip_address": "203.0.113.42",
      "user_agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64)",
      "timestamp": "2024-03-01T14:28:12Z"
    },
    {
      "transaction_id": "t-12347",
      "user_id": "user-456",
      "amount": 79.99,
      "currency": "USD",
      "payment_method": "paypal",
      "billing_postal_code": "94105",
      "shipping_postal_code": "94105",
      "ip_address": "198.51.100.73",
      "user_agent": "Mozilla/5.0 (iPhone; CPU iPhone OS 15_0 like Mac OS X)",
      "timestamp": "2024-03-01T15:05:22Z"
    },
    {
      "transaction_id": "t-12348",
      "user_id": "user-789",
      "amount": 1299.99,
      "currency": "USD",
      "payment_method": "credit_card",
      "card_last_four": "9876",
      "billing_postal_code": "10001",
      "shipping_postal_code": "33101",
      "ip_address": "198.51.100.42",
      "user_agent": "Mozilla/5.0 (iPad; CPU OS 15_0 like Mac OS X)",
      "timestamp": "2024-03-01T15:15:30Z"
    }
  ]
  ```
</details>

---

## Fraud Detection Rules  
Implement at least two of these rules to flag potentially fraudulent transactions:

1. **Unusual Amount** – Transaction amount significantly higher than user's average.
2. **Location Mismatch** – Billing and shipping postal codes don't match.
3. **Rapid Transactions** – Multiple purchases from the same user within minutes.
4. **Payment Method Change** – User suddenly using a different payment method or card.

---

## Extra Credit!   
Want to enhance your fraud detection system? Try adding:  

- **Machine Learning Integration** – Use AWS SageMaker to build a simple ML model for fraud prediction.
- **Real-time Alerts** – Send notifications (via SNS) when suspicious transactions are detected.
- **Fraud Score API** – Create an API endpoint to check a transaction's fraud probability.
---

## Submission Requirements  
- **GitHub Repo** – Include your TypeScript code and a basic `README.md`.
- **Simple Diagram** – Sketch how your components connect.
- **Short Demo** – Be ready to show your system working live during presentation.

---

This project gives you hands-on experience with serverless architecture and real-time data processing. 

