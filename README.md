# Assessment Project

## Overview
This project is a full-stack application developed using the MERN (MongoDB, Express.js, React.js, Node.js) stack. It handles transaction data from a third-party API and provides various functionalities such as listing transactions, generating statistics, and displaying them in a user-friendly web interface.

## Table of Contents
- [Backend](#backend)
- [API Endpoints](#api-endpoints)
  - [Initialization API](#initialization-api)
  - [List Products API](#list-products-api)
  - [Statistics API](#statistics-api)
  - [Bar Chart API](#bar-chart-api)
  - [Pie Chart API](#pie-chart-api)
  - [Combined API](#combined-api)
- [Frontend](#frontend)
  - [Transactions Table](#transactions-table)
  - [Transactions Statistics](#transactions-statistics)
  - [Transactions Bar Chart](#transactions-bar-chart)
- [Installation and Setup](#installation-and-setup)
- [Technologies Used](#technologies-used)
- [License](#license)

## Backend

### API Endpoints

#### Initialization API
- **Endpoint:** `/api/v1/product/initialize-seed-data`  
- **Method:** GET  
- **Description:** Initializes the database by fetching data from a third-party API and seeding the database with the obtained data.  
- **Third-party API URL:** [Product Transaction Data](https://s3.amazonaws.com/roxiler.com/product_transaction.json)

#### List Products API
- **Endpoint:** `/api/v1/product`  
- **Method:** GET  
- **Parameters:**  
  - `month` (string): The month for which transactions need to be fetched.  
  - `page` (integer, optional): Page number for pagination (default: 1).  
  - `perPage` (integer, optional): Number of items per page for pagination (default: 10).  
  - `search` (string, optional): Search text to filter transactions based on title/description/price.

#### Statistics API
- **Endpoint:** `/api/v1/analytics/statistics`  
- **Method:** GET  
- **Parameters:**  
  - `month` (string): The month for which statistics need to be fetched.

#### Bar Chart API
- **Endpoint:** `/api/v1/analytics/bar-chart`  
- **Method:** GET  
- **Parameters:**  
  - `month` (string): The month for which bar chart data needs to be fetched.

#### Pie Chart API
- **Endpoint:** `/api/v1/analytics/pie-chart`  
- **Method:** GET  
- **Parameters:**  
  - `month` (string): The month for which pie chart data needs to be fetched.

#### Combined API
- **Endpoint:** `/api/v1/analytics/combined-chart`  
- **Method:** GET  
- **Description:** Fetches data from all the above APIs, combines the response, and sends a final JSON response.

## Frontend

### Transactions Table
- Displays a table of transactions with:
  - Month selection dropdown (Jan to Dec) to filter transactions by month.
  - Default selection: March.
  - Search box to filter transactions based on title/description/price.
  - Pagination with Next and Previous buttons.

### Transactions Statistics
- Displays:
  - Total amount of sale
  - Total sold items
  - Total not sold items for the selected month.

### Transactions Bar Chart
- Displays a bar chart showing the price range and the number of items in each range for the selected month.

## Installation and Setup
1. **Clone the repository:**
   ```bash
   git clone https://github.com/Suraj051198/assessment-project.git
   cd assessment-project

## cd backend
npm install
npm start

## cd frontend
npm install
npm run dev

 4. **Access the Application:**
    Backend: http://localhost:5000
    Frontend: http://localhost:3000

## Technologies Used

    MongoDB: NoSQL database
    Express.js: Backend framework
    React.js: Frontend library
    Node.js: Runtime environment

## License

This project is licensed under the MIT License.


### Step 1: Create and Edit the README.md File
1. In your project directory, create a new file named `README.md` if you haven't already.
2. Copy and paste the content above into the `README.md` file.
3. Save the file.

### Step 2: Add and Push the README to GitHub
Run the following commands in your terminal to add and push the `README.md` file:

```bash
# Add the README file
git add README.md

# Commit the changes
git commit -m "Added README documentation"

# Push to GitHub
git push origin main


