Employee Query Assistant
This project is a FastAPI-based Employee Query Assistant that allows users to retrieve employee and department-related data using natural language queries.

How It Works

The app initializes an SQLite database (company.db) with sample employee and department data.
It provides a /query endpoint where users can send a query as a JSON payload.
The app processes the query, extracts relevant keywords, and executes SQL queries.
It returns structured responses based on the query type.
The app also handles invalid inputs, ensuring robustness.
Project Structure

app.py - Main FastAPI application
setup_db.py - Initializes the database (Optional)
requirements.txt - Required dependencies
README.md - Documentation
company.db - SQLite database (auto-created)
Running the Project Locally

Step 1 Install Python and Dependencies

Ensure you have Python 3 installed.
Install the required dependencies by running the command:
pip install fastapi uvicorn sqlite3 pydantic
Step 2 Initialize the Database

Run the following command to set up the SQLite database:
python app.py
This will create company.db and populate it with sample data.
Step 3 Start the FastAPI Server

Run the FastAPI app using Uvicorn:
uvicorn app:app --host 0.0.0.0 --port 8000
The server will start running on http://0.0.0.0:8000
API Usage

Endpoint: POST /query
Request Format: JSON
{ "text": "Who is the manager of the Engineering department?" }
Response Format: JSON
{ "message": "The manager of Engineering is Bob" }