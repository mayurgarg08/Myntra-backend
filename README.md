# Myntra Clone: Backend

A lightweight Express API that serves the product catalogue for the [Myntra clone frontend](https://github.com/mayurgarg08/Myntra-frontend). Products are stored in a local `items.json` file, so no database is needed.

## Features

- List all products, fetch one by ID, and add new products
- File-based storage (`items.json`) using `fs/promises`
- CORS enabled for all origins
- An artificial 2-second delay on `GET /items` so the frontend's loading state can be seen

## Tech stack

Node.js · Express · body-parser

## API

Base URL: `http://localhost:8080`

| Method | Endpoint | Description |
| --- | --- | --- |
| GET | `/items` | All products: `{ items: [...] }` |
| GET | `/items/:id` | One product: `{ item }` |
| POST | `/items` | Add a product (JSON body). Returns `201` with the new item. |

### Product shape

```json
{
  "id": "001",
  "image": "images/1.jpg",
  "company": "Carlton London",
  "item_name": "Rhodium-Plated CZ Floral Studs",
  "original_price": 1045,
  "current_price": 606,
  "discount_percentage": 42,
  "return_period": 14,
  "delivery_date": "10 Oct 2023",
  "rating": { "stars": 4.5, "count": 1400 }
}
```

## Project structure

```
app.js           Express server and routes
data/items.js    read/write helpers for items.json
items.json       product data
```

## Getting started

### Prerequisites
- Node.js 18+

```bash
git clone https://github.com/mayurgarg08/Myntra-backend.git
cd Myntra-backend
npm install
npm start        # http://localhost:8080
```

Then start the [frontend](https://github.com/mayurgarg08/Myntra-frontend).

## Author

**Mayur Garg** · [GitHub](https://github.com/mayurgarg08) · [LinkedIn](https://www.linkedin.com/in/mayur-garg-428a291b4/)
