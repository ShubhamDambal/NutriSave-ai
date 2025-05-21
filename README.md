# 🍱 Smart Food Waste Management System

A full-stack web platform designed to reduce food waste by intelligently matching surplus food sources with NGOs, food banks, and individuals. It combines real-time data dashboards, predictive ML modeling, and blockchain transparency to ensure sustainable and efficient food redistribution.

---

## ⚙️ How It Works

1. **Food Donors (Restaurants, Events, Households)** register and upload surplus food details (type, quantity, cooking time, etc.).
2. A **Machine Learning model** predicts the expiry of food based on parameters like:
   - Food Type (vegetarian, non-vegetarian, dairy, etc.)
   - Cooking Time (in minutes)
   - Storage Temperature (°C)
   - Humidity (%)
   - Quantity (grams/kgs)
3. Based on expiry predictions, the system prioritizes food redistribution to ensure **safe consumption before spoilage**.
4. NGOs and food banks view available food in **real-time on an interactive map** powered by Leaflet.js and can accept/reject donations.
5. All redistribution transactions are logged via **blockchain** for traceability and trust.
6. Users are notified of collection/delivery, and donors can track their impact over time.

---

## 🚀 Key Features

- ♻️ **Surplus Matching Engine** – Matches food donors with NGOs based on location and food type.
- 📊 **Live Dashboard** – Displays real-time food availability on maps with status updates.
- 🧠 **Expiry Prediction** – ML model forecasts spoilage based on food characteristics.
- 🔐 **User Authentication** – Secure login/registration system with Express.js.
- 🌐 **Blockchain Transparency** – Ensures traceable, tamper-proof redistribution.
- 📦 **Inventory Trends** – Helps users optimize food procurement and reduce excess.

---

## 🛠️ Tech Stack

### 💻 Frontend
- React.js (with Vite)
- Leaflet.js (for interactive maps)
- Tailwind CSS / Custom CSS for styling

### ⚙️ Backend
- Node.js
- Express.js
- MongoDB Atlas (cloud database)

### 🤖 Machine Learning
- Python
- Flask (as a REST API server)
- Pandas, NumPy, Scikit-learn

---

## 🔬 ML Model: Expiry Prediction

**Goal:** Estimate the shelf life of donated food to enable timely redistribution.

**Features Used:**
- `foodType`
- `cookingTime` (in minutes)
- `storageTemp` (°C)
- `humidity` (%)
- `quantity` (g/kg)

**Output:**  
- Predicted expiry time (in hours)
- Categorization: Safe / Soon to Expire / Expired

The model is trained using historical food spoilage data and is served through a Flask API to the main web platform.

---

## 👤 Roles & Contributions

- **Frontend Developer** – Built responsive user interface in React, integrated Leaflet for map visualization, and connected the frontend to the backend APIs and ML model.
- **Team Members** – Focused on backend logic, ML model development, database design, and blockchain integration.

---

## 🔐 Authentication

- JWT-based login and registration system
- Role-based access for donors, NGOs, and admins

---

## 🚀 Local Setup Instructions

```bash
# Clone the repository
git clone https://github.com/yourusername/food-waste-management.git
cd food-waste-management

# Frontend Setup
cd client
npm install
npm run dev

# Backend Setup
cd ../server
npm install
npm start

# ML Model Setup (optional)
cd ../ml-model
pip install -r requirements.txt
python app.py
