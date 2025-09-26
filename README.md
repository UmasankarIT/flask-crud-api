Flask User API

A simple REST API built with Flask for managing user data with CRUD operations (GET, POST, PUT, DELETE).

📌 Project Overview

This project is a basic REST API using Python and Flask. It allows storing, retrieving, updating, and deleting user information.
Data is stored in memory (dictionary) for learning and testing purposes — meaning all data resets when the server restarts.

🛠 Tools Used

Python — Programming language

Flask — Web framework for API creation

VS Code — Code editor

REST Client extension (optional) — To test API requests inside VS Code

cURL/Postman — Alternative tools for testing API

🚀 Features

GET /users — Retrieve all users

GET /users/<id> — Retrieve a specific user by ID

POST /users — Add a new user

PUT /users/<id> — Update an existing user

DELETE /users/<id> — Delete a user

📂 Project Structure
flask-user-api/
│
├── app.py           # Flask application code
├── api_test.http    # REST Client testing file
├── README.md        # Project documentation
└── requirements.txt # Project dependencies

⚙ Installation & Running

Clone the repository

git clone https://github.com/yourusername/flask-user-api.git


Navigate to project folder

cd flask-user-api


Install dependencies

pip install flask


Run the Flask server

python app.py


Server runs at:

http://127.0.0.1:5000

🧪 Testing the API
Using VS Code REST Client

Install the REST Client extension in VS Code.

Open api_test.http.

Click "Send Request" above the request you want to run.

Using cURL

Example commands:

Add User

curl -X POST http://127.0.0.1:5000/users \
-H "Content-Type: application/json" \
-d '{"name":"Alice","email":"alice@example.com"}'


Get All Users

curl http://127.0.0.1:5000/users


Get User by ID

curl http://127.0.0.1:5000/users/1


Update User

curl -X PUT http://127.0.0.1:5000/users/1 \
-H "Content-Type: application/json" \
-d '{"email":"alice_new@example.com"}'


Delete User

curl -X DELETE http://127.0.0.1:5000/users/1

📌 Example Output

GET /users

{
  "1": {
    "name": "Alice",
    "email": "alice@example.com"
  }
}

📚 Learnings

This project helps you understand:

Creating REST APIs with Flask
CRUD operations
Testing APIs with REST Client and cURL
Basic API structure and routing
