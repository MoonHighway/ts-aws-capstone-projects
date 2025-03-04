# Capstone Project: Subscription Management System

## Objective  
Your mission: Build a **serverless subscription management system** that handles recurring payments, subscriber tracking, and lifecycle events using **TypeScript, AWS Lambda, DynamoDB, and Step Functions**, with **Datadog** for monitoring.

## Tech Stack  
- **TypeScript** - Strong typing for defining subscription models and payment interfaces.  
- **AWS Lambda** – Process subscription events, payments, and notifications.  
- **DynamoDB** – Store subscriber data, payment history, and subscription status.  
- **AWS Step Functions** – Orchestrate simple subscription workflows.

---

## Requirements  
This project focuses on creating a robust subscription management system for a SaaS product. Here's what you'll build:  

- **Subscription API** – Create Lambda functions that:  
  - Handle subscription creation, updates, and cancellations.
  - Process recurring payments (simulated).
  - Track subscription status changes.

- **Subscriber Management** – Use DynamoDB to:  
  - Store subscriber information and their active subscriptions.
  - Maintain payment history and subscription tier details.

- **Simple Workflow** – Implement a basic Step Function to:
  - Manage subscription status changes (active → canceled or past_due).
  - Handle basic subscription events.

- **Console Logging** – Add simple logging for subscription operations.

---

## Sample Subscription Data  
To populate your **subscription system**, use the following sample dataset.

<details>
  <summary>Click to expand sample data 📂 </summary>

  ```json
  [
    {
      "subscriber_id": "sub_001",
      "email": "john.doe@example.com",
      "plan_tier": "premium",
      "price": 19.99,
      "billing_cycle": "monthly",
      "start_date": "2024-02-01T00:00:00Z",
      "next_billing_date": "2024-04-01T00:00:00Z",
      "status": "active",
      "payment_method": {
        "type": "credit_card",
        "last_four": "4242",
        "expiry": "01/2026"
      },
      "payment_history": [
        {
          "transaction_id": "tx_12345",
          "amount": 19.99,
          "status": "succeeded",
          "date": "2024-02-01T10:30:00Z"
        },
        {
          "transaction_id": "tx_12346",
          "amount": 19.99,
          "status": "succeeded",
          "date": "2024-03-01T10:32:15Z"
        }
      ]
    },
    {
      "subscriber_id": "sub_002",
      "email": "jane.smith@example.com",
      "plan_tier": "basic",
      "price": 9.99,
      "billing_cycle": "monthly",
      "start_date": "2024-01-15T00:00:00Z",
      "next_billing_date": "2024-04-15T00:00:00Z",
      "status": "active",
      "payment_method": {
        "type": "paypal",
        "email": "jane.smith@example.com"
      },
      "payment_history": [
        {
          "transaction_id": "tx_12347",
          "amount": 9.99,
          "status": "succeeded",
          "date": "2024-01-15T14:22:10Z"
        },
        {
          "transaction_id": "tx_12348",
          "amount": 9.99,
          "status": "succeeded",
          "date": "2024-02-15T14:25:30Z"
        },
        {
          "transaction_id": "tx_12349",
          "amount": 9.99,
          "status": "succeeded",
          "date": "2024-03-15T14:20:45Z"
        }
      ]
    },
    {
      "subscriber_id": "sub_003",
      "email": "alex.wilson@example.com",
      "plan_tier": "premium",
      "price": 19.99,
      "billing_cycle": "monthly",
      "start_date": "2024-02-20T00:00:00Z",
      "next_billing_date": "2024-03-20T00:00:00Z",
      "status": "past_due",
      "payment_method": {
        "type": "credit_card",
        "last_four": "5678",
        "expiry": "11/2024"
      },
      "payment_history": [
        {
          "transaction_id": "tx_12350",
          "amount": 19.99,
          "status": "succeeded",
          "date": "2024-02-20T09:15:22Z"
        },
        {
          "transaction_id": "tx_12351",
          "amount": 19.99,
          "status": "failed",
          "date": "2024-03-20T09:18:37Z",
          "failure_reason": "insufficient_funds"
        }
      ]
    }
  ]
  ```
</details>

---

## Extra Credit!   
Ready to make your subscription system even more powerful? Try adding:  

- **Plan Change Handling** – Allow subscribers to upgrade/downgrade with pro-rated billing.
- **Dunning Management** – Implement a payment retry system for failed payments.
- **Usage-Based Billing** – Add support for metered billing based on API calls or resource usage.
- **Simple Notifications** – Send basic email notifications for subscription events.

---

## Submission Requirements  
- **GitHub Repo** – Include your TypeScript Lambda functions, Step Functions definition, and thorough documentation.
- **System Design Document** – Explain your data model and workflow orchestration.
- **Short Demo** – Be ready to show your system working live during presentation.

---

This project will give you practical experience with subscription business models and serverless architecture. 

