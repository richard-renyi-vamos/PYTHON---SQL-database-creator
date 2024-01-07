User
create a python script that lets you create a SQL database 
ChatGPT
Sure, creating a basic SQLite database using Python can be quite straightforward. You'll need to use the sqlite3 module which comes built-in with Python. Here's a simple example of how you can create a SQLite database:

python
Copy code
import sqlite3

# Connect to or create a new database file
conn = sqlite3.connect('example.db')

# Create a cursor object to execute SQL commands
cursor = conn.cursor()

# Create a table in the database
cursor.execute('''CREATE TABLE IF NOT EXISTS Users (
                    id INTEGER PRIMARY KEY,
                    name TEXT NOT NULL,
                    email TEXT NOT NULL UNIQUE
                )''')

# Commit changes and close the connection
conn.commit()
conn.close()
This script does the following:

Imports the sqlite3 module.
Establishes a connection to a SQLite database file named 'example.db'.
Creates a cursor object to execute SQL commands.
Executes a SQL command to create a table called 'Users' with columns for 'id', 'name', and 'email'.
You can modify the SQL CREATE TABLE command and add more columns or different data types according to your needs.

Remember, this is a basic example. In a real-world scenario, you might want error handling and more complex database designs.
