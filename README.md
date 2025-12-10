# Smart Expense & Budget Tracker

A lightweight Flask-based web application that helps users track daily expenses, categorize them, set monthly budgets, receive alerts when exceeding budgets, and view category-wise spending analytics.

## Features

✨ **Key Features:**
- Add and manage daily expenses with categories
- Set budget limits for different expense categories
- Automatic budget alerts when spending exceeds limits
- Category-wise expense analytics and reports
- Simple and intuitive user interface
- SQLite database for data persistence

## Tech Stack

- **Backend:** Python, Flask
- **Database:** SQLite
- **Frontend:** HTML, CSS, Jinja2 Templates
- **Server:** Flask Development Server

## Project Structure

```
smart_expense_tracker/
│── app.py                  # Main Flask application
│── database.py             # Database initialization and setup
│── static/
│   └── style.css           # CSS styling
│── templates/
│   ├── index.html          # Dashboard/home page
│   ├── add_expense.html    # Add expense form
│   ├── set_budget.html     # Set budget form
│   └── report.html         # Category-wise report
├── README.md               # Project documentation
└── requirements.txt        # Python dependencies
```

## Installation

### Prerequisites
- Python 3.7 or higher
- pip (Python package manager)

### Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/whynotprajwal/smart-expense-budget-tracker.git
   cd smart_expense_tracker
   ```

2. **Create a virtual environment (optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install flask
   ```

4. **Run the application:**
   ```bash
   python app.py
   ```

5. **Open in browser:**
   Navigate to `http://localhost:5000` in your web browser

## Usage

### Dashboard (`/`)
- View all recent expenses
- See current budget status
- Quick navigation to other features

### Add Expense (`/add`)
- Enter expense amount
- Select category
- Add optional notes
- Set the date of expense

### Set Budget (`/budget`)
- Define budget limits for different categories
- Update existing budgets

### View Report (`/report`)
- Category-wise spending summary
- Compare spending against budgets
- Identify spending patterns

## Database Schema

### Expenses Table
```sql
CREATE TABLE expenses (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    amount REAL NOT NULL,
    category TEXT NOT NULL,
    note TEXT,
    date TEXT NOT NULL
)
```

### Budget Table
```sql
CREATE TABLE budget (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    category TEXT UNIQUE,
    limit_amount REAL NOT NULL
)
```

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | View dashboard with all expenses |
| GET, POST | `/add` | Add new expense |
| GET, POST | `/budget` | Set or update budget |
| GET | `/report` | View category-wise report |

## Future Enhancements

- User authentication and login system
- Data visualization with charts and graphs
- Export expenses to CSV/Excel
- Monthly and yearly reports
- Budget forecast and predictions
- Mobile responsive design
- Multiple user profiles
- Data backup and recovery

## Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for bugs and feature requests.

## License

This project is open source and available under the MIT License.

## Author

Created as a Python course project by Prajwal Parve

## Support

For questions or issues, please open an issue on the GitHub repository.
