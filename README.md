![image](https://github.com/user-attachments/assets/6a4ab7b8-1a7c-45b3-89d2-1f7c8e65ed69)




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
- `git clone https://github.com/shayben838/orders_manager_docker.git`
- `git clone https://github.com/shayben838/orders_manager_BackEnd.git`
- `git clone https://github.com/shayben838/orders_manager_FrontEnd.git`
- `cd orders_manager_docker`
- `docker-compose up --build`


This will build the Docker images for the frontend and backend, set up the database (SQLite), and start the backend on port 3000 and the frontend on port 3001.

### Access the Application
- Frontend: Open http://localhost:3001 in your browser to view the React app.
- Backend: Open http://localhost:3000 in your browser to access the Rails API.


## Docker Setup  
The Docker setup has been tested on macOS. If you're using Windows, you may need to make some adjustments.  

### Running the Application Without Docker  

#### Backend (Rails)  
*Note: If you're on Windows, you may need to install Ruby first.*  

Run the following commands:  

- **Install dependencies:**  
  bundle install

- **Set up the database schema::**  
  rails db:migrate

- **Seed the database with sample data (300 orders):**  
  rails db:seed

- **Start the server:**  
  rails s

#### Frontend (React)
Run the following commands:  

- **Install dependencies:**  
  npm install

- **Start the development server:**  
  npm start

