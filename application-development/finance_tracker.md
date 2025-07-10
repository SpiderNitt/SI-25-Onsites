# Personal Finance Tracker

## Objective

Build a full-stack personal finance tracker that allows users to securely log in, track their income and expenses, and visualize spending trends using dynamic charts. Users can optionally receive their monthly expense report via email.

## Key Features to Implement

### 1. User Authentication

**Functionality:**  
Ensure that user data is securely protected through authentication.

**Requirements:**
- Register and login endpoints with hashed password storage (e.g., bcrypt).
- JWT or session-based authentication.
- Auth middleware to protect finance-related endpoints.

### 2. Expense & Income Management

**Functionality:**  
Allow users to track financial transactions by date, amount, and category.

**Requirements:**
- `POST /transaction`: Add income or expense with date, amount, category, and description.
- `GET /transactions?month=MM&year=YYYY`: Retrieve filtered transactions.
- `DELETE /transaction/:id`: Delete a specific transaction.
- Categorize by: Food, Rent, Utilities, Salary, etc.

### 3. Monthly Charts & Graphs (Chart.js)

**Functionality:**  
Visualize financial trends using Chart.js in the frontend.

**Requirements:**
- Line chart or bar graph for month-wise expenses.
- Pie chart for category-wise spending distribution.
- Dynamic updates based on date filter.

### 4. Email Monthly Expense Summary (Nodemailer)

**Functionality:**  
Allow users to receive a monthly breakdown of expenses via email.

**Requirements:**
- `POST /email/monthly-summary`: Trigger email with current month’s expense summary.
- Use Nodemailer to format and send a detailed HTML report.
- Option to include chart image or a breakdown table.


