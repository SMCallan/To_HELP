### Step 5: CRUD Operations for Departments and Employees

**Objective**: Write functions for creating, reading, updating, and deleting (CRUD) information about departments and employees in CSV files. These functions will be integrated with the menu system in your `main.py` file.

#### **Instructions**:

1. **Understand CRUD Operations**:
   - **Create**: Add new data.
   - **Read**: Display existing data.
   - **Update**: Change existing data.
   - **Delete**: Remove existing data.

2. **Open Your `main.py` File**:
   - Go to the "ELATT_Coursework" folder.
   - Open `main.py` in your text editor.

3. **Define CRUD Functions**:
   - Write separate functions for each CRUD operation. Below are simplified examples for departments. You can create similar ones for employees.

   **Read Function Example**:
   ```python
   def read_departments(file_name):
       with open(file_name, mode='r', newline='', encoding='utf-8') as file:
           csv_reader = csv.reader(file)
           for row in csv_reader:
               print(row)
   ```

   **Create, Update, Delete**:
   - For create, update, and delete operations, consider how you want to structure your data and how these operations will interact with the CSV file.

4. **Integrate CRUD Functions with Menu**:
   - Modify your `main` function to call these CRUD functions based on the user's menu selection.
   - Example Integration:
     ```python
     def main():
         while True:
             choice = get_user_choice()
             if choice == "1":
                 read_departments("departments.csv")
             # Add more conditions for other choices
             elif choice == "5":
                 print("Exiting the program.")
                 break
             else:
                 print("Invalid choice, please try again.")
     ```

5. **Create Sample CSV Files**:
   - Create sample CSV files like `departments.csv` and `employees.csv` with some dummy data for testing.

6. **Test the CRUD Operations**:
   - Run `main.py` and test each menu option to see if the corresponding CRUD operation works as expected.

#### **Tips**:

- **File Paths**: Ensure the file paths in your CRUD functions match the location of your CSV files.
- **Error Handling**: Include basic error handling, like checking if the file exists before trying to read it.
- **Simplicity**: Keep the functions straightforward. Complex logic can be introduced later as you gain more experience.

#### **Visual Aid**:
- Screenshots or short clips showing the process of writing these functions, creating the CSV files, and the output when running different menu options can be helpful.

---

This step introduces you to CRUD operations, a fundamental concept in managing data in applications. The instructions aim to guide you through writing basic functions to interact with CSV files and integrating these functions into your menu system, providing a hands-on experience in building a functional Python application.
