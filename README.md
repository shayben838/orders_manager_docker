![image](https://github.com/user-attachments/assets/6a4ab7b8-1a7c-45b3-89d2-1f7c8e65ed69)
![image](https://github.com/user-attachments/assets/d8aadf11-385a-43ce-8ace-7a96021b2235)




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


## Features

### Table Sorting  
The orders table supports sorting by any column, allowing you to quickly organize the data based on your preferences.

### Table Filtering (by Status)  
You can filter the list of orders by their status, making it easy to view orders in a specific stage (e.g., Pending, Completed).

### Data Pooling  
New orders are automatically updated in the UI in real time.  
- You can create a new order in Window 1, and the list of items will be updated automatically in Window 2.

### Config File  
Each customer can customize their settings through a config file, including:  
- Adjusting the pooling time (frequency of updates)  
- Setting the colors for each order status for better visual distinction

### Versions & Soft Delete  
- Orders are never deleted. Every update to an order is saved and tracked, allowing you to view past versions of an order.  
- Soft delete ensures that when an order is removed, it can still be restored if needed.

### Creating Orders  
- Orders can be created via a user-friendly interface, with all necessary details captured in a simple form.

### Update Order Status  
- The status of an order can be updated at any time, with changes automatically reflected in the system.




