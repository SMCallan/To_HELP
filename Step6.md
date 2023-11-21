### Step 6: Basic Functionality for Searching and Displaying Data

**Objective**: Develop features in your Python program to search for specific departments or employees and display their relevant information from the CSV files.

#### **Instructions**:

1. **Open Your `main.py` File**:
   - Go to the "ELATT_Coursework" folder.
   - Open `main.py` in your text editor.

2. **Implementing Search Functionality**:
   - You'll create functions to search for specific data (like a department or employee name) in the CSV files.

3. **Search and Display Departments**:
   - Write a function to search for a department by name and display its details.
   - Example Function:
     ```python
     def search_department(file_name, department_name):
         found = False
         with open(file_name, mode='r', newline='', encoding='utf-8') as file:
             csv_reader = csv.reader(file)
             for row in csv_reader:
                 if row[0] == department_name:  # Assuming the department name is in the first column
                     print("Department Found:", row)
                     found = True
                     break
         if not found:
             print("Department not found.")
     ```

4. **Search and Display Employees**:
   - Similarly, write a function to search for an employee by an identifier (like an employee ID) and display their details.
   - Example Function:
     ```python
     def search_employee(file_name, employee_id):
         found = False
         with open(file_name, mode='r', newline='', encoding='utf-8') as file:
             csv_reader = csv.reader(file)
             for row in csv_reader:
                 if row[0] == employee_id:  # Assuming the employee ID is in the first column
                     print("Employee Found:", row)
                     found = True
                     break
         if not found:
             print("Employee not found.")
     ```

5. **Integrate Search Functions with Menu**:
   - Modify your `main` function to include options for searching departments and employees.
   - Get the search term (department name or employee ID) from the user using `input()`.
   - Example Integration:
     ```python
     def main():
         while True:
             choice = get_user_choice()
             if choice == "1":
                 department_name = input("Enter department name to search: ")
                 search_department("departments.csv", department_name)
             elif choice == "3":
                 employee_id = input("Enter employee ID to search: ")
                 search_employee("employees.csv", employee_id)
             # Include other menu options
             elif choice == "5":
                 print("Exiting the program.")
                 break
             else:
                 print("Invalid choice, please try again.")
     ```

6. **Test Your Search Features**:
   - Run `main.py` and test the search functionalities by entering different department names and employee IDs.

#### **Tips**:

- **Consistent Data**: Ensure the structure of your CSV files matches the way you're accessing data in your search functions (like which column holds the department name or employee ID).
- **Handling No Results**: Include messages for scenarios where the search term isn't found in the CSV file.

#### **Visual Aid**:
- Screenshots or a video clip demonstrating how to add these search functions and showing them in action when the program runs can greatly assist in understanding.

---

This step focuses on adding search functionality to your Python application, allowing you to query and display specific data from your CSV files. This essential feature enhances the interactivity and practicality of your project, providing foundational skills in data handling and user input processing.
