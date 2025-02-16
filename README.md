# Orders Manager - Docker Setup

This project provides a local development environment for the Orders Manager application, which consists of two main parts:

- **Backend**: A Rails API running with SQLite.
- **Frontend**: A React application serving the UI.

Both the frontend and backend are set up to run in Docker containers, with the necessary configuration to run the app locally using Docker Compose.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Folder Structure

Here is the expected folder structure for this project:
- **`orders_manager-dev/`**: The root directory containing the Docker setup.
  - **`docker-compose.yml`**: The configuration file for Docker Compose, defining how the frontend, backend, and database containers are built and run together.
  - **`orders_manager_api/`**: The backend repository, which is a Rails app.
    - Contains all the necessary Rails code, configuration files, and database files.
  - **`orders-manager/`**: The frontend repository, which is a React app.
    - Contains all the React components, public assets, and the necessary configurations.

## Getting Started

### Clone the Repositories

To get started, clone the necessary repositories:

- [Orders Manager Docker Setup](https://github.com/shayben838/orders_manager_docker)
- [Backend Repository (Rails API)](https://github.com/shayben838/orders_manager_BackEnd)
- [Frontend Repository (React app)](https://github.com/shayben838/orders_manager_FrontEnd)

### Run the Application Locally

1. Navigate to the `orders_manager-dev` directory:
   cd orders_manager-dev

### Run Docker Compose to build and start the containers:
docker-compose up --build

This will build the Docker images for the frontend and backend, set up the database (SQLite), and start the backend on port 3000 and the frontend on port 3001.

### Access the Application
Frontend: Open http://localhost:3001 in your browser to view the React app.
Backend: Open http://localhost:3000 in your browser to access the Rails API.
