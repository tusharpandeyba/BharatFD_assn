# 📌 FAQ Management System

A powerful and efficient FAQ Management System leveraging Node.js, Express, MongoDB, and Redis to deliver fast, multilingual, and scalable FAQ services.
## 🔥 Core Capabilities

- **Fetch all FAQs** with multilingual support (English, Hindi, Bengali).
- **Create new FAQs** with auto-translation.
- **Retrieve a single FAQ efficiently** using Redis caching for faster response times.

---

## 🚀 Features

✅ **Multilingual Support** – FAQs are stored in multiple languages using Google Trans.

✅ **Redis Caching** – Enhances performance by caching frequently accessed FAQs.

✅ **MongoDB Integration** – Stores FAQs efficiently with schema-based validation.

✅ **RESTful API** – Easily integrate with frontend applications.

✅ **Environment Variables** – Uses `.env` for sensitive data management.

---

## 📁 Project Structure

```
📂 faq-management
 ├── 📂 config
 │   ├── db.js            # MongoDB connection setup
 │   ├── redis.js         # Redis connection setup
 │
 ├── 📂 controllers
 │   ├── faqController.js # Controllers handling FAQ CRUD operations
 │
 ├── 📂 models
 │   ├── faqModel.js      # Mongoose schema for FAQs
 │
 ├── 📂 routes
 │   ├── faqRoutes.js     # API routes for FAQ operations
 │
 ├── 📂 utils
 │   ├── translate.js     # Google Translate API utility
 │
 ├── .env                 # Environment variables
 ├── package.json         # Dependencies and scripts
 ├── server.js            # Entry point for Express server
```

---

## 🛠️ Installation & Setup

### Prerequisites
Ensure you have **Node.js** and **MongoDB** installed.

### 1️⃣ Clone the Repository
```bash
$ git clone https://github.com/webdesignbysubhasis6/faq-backend.git
$ cd faq-management
```

### 2️⃣ Install Dependencies
```bash
$ npm install
```

### 3️⃣ Setup Environment Variables
Create a `.env` file in the root directory and configure it:
```env
MONGO_URI=mongodb://localhost:27017/faq-db
REDIS_HOST=localhost
REDIS_PORT=10812
REDIS_PASS=your_redis_password
```

### 4️⃣ Start the Server
```bash
$ npm start
```

The API will be available at: `http://localhost:5000`

---

## 📌 API Endpoints

### ✅ Get All FAQs
**GET** `/api/faqs?lang={language}`

📌 Fetch all FAQs. If no language is provided, English (`en`) is used by default.

### ✅ Get a Specific FAQ (With Redis Caching)
**GET** `/api/faqs/getOne?id={faq_id}&lang={language}`

📌 Retrieves a specific FAQ and caches the result for **faster responses**.

### ✅ Add a New FAQ
**POST** `/api/faqs/addFaq`

📌 Adds a new FAQ and automatically translates it into **Hindi** and **Bengali**.

#### 📤 Request Body (JSON)
```json
{
  "question": "What is Node.js?",
  "answer": "Node.js is a JavaScript runtime."
}
```

---

## 🛡️ Technologies Used

- **Node.js & Express.js** – Backend framework
- **MongoDB & Mongoose** – Database & ODM
- **Redis** – Caching layer
- **Google Trans** – Text translation
- **dotenv** – Environment variable management

---

## 👨‍💻 Contributors
- **Tushar Pandey** – [GitHub](https://github.com/tusharpandeyba/)

---


