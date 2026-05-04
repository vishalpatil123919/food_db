# 🍽️ Food API (Django + MongoDB)

A simple RESTful API built using **Django** and **MongoDB** to manage food items.
This project demonstrates CRUD operations (Create, Read, Update, Delete) using **Django REST Framework** and **PyMongo**.

---

## 🚀 Features

* ✅ Create new food items
* 📖 Retrieve all food items
* 🔍 Get a single food item by ID
* ✏️ Update existing food items
* ❌ Delete food items
* ⚡ Direct MongoDB integration using PyMongo

---

## 🛠️ Tech Stack

* **Backend:** Django, Django REST Framework
* **Database:** MongoDB
* **Library:** PyMongo
* **Language:** Python

---

## 📂 Project Structure

```
MongoAPI/
│
├── Food/
│   ├── views.py        # API logic (CRUD operations)
│   ├── models.py       # (Not used - MongoDB handles schema)
│   ├── dbconnect.py    # MongoDB connection setup
│
├── MongoAPI/
│   ├── settings.py     # Django settings
│   ├── urls.py         # API routes
│
└── manage.py           # Django project manager
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone <your-repo-link>
cd MongoAPI
```

### 2️⃣ Create Virtual Environment (Optional but Recommended)

```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

### 3️⃣ Install Dependencies

```bash
pip install django djangorestframework pymongo
```

### 4️⃣ Start MongoDB

Make sure MongoDB is running locally:

```
mongodb://127.0.0.1:27017/
```

### 5️⃣ Run the Server

```bash
python manage.py runserver
```

---

## 🌐 API Endpoints

### 🔹 Base URL

```
http://127.0.0.1:8000/
```

---

### 🏠 Home

```
GET /
```

**Response:**

```
Welcome to the Food API!
```

---

### 🍔 Get All Foods / Add Food

#### Get All Foods

```
GET /api/foods/
```

#### Add New Food

```
POST /api/foods/
```

**Request Body (JSON):**

```json
{
  "name": "Pizza",
  "price": 250,
  "description": "Cheesy and delicious"
}
```

---

### 🔍 Get Single Food

```
GET /api/foods/{id}/
```

---

### ✏️ Update Food

```
PUT /api/foods/{id}/
```

---

### ❌ Delete Food

```
DELETE /api/foods/{id}/
```

---

## 🧠 How It Works

* MongoDB is connected using **PyMongo** (`dbconnect.py`)
* Data is stored in:

  * Database: `Restaurant`
  * Collection: `food`
* No Django models are used (schema-less design)
* ObjectId is converted to string before sending response

---

## ⚠️ Important Notes

* MongoDB must be running locally
* IDs must be valid MongoDB ObjectIds
* No authentication implemented (open API)

---

## 🔮 Future Improvements

* 🔐 Add authentication (JWT / Token-based)
* 📦 Use Django Models or ODM (like MongoEngine)
* 🧾 Add validation & serializers
* 🌍 Deploy to cloud (Render / AWS / Railway)
* 📊 Add pagination & filtering

---

## 👨‍💻 Author

Developed as a learning project for integrating **Django with MongoDB**.

---

## ⭐ Support

If you like this project, give it a ⭐ and share it!
