# Bicycle Rental System

This project involves creating a bicycle rental system using a PostgreSQL database and a Bash script to interact with it. The goal is to simulate the operation of a bicycle rental shop, allowing users to rent and return bicycles, manage inventories, and keep records of customers and rentals.

## General Description

The system is composed of three main tables in the database:

- **Bicycles (bikes):** Stores the inventory of available bicycles, including information such as type, size, and availability.
- **Customers (customers):** Records customer information, such as name and phone number.
- **Rentals (rentals):** Keeps track of rented bicycles, including the customer who rented it, the rental date, and the return date.

The Bash script (`bike-shop.sh`) acts as the main interface of the system, allowing users to interact with the database through a menu of options. The main functionalities include:

- **Rent a Bicycle:** Users can select an available bicycle and provide their information to register it as rented.
- **Return a Bicycle:** Users can return a previously rented bicycle, which updates its status in the database.
- **Exit the System:** Users can exit the program at any time.

## Project Structure

### Database

The database is structured into three main tables:

- **bikes:** Contains the bicycles available for rent, with columns such as `bike_id`, `type`, `size`, and `available`.
- **customers:** Stores customer information, with columns such as `customer_id`, `phone`, and `name`.
- **rentals:** Records active rentals, with columns such as `rental_id`, `customer_id`, `bike_id`, `date_rented`, and `date_returned`.

### Bash Script (`bike-shop.sh`)

The Bash script is the core of the system, allowing users to interact with the database through a menu of options. The main functionalities implemented are:

- **Main Menu:** Offers options to rent a bicycle, return a bicycle, or exit the system.
- **Bicycle Rental:** Displays available bicycles, allows the user to select one, and registers the rental in the database.
- **Bicycle Return:** Displays the bicycles rented by a customer, allows the user to select one to return, and updates its status in the database.
- **Validations:** The script includes validations to ensure that user inputs are correct (for example, that the phone number is valid or that the selected bicycle is available).

## Technologies Used

- **PostgreSQL:** For database management.
- **Bash:** For creating the script that interacts with the database.
- **Terminal:** For running the script and interacting with the system.

## How to Run the Project

### Database Setup

1. Connect to PostgreSQL and create a database named `bikes`.
2. Create the `bikes`, `customers`, and `rentals` tables with the necessary columns.
3. Insert some test data into the `bikes` table to simulate the initial inventory.

### Running the Script

1. Ensure that the file `bike-shop.sh` has execution permissions:
   ```bash
   chmod +x bike-shop.sh

2. Run the script from the terminal:
   ```bash
   ./bike-shop.sh
   
3. Follow the on-screen instructions to rent or return bicycles.

## Learnings and Conclusions

This project allowed me to deepen my understanding of relational databases with PostgreSQL, as well as creating Bash scripts to automate tasks and manage user interactions. Additionally, I reinforced concepts such as database normalization, the use of primary and foreign keys, and data manipulation through SQL queries.

This system is a basic yet functional example of how a bicycle rental business can be managed, and it can be expanded in the future with additional features such as payment processing, report generation, or integration with a graphical user interface.

A project done in psql and Bash for freecodecamp.org
