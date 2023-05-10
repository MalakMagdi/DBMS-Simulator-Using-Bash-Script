
# MySQL Database Simulator (Bash Project)

This Bash project simulates the functionality of a MySQL database. It provides a set of scripts to perform various operations on the database. The project is organized under a directory called `MySQL`, with a main script named `main.sh`. When the user runs the script, the screen will be cleared, and a menu will be displayed with options numbered from 1 to 7. Each option corresponds to a specific script for a particular operation.

## Project Structure

The project follows the following structure:

```
MySQL/
├── main.sh
├── DB_admins.db
└── DataBases/
    ├── YOUR_NEW_DB/
    │   ├── owner.txt
    │   └── ...
    └── ...
```

- `main.sh`: The main script that serves as the entry point to the database simulator.
- `DB_admins.db`: A file that stores a list of admin users, including the default system user called "oracle".
- `DataBases/`: A directory that contains the created databases.
- `YOUR_NEW_DB/`: A directory representing a created database. The name of the directory will correspond to the entered database name.
- `owner.txt`: A file inside each database directory that stores the username of the user who created the database.


## Operation Descriptions

1. **Create Database User**

   - By default, a system user called "oracle" exists.
   - If the user running the script is "oracle" or an admin user, the script will prompt for a new admin user.
   - If the entered user already exists, a message will appear indicating that the user already exists.
   - If not, the entered user will be added to the `DB_admins.db` file, which stores a list of admin users.

2. **Delete Database User**

   - Only users listed in the `DB_admins.db` file can run this script.
   - The script will display the list of users from the `DB_admins.db` file.
   - If a user is selected, it will be deleted from the `DB_admins.db` file.
   - The "oracle" user cannot be deleted.

3. **Create New Database**

   - Only users listed in the `DB_admins.db` file can run this script.
   - The script will prompt for the database name.
   - A directory with the entered database name will be created under `MySQL/DataBases/`.
   - An `owner.txt` file will be created in the database directory, containing the username of the user who created the database.

4. **Delete an Existing Database**

   - Only users listed in the `DB_admins.db` file can run this script.
   - The script will display all available created databases inside `MySQL/DataBases`.
   - If the database owner is the same as the user running the script, the database directory and its contents will be deleted.

5. **Create a New Table inside Database**

   - Only users listed in the `DB_admins.db` file can run this script.
   - The script will display all available created databases inside `MySQL/DataBases`.
   - If the database owner is the same as the user running the script, it will prompt for the table name and the number of columns to be created.
   - If the table name does not already exist in this database, it will prompt for
