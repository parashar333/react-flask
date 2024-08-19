# React-Flask Application
Live Demo
You can view a live demo of the application at: https://react-flask-article-54a5a7525137.herokuapp.com/

## Overview

This project is a simple Article Management System built with React on the frontend, Flask on the backend, and MySQL as the database. It allows users to create, read, update, and delete articles through a RESTful API and a React frontend interface.

## Features

- **Frontend:** Built with React, serves a user interface to interact with the API.
- **Backend:** Built with Flask, provides a RESTful API to manage articles.
- **Database:** MySQL, stores article data and is managed via SQLAlchemy.
- **Deployment:** Containerized with Docker and deployed to Heroku.

## Tech Stack

- **Frontend:** React, Node.js, npm
- **Backend:** Flask, Python, SQLAlchemy
- **Database:** MySQL
- **Containerization:** Docker
- **Deployment:** Heroku

## Getting Started

To get a local copy of the project up and running, follow these steps:

### Prerequisites

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [Node.js](https://nodejs.org/) (for building the frontend)
- [Python 3](https://www.python.org/downloads/) (for running the backend)

### Clone the Repository

```bash
git clone https://github.com/yourusername/react-flask-article.git
cd react-flask-article

Build and Run Containers
Ensure Docker and Docker Compose are installed. From the project root directory, use Docker Compose to build and run the containers.
docker-compose up --build

This command will build and start the frontend, backend, and MySQL containers. The frontend will be available at http://localhost:3000, and the backend at http://localhost:5000.

Frontend
The frontend is built with React. The Dockerfile in the frontend directory sets up the Node.js environment, installs dependencies, builds the React app, and serves it using a static server.

Backend
The backend is built with Flask. The Dockerfile in the backend directory sets up the Python environment, installs dependencies, and runs the Flask application.

Database
The MySQL database is configured with a Docker container. It initializes with a default database named react-flask and uses the password password.

Usage
GET /get: Retrieve all articles.
GET /get/<id>: Retrieve a specific article by ID.
POST /add: Add a new article. Requires JSON body with title and body.
PUT /update/<id>: Update an existing article. Requires JSON body with title and body.
DELETE /delete/<id>: Delete an article by ID.

License
This project is licensed under the MIT License.
