# AIchatbot
A simple AI Chatbot built with Node.js and SQLite. This project includes a backend and a frontend, uses a database to store user information, and provides endpoints for AI-driven chat functionality.

# Features
Database Initialization: Uses SQLite to create necessary tables (e.g., People, Sessions) on startup.

Chat Functionality: Implements a basic AI response mechanism (can be integrated with third-party AI services).

API Endpoints: Provides RESTful API endpoints (using Express or similar) for chat and database operations.

Frontend: Offers a web-based interface to interact with the chatbot in real time.

backend: Contains server-side code, including the Express server and database logic.

frontend: Contains client-side code. Could be a simple HTML/JS page or a framework-based project (React, Vue, etc.).

initDB.js: Automatically runs on server start (or can be run separately) to initialize database tables.

dbHandler.js: Encapsulates CRUD operations for the database.

#Installation
Clone the repository

bash
Copy
git clone <your-repo-url> aichatbot
cd aichatbot
Install dependencies

bash
Copy
npm install
If you have a separate frontend project (e.g., React), navigate into the frontend folder and run:

bash
Copy
cd frontend
npm install
Initialize the database

By default, running the server will automatically execute initDB.js to create any missing tables.

To run the initialization separately (for debugging or manual setup), use:

bash
Copy
cd backend
node initDB.js
Start the backend server

bash
Copy
# From the project root or backend directory
npm run start
Or:

bash
Copy
node backend/app.js
You should see console output indicating that the server is running.

Start the frontend (if applicable)

Navigate to the frontend directory and run:

bash
Copy
npm run serve
or

bash
Copy
npm run start
After the frontend starts, open your browser and visit the provided URL (e.g., http://localhost:3000 or http://localhost:8080).

Access and test

If the backend is running on http://localhost:3001, you can test endpoints like http://localhost:3001/api/people.

The frontend is typically accessible at http://localhost:3000 (or another port) to interact with the chatbot UI.

Environment Variables
Create a .env file in the project root (or backend directory) to manage environment-specific settings, for example:

ini
Copy
PORT=3001
DB_PATH=./database/mydb.sqlite
OPENAI_API_KEY=YOUR_API_KEY
Then reference them in your code via process.env.PORT, process.env.DB_PATH, etc.

# Usage
Chat: In the frontend UI, enter your queries to receive AI-generated responses. The backend can be integrated with services like OpenAI or other NLP libraries for more advanced responses.

Database: You can customize or extend initDB.js to create additional tables (e.g., Sessions, Messages) for storing chat history or user data.

Deployment: Deploy to cloud platforms (AWS, Azure, etc.) or use Docker for containerization. Adjust environment variables and scripts accordingly.

# FAQ
Why is my database not being created?

Ensure you have write permissions in the directory specified by DB_PATH.

Double-check that initDB.js is actually being called on server start.

Port conflicts

If you encounter an “address already in use” error, modify the port in your .env or code.

AI API errors

If you are using a third-party AI service, verify that your API key is correct and that you have a valid subscription or sufficient quota.

Contributing
Contributions are welcome! To get involved:

Submit Issues: If you find bugs or have feature requests, open an issue on GitHub.

Pull Requests: Fork the repository, commit your changes, and submit a pull request to help improve the project.

License
No specific license has been chosen yet. You may add an open-source license such as MIT or Apache 2.0 here if needed.
