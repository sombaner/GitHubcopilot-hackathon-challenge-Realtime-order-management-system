# 🚀 GitHub Copilot Vibe Coding Hackathon: Order Management System

## 🧠 Scenario

You’re part of a startup building a **real-time Order Management Dashboard** for a food-delivery platform.

---

## 🎯 Problem Statement

### ✅ Objective

Build a responsive front-end application that:

- Displays and manages orders in real-time.
- Includes business logic for:
  - Filtering (by status and date)
  - Sorting (e.g., by date, amount)
  - Order status transitions (Pending → In Progress → Delivered)

---

### 📦 Features to Implement

1. **Order List View**
   - Paginated list of orders with:
     - Order ID
     - Customer Name
     - Items
     - Total Amount
     - Status (Pending, In Progress, Delivered)

2. **Order Detail Panel**
   - Display full order details.
   - Enable status update.

3. **Filters & Search**
   - Filter by order status and date.
   - Search by customer name and item name.

4. **Dashboard Metrics**
   - Summary cards for:
     - Total orders
     - Pending orders
     - Average delivery time (use dummy data)

---

## 🔢 Data

- Use a mocked REST API or in-memory JSON dataset with **50+ realistic orders**.

---

## 🛠️ Deliverables

- UI code
- Mock data source
- Business-logic modules

### 🎯 Focus On

- Clean component structure
- State management (e.g., Redux, Context, RxJS)
- Styling consistency (e.g., Tailwind CSS, CSS-in-JS)

---

## 🧪 Evaluation Criteria

- UX intuition and responsiveness
- Code modularity and organization
- Use of GitHub Copilot for faster development
- Edge case handling and error management
- Unit test coverage and CI pipeline
- Documentation (inline and project-level)
- Working and deployable application

---

## 📊 Data Model & Mock Data

### 📐 Entities & Attributes

- **Customer**:
  - `customerId` (UUID)
  - `name` (string)
  - `email` (string)
  - `address` (string)

- **Product**:
  - `productId` (UUID)
  - `name` (string)
  - `description` (string)
  - `price` (number)

- **Order**:
  - `orderId` (UUID)
  - `customerId` (FK)
  - `status` (enum: Pending | InProgress | Delivered)
  - `orderDate` (ISO datetime)
  - `deliveryTime` (int, minutes)

- **OrderItem**:
  - `orderItemId` (UUID)
  - `orderId` (FK)
  - `productId` (FK)
  - `quantity` (int)
  - `itemTotal` (number)

### 🧾 Sample JSON

```json
{
  "customers": [
    { "customerId": "c1", "name": "Alice", "email": "alice@example.com", "address": "123 Maple St" },
    { "customerId": "c2", "name": "Bob",   "email": "bob@example.com",   "address": "456 Oak Ave" }
  ],
  "products": [
    { "productId": "p1", "name": "Burger",  "description": "Beef burger",  "price": 5.99 },
    { "productId": "p2", "name": "Fries",   "description": "French fries",  "price": 2.49 }
  ],
  "orders": [
    {
      "orderId": "o1",
      "customerId": "c1",
      "status": "Pending",
      "orderDate": "2025-07-03T10:00:00Z",
      "deliveryTime": 30,
      "items": [
        { "orderItemId": "oi1", "productId": "p1", "quantity": 2, "itemTotal": 11.98 },
        { "orderItemId": "oi2", "productId": "p2", "quantity": 1, "itemTotal": 2.49 }
      ]
    }
  ]
}
```

> ⚠️ Please expand this dataset with 50+ orders during implementation.

---

## 💡 Developer Instructions

Use GitHub Copilot to:

- Parse ER/class diagrams into code models
- Scaffold REST/in-memory data services
- Generate UI components: list, detail view, filters, and metrics
- Implement state management and logic
- Write unit tests
- **Participants are free to choose any programming language**

---

## 📤 Submission

Each team must submit:

- GitHub repo with the source code
- A complete README with setup instructions

---

## 🎉 Happy Hacking with GitHub Copilot!
