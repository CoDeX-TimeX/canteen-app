# 🍔 Gwalia Canteen Web App

A comprehensive, distributed web application designed to digitize the ordering process at Nirma University's Gwalia Canteen. This system replaces paper slips with a real-time, QR-based ordering workflow involving three distinct interfaces: a **Student App**, a **POS/Admin Terminal**, and a **Manager Dashboard**.

![Project Status](https://img.shields.io/badge/Status-Live-success)
![Tech Stack](https://img.shields.io/badge/Tech-Firebase%20%7C%20HTML5%20%7C%20JS-orange)

## 🚀 Features

### 📱 1. Student App (Client Side)
* **Dynamic Menu:** Loads latest items and prices instantly from the Cloud.
* **Smart Cart:** Prevents adding items if stock is low (e.g., "Only 2 left!").
* **QR Code Checkout:** Generates a verified QR code containing the order details.
* **Reference System:** Creates unique, time-stamped Order IDs (e.g., `123045-99`).
* **Dark Mode:** Fully responsive UI with auto-switching dark/light themes.
* **Store Status Check:** Automatically disables ordering when the shop is closed by the manager.

### 📠 2. Admin POS (Cashier Side)
* **QR Scanner:** Built-in camera scanner to read Student QRs instantly.
* **Smart Deduct:** Automatically subtracts inventory from the database upon scanning.
* **Gatekeeper Logic:** Rejects orders if stock has run out in the meantime.
* **Token Generator:** Assigns sequential kitchen tokens (e.g., `Token #101`) for accepted orders.
* **Live History:** View today's revenue and recent order details.

### 💼 3. Manager & Analytics (Back Office)
* **Master Kill Switch:** Open or Close the entire online store with one toggle.
* **Inventory Table:** Edit prices, update stock counts, or mark items "Sold Out" in real-time.
* **CEO Dashboard:** Visual analytics using **Chart.js**:
    * 🔥 **Rush Hour Graph:** See peak ordering times.
    * 🏆 **Best Sellers:** Leaderboard of top-performing items.
    * 💰 **Revenue Meter:** Track monthly income and average order value.
    * ⚠️ **Low Stock Alerts:** Warnings for items running low.

---

## 🛠️ Tech Stack

* **Frontend:** HTML5, CSS3 (Variables & Responsive Grid), Vanilla JavaScript (ES6+).
* **Backend / Database:** Google Firebase Firestore (NoSQL).
* **Libraries:**
    * `html5-qrcode` (For scanning QRs).
    * `Chart.js` (For analytics visualization).
* **Deployment:** GitHub Pages / Netlify (Static Hosting).

---

## 📂 Project Structure

```text
Gwalia_Canteen_App/
│
├── index.html          # Student App (Home/Menu)
├── cart.html           # Shopping Cart & Checkout
├── order.html          # Receipt & QR Code Generation
├── style.css           # Global Styles & Dark Mode
│
├── admin.html          # Cashier POS System
├── Manager.html        # Inventory & Store Controls
├── analytics.html      # Revenue & Data Dashboard
│
├── menu.js             # (Archive) Original menu data
└── upload_menu.html    # Utility tool to upload menu to Firebase