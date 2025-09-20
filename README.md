# Performance Management System

This repository contains a full-stack application designed for a **Performance Management System**. The system allows managers and employees to collaboratively set goals, track progress, provide feedback, and view performance history.

The application is built with Python, using Streamlit for the front end and PostgreSQL as the database. It adheres to the **CRUD (Create, Read, Update, Delete)** principles for managing data and provides valuable business insights.

---

## 🚀 Features

* **Goal and Task Setting**: Managers can create, assign, and manage individual goals for employees. Employees can view their assigned goals and log tasks to achieve them.
* **Progress Tracking**: Both managers and employees can view real-time progress. Managers have the exclusive ability to update a goal's status.
* **Feedback**: A dedicated section allows managers to provide detailed written feedback on an employee's performance, which is linked to specific goals.
* **Reporting**: The system provides a comprehensive history of an employee's past and present goals, along with all associated feedback.
* **Business Insights**: The dashboard includes an insights section with key performance metrics, such as total goals, average completion time, and top performers, using SQL aggregation functions.

---

## ⚙️ Technology Stack

* **Frontend**: Streamlit
* **Backend**: Python
* **Database**: PostgreSQL
* **Libraries**: `psycopg2`, `pandas`

---

## 💻 Getting Started

Follow these steps to set up and run the application on your local machine.

### Prerequisites

* **Python 3.8+**
* **PostgreSQL** (with a running instance and a user that can create databases/tables)

### Installation

1.  Clone this repository to your local machine:
    ```bash
    git clone <repository_url>
    cd <repository_folder>
    ```

2.  Create a virtual environment and activate it:
    ```bash
    python -m venv venv
    source venv/bin/activate # On Windows, use `venv\Scripts\activate`
    ```

3.  Install the required Python packages:
    ```bash
    pip install -r requirements.txt
    ```
    If you don't have a `requirements.txt` file, you can create one with the following content:
    ```
    streamlit
    psycopg2-binary
    pandas
    ```

### Database Setup

1.  Connect to your PostgreSQL database using a client like `psql` or pgAdmin.
2.  Create a new database for the application (e.g., `performance_db`).
3.  Run the commands from the `sql_schema.sql` file to create the necessary tables and populate them with initial data.
    ```sql
    -- Example using psql
    \c performance_db
    \i sql_schema.sql
    ```

4.  Set up your database connection details as environment variables. The application uses these to connect to the database.
    * `DB_HOST`
    * `DB_NAME`
    * `DB_USER`
    * `DB_PASSWORD`

    Example on Linux/macOS:
    ```bash
    export DB_HOST='localhost'
    export DB_NAME='performance_db'
    export DB_USER='your_username'
    export DB_PASSWORD='your_password'
    ```

### Running the Application

Once the database is set up and environment variables are configured, you can launch the application by running the Streamlit command on your `Frontend_fin.py` file:

```bash
streamlit run Frontend_fin.py
