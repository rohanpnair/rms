🍽️ Restaurant Management System (RMS)

A console-based Python application that manages a restaurant's menu using MySQL as a backend database. This system allows users to add, modify, search, delete, and display food items in the menu.

📌 Features

✅ Create Menu Table — Automatically creates the Menu table in the database if it doesn’t exist.

✅ Add New Food Item — Input details like food code, name, availability, type, cost, and offer information.

✅ Modify Item Cost — Update the cost of a food item by its unique food code.

✅ Search Food Item — Search and display details of a food item by its name.

✅ Delete Item — Remove a food item from the menu based on its food code.

✅ Display All Items — Show the complete food menu with all available records.

💾 Tech Stack

Python 3.x

MySQL (with mysql-connector-python library)

📚 Modules Used

mysql.connector

Standard Python libraries: try-except for error handling, input() for user interaction

📌 Project Highlights

Fully menu-driven console application.

Uses SQL commands (CREATE, INSERT, UPDATE, SELECT, DELETE) through Python.

Proper exception handling for database operations.

Menu loop to perform multiple operations continuously.

🎮 How to Run

1.Ensure MySQL server is installed and running.

2.Create a database named RMS in your MySQL environment

3.Install the MySQL connector for Python if not installed

4.Run the python script

📸 Console Menu

Welcome to the RMS or Restaurant management system

Please select your choice from the options:

1. Input food items

2. Modify food item's cost

3. Search food items

4. Delete an item

5. Display table

6. Exit
