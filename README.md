# Multi-Container Flask Application with Redis

This project demonstrates a simple multi-container application using Flask and Redis. The application tracks the number of visits to a web page and displays the count dynamically.

## Project Structure
├── docker-compose.yml # Docker Compose configuration ├── web/ │ ├── app.py # Flask application code │ ├── Dockerfile # Dockerfile for the Flask app │ ├── requirements.txt # Python dependencies │ └── templates/ │ └── index.html # HTML template for the web page

## Features

- **Flask**: A lightweight Python web framework for building the web application.
- **Redis**: An in-memory data store used to track the number of visits.
- **Docker Compose**: Orchestrates the multi-container setup for the Flask app and Redis.

## Prerequisites

- [Docker](https://www.docker.com/) installed on your system.
- [Docker Compose](https://docs.docker.com/compose/) installed.

## Getting Started

1. Clone this repository to your local machine:
   ```bash
   git clone <repository-url>
   cd my-multi-container-app

2.Build and start the containers using Docker Compose:
   ```bash
   docker-compose up --build
   ```
3. Open your web browser and navigate to `http://localhost:5000` to see the application in action.
4. Refresh the page to see the visit count increase.

📁Project Components
Flask Application
The Flask app is defined in web/app.py. It includes:

A route (/) that increments the visit count in Redis and renders the index.html template.
The app runs on port 5000 by default.
Redis
The Redis service is defined in the docker-compose.yml file and uses the lightweight redis:alpine image.

Docker Compose
The docker-compose.yml file orchestrates the services:

Web: Builds the Flask app from the web directory and maps port 5000 on the host to port 5000 in the container.
Redis: Uses the official Redis image.
HTML Template
The HTML template web/templates/index.html displays the visit count dynamically using Flask's template rendering.

File Descriptions
docker-compose.yml: Defines the services and their configurations.
web/Dockerfile: Specifies the steps to build the Docker image for the Flask app.
web/requirements.txt: Lists the Python dependencies (flask and redis).
web/app.py: Contains the Flask application code.
web/templates/index.html: The HTML template for the web page.

Stopping the Application 🛑
To stop the application, press Ctrl+C in the terminal where docker-compose up is running. Alternatively, you can stop the containers with:
"docker-compose down"

License
This project is licensed under the MIT License. See the LICENSE file for details.

Acknowledgments
Flask
Redis
Docker

This `README.md` provides an overview of the project, instructions for setup, and details about its components.

