# Personal Finance Tracker

## What do you want to build?

Build a web-based personal finance tracker in Python using Flask that allows users to record income and expenses, categorize transactions, set monthly budgets, visualize spending patterns with charts, and import transactions from CSV files. The application should include user authentication, a SQLite database for persistence, and interactive dashboards showing spending trends over time.

The implementation must include:
- Flask web application with user authentication (signup, login, session management)
- Transaction management: create, edit, delete, categorize (income/expense with subcategories)
- Budget setting: define monthly limits per category with alerts when approaching or exceeding
- CSV import/export: support common bank statement formats with column mapping
- Interactive charts: spending by category (pie chart), spending over time (line chart), budget vs actual (bar chart)
- Search and filtering: by date range, category, amount, or description
- SQLite database with proper schema design and migrations
- Responsive UI that works on desktop and mobile

## How do you consider the project is success?

1. Users can sign up, log in, and manage their own transactions with proper session isolation
2. Transaction CRUD operations work correctly with categorization and validation (required fields, numeric amounts)
3. Budget tracking correctly calculates spending per category per month and shows percentage used
4. CSV import successfully parses at least 3 different bank statement formats with configurable column mapping
5. Charts render correctly using JavaScript (Chart.js or similar) and update dynamically when filters change
6. Search and date range filtering return accurate results within 100ms for datasets with 10,000+ transactions
7. Test suite with at least 20 tests covering authentication, transaction logic, budget calculations, and CSV parsing
8. Deployed with proper database schema migrations and a seed data script for demonstration
