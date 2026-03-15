# IN226005302_FASTAPI

# 🛒 FastAPI Cart System

**Innomatics Research Labs – Internship Task**

This project was developed as part of my **Backend Development Internship at Innomatics Research Labs**.
The goal of this task was to build a **RESTful Shopping Cart API using FastAPI** and understand how backend systems manage products, cart operations, and order processing.

The API allows users to browse products, add items to a cart, update quantities, remove items, and perform checkout operations while handling errors properly.

---

# 🎯 Internship Task Objective

The objective of this task was to practice:

* Building REST APIs using **FastAPI**
* Using **Pydantic models for request validation**
* Implementing **cart logic and order workflows**
* Handling **HTTP status codes and errors**
* Testing APIs using **Swagger UI**

---

# 🚀 Features Implemented

### Product System

* Retrieve all available products
* Each product contains:

  * Product ID
  * Name
  * Price
  * Category
  * Stock availability

### Cart System

* Add products to the cart
* Update quantity if product already exists in cart
* Calculate subtotal for each item
* Calculate cart grand total
* Remove items from the cart
* View cart contents

### Checkout System

* Checkout items from cart
* Store orders in the system
* Clear cart after successful checkout

### Error Handling

The API properly handles cases such as:

* Product not found
* Product out of stock
* Checkout with empty cart

---

# 🛠 Tech Stack

* **Python**
* **FastAPI**
* **Pydantic**
* **Uvicorn**
* **Swagger UI (for API testing)**

---

# 📂 Project Structure

```
project-folder
│
├── main.py       # FastAPI backend application
├── README.md     # Project documentation
```

---

# ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```
git clone https://github.com/your-username/fastapi-cart-system.git
```

### 2️⃣ Navigate to the Project Folder

```
cd fastapi-cart-system
```

### 3️⃣ Install Dependencies

```
pip install fastapi uvicorn
```

---

# ▶️ Running the Application

Start the FastAPI server using:

```
uvicorn main:app --reload
```

The API will run on:

```
http://127.0.0.1:8000
```

---

# 📑 API Documentation

FastAPI automatically generates interactive documentation.

Open Swagger UI:

```
http://127.0.0.1:8000/docs
```

This interface allows testing all endpoints directly in the browser.

---

# 🔗 API Endpoints

## Products

### Get All Products

```
GET /products
```

---

## Cart

### Add Item to Cart

```
POST /cart/add
```

Parameters:

* `product_id`
* `quantity`

---

### View Cart

```
GET /cart
```

---

### Remove Item from Cart

```
DELETE /cart/{product_id}
```

---

## Checkout

### Checkout Cart

```
POST /cart/checkout
```

Example Request Body:

```
{
  "customer_name": "John",
  "delivery_address": "Hyderabad, India"
}
```

---

## Orders

### View Orders

```
GET /orders
```

---

# 🧪 Example Workflow

1. Retrieve products from `/products`
2. Add products to cart using `/cart/add`
3. View cart details using `/cart`
4. Remove items if needed
5. Checkout using `/cart/checkout`
6. View placed orders using `/orders`

---

# 📌 Important Note

The cart and order data are stored **in memory**, so all data resets whenever the server restarts.
This behavior is expected for this internship task.

---

# 👨‍💻 Author

**Yashvin**
AI & Data Science Student
Backend Development Intern – **Innomatics Research Labs**
