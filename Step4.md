[Back to Main README](README.md)

### Step 4: Implementing the Menu System

**Objective**: Create a simple console menu system in the `main.py` file. This menu will display different options (like searching and displaying departments or employees), and you will use the `input()` function to let the user choose an option.

#### **Instructions**:

1. **Open Your `main.py` File**:
   - Go to the "ELATT_Coursework" folder on your desktop.
   - Double-click `main.py` to open it in your text editor.

2. **Write a Function to Display the Menu**:
   - Define a new function called `show_menu()` that prints the menu options.
   - Here’s an example:
     ```python
     def show_menu():
         print("1. Search Departments")
         print("2. Display Departments")
         print("3. Search Employees")
         print("4. Display Employee Details")
         print("5. Exit")
     ```

3. **Write a Function to Get User Input**:
   - Write another function that calls `show_menu()` and then gets input from the user.
   - Example:
     ```python
     def get_user_choice():
         show_menu()
         choice = input("Enter your choice: ")
         return choice
     ```

4. **Implementing a Loop for the Menu**:
   - Write a loop in your `main` function that keeps showing the menu until the user decides to exit.
   - Example:
     ```python
     def main():
         while True:
             choice = get_user_choice()
             if choice == "5":
                 print("Exiting the program.")
                 break
             else:
                 print("You chose:", choice)
                 # Additional code will go here to handle each choice.

     if __name__ == "__main__":
         main()
     ```

5. **Run and Test Your Menu**:
   - Save the changes in `main.py`.
   - Open a terminal or command prompt, navigate to the "ELATT_Coursework" folder, and run `python main.py`.
   - Test the menu by entering different numbers and seeing if it responds correctly.

#### **Tips**:

- **Validating Input**: Initially, you can keep input validation simple. Later, you may add checks to ensure the user enters a valid option.
- **Function Names**: Use clear and descriptive names for your functions (`show_menu`, `get_user_choice`, etc.) so that their purpose is easily understood.

#### **Visual Aid**:
- Screenshots showing the `main.py` file with the new functions and a sample output in the terminal where the menu is displayed can be very helpful.

---

This step guides you through implementing a basic menu system in your Python project. The menu allows the user to interact with your program by selecting options, which is a fundamental aspect of creating user-friendly console applications. The instructions are designed to be simple, providing a practical example of how to create and use functions in Python.
[Back to Main README](README.md)

