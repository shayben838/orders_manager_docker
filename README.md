# Orders Manager - Application Setup

This project provides a local development environment for the Orders Manager application, which consists of two main parts:

- **Backend**: A Rails API running with SQLite.
- **Frontend**: A React application serving the UI.

Both the frontend and backend are set up to run in Docker containers, with the necessary configuration to run the app locally using Docker Compose.

### Prerequisites

Before you begin, ensure you have the following installed:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

# Getting Started
- `git clone git@github.com:shayben838/orders_manager_docker.git`
- `git clone git@github.com:shayben838/orders_manager_BackEnd.git`
- `git clone git@github.com:shayben838/orders_manager_FrontEnd.git`
- `cd orders_manager_docker`
- `docker-compose up --build`


This will build the Docker images for the frontend and backend, set up the database (SQLite), and start the backend on port 3000 and the frontend on port 3001.

### Access the Application
- Frontend: Open http://localhost:3001 in your browser to view the React app.
- Backend: Open http://localhost:3000 in your browser to access the Rails API.
