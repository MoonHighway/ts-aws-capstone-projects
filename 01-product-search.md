# Capstone Project: Serverless Product Search API with Event-Driven Processing

## Objective  
Your mission: Develop a serverless product search API using AWS Lambda, API Gateway, DynamoDB, Kinesis, SQS, and SNS. The system should allow users to search for products efficiently and process product additions asynchronously.

## Tech Stack  
- **TypeScript** - Strong typing, structured API responses, and well-defined interfaces.  
- **AWS Lambda** – Process search queries on-demand, without managing servers.  
- **API Gateway** - Create RESTful endpoints for your product search service.
- **DynamoDB** - Store and retrieve product data using Global Secondary Indexes.
- **Kinesis** - Stream product addition events for real-time processing.
- **SQS** - Queue product processing tasks for asynchronous handling.
- **SNS** - Send notifications to admin team for product additions.

---

## Requirements  
This project is all about creating a simple yet powerful product search service using **AWS Lambda and TypeScript**. Here's what you'll build:  

- **Product Search:** Enable users to search for products stored in DynamoDB using Global Secondary Indexes (GSI) for optimized queries.
  - Accept a search query (`GET /search?query=shoes`).
  - Fetch and return matching products from DynamoDB.
  - Implement efficient query filtering.

- **Asynchronous Processing:** Handle product additions through Kinesis and SQS, ensuring real-time analytics or logging.
  - Create endpoints for adding new products.
  - Stream new product data through Kinesis.
  - Process product additions using SQS for reliable handling.

- **Admin Notifications:** Notify the admin team via SNS whenever a new product is added.
  - Configure SNS topics and subscriptions.
  - Send detailed product information in notifications.
  - Include timestamps and relevant metadata.

- **TypeScript Best Practices** – Use interfaces to keep your API responses and query parameters well-structured and predictable.  

---

## Sample Product Data  
To populate your **DynamoDB table**, use the following sample dataset.

<details>
  <summary>Click to expand sample data 📂 </summary>

  ```json
  [
    {
      "id": "1",
      "name": "Running Shoes",
      "category": "Footwear",
      "price": 99.99,
      "rating": 4.5,
      "stock": 50,
      "description": "Lightweight running shoes for all terrains.",
      "brand": "Nike",
      "created_at": "2024-03-01T12:00:00Z"
    },
    {
      "id": "2",
      "name": "Wireless Headphones",
      "category": "Electronics",
      "price": 149.99,
      "rating": 4.7,
      "stock": 30,
      "description": "Noise-canceling wireless headphones with 40-hour battery life.",
      "brand": "Sony",
      "created_at": "2024-03-02T10:30:00Z"
    },
    {
      "id": "3",
      "name": "Smartwatch",
      "category": "Wearables",
      "price": 199.99,
      "rating": 4.3,
      "stock": 20,
      "description": "Fitness tracking smartwatch with heart rate monitor.",
      "brand": "Apple",
      "created_at": "2024-03-02T15:45:00Z"
    }
  ]
  ```
</details>

---

## Extra Credit!   
Feeling ambitious? Try adding one (or all) of these enhancements:  

- **Search Autocomplete** – Make your search smarter by implementing basic prefix-matching for suggestions.  
- **Deploy to AWS** – Get your API up and running with a complete cloud architecture.  
- **Basic Sorting** – Let users sort results by price, rating, or other criteria.  
- **Analytics Pipeline** – Track product search patterns and popular items.
- **Admin Dashboard** – Create a simple interface for viewing notifications and product data.

---

## Submission Requirements  
- **GitHub Repo** – Include `index.ts` (your Lambda function) and `README.md` with instructions.  
- **Architecture Diagram** – Show how your AWS services connect together.
- **Short Demo** – Be ready to show your system working live during presentation. 

---

This project is a great way to flex your TypeScript skills while getting hands-on with AWS and event-driven architecture. Keep it simple, focus on the core functionality first, and if you have extra time, tackle some of the bonus features.
