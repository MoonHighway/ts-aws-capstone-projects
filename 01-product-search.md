# Capstone Project: Product Search API 

## Objective  
Your mission: Build a **serverless product search API** that allows users to search for products using **TypeScript and AWS Lambda**, powered by **ElasticSearch** for fast and efficient results.  

## Tech Stack  
- **TypeScript** - Strong typing, structured API responses, and well-defined interfaces.  
- **AWS Lambda** – Process search queries on-demand, without managing servers.  
- **ElasticSearch** – Store and retrieve product data quickly and efficiently.  

---

## Requirements  
This project is all about creating a simple yet powerful product search service using **AWS Lambda and TypeScript**. Here’s what you’ll build:  

- **Basic Product Search API** – Create a Lambda function that:  
  - Accepts a search query (`GET /search?query=shoes`).  
  - Fetches and returns matching products from ElasticSearch.  

- **ElasticSearch Integration** – Store a small sample of product data and retrieve relevant results.  

- **TypeScript Best Practices** – Use interfaces to keep your API responses and query parameters well-structured and predictable.  

---

## Sample Product Data  
To populate your **ElasticSearch index**, use the following sample dataset.

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
- **Deploy to AWS** – Get your API up and running with AWS API Gateway.  
- **Basic Sorting** – Let users sort results by price, rating, or other criteria.  

---

## Submission Requirements  
- **GitHub Repo** – Include `index.ts` (your Lambda function) and `README.md` with instructions.  
- **Deployed API Link (optional)** – Share your API Gateway URL so others can test it.  
- **Short Demo** – Be ready to show your system working live during presentation. 

---

This project is a great way to flex your TypeScript skills while getting hands-on with AWS and ElasticSearch. Keep it simple, focus on the core functionality first, and if you have extra time, tackle some of the bonus features.  
