[Back to Main README](README.md)
### Step 7: Error Handling

**Objective**: Implement basic error checks in your Python program to handle common issues such as invalid menu options and problems encountered while reading or writing files.

#### **Instructions**:

1. **Open Your `main.py` File**:
   - Navigate to the "ELATT_Coursework" folder.
   - Open `main.py` in your text editor.

2. **Handling Invalid Menu Options**:
   - Modify the `get_user_choice` function to validate the user's input.
   - Example:
     ```python
     def get_user_choice():
         show_menu()
         choice = input("Enter your choice: ")
         if choice not in ["1", "2", "3", "4", "5"]:
             print("Invalid choice, please try again.")
             return None
         return choice
     ```
   - In the `main` function, check if `choice` is `None` and continue to the next iteration if it is.

3. **Handling File-Related Errors**:
   - Use `try-except` blocks to catch exceptions when dealing with file operations.

   **Example for Reading Files**:
   ```python
   def read_csv_file(filename):
       try:
           with open(filename, mode='r', newline='', encoding='utf-8') as file:
               csv_reader = csv.reader(file)
               for row in csv_reader:
                   print(row)
       except FileNotFoundError:
           print(f"File {filename} not found.")
       except Exception as e:
           print(f"An error occurred: {e}")
   ```

   **Example for Writing Files**:
   ```python
   def write_csv_file(filename, data):
       try:
           with open(filename, mode='w', newline='', encoding='utf-8') as file:
               csv_writer = csv.writer(file)
               for row in data:
                   csv_writer.writerow(row)
       except IOError:
           print(f"Could not write to file {filename}.")
       except Exception as e:
           print(f"An error occurred: {e}")
   ```

4. **Testing Error Handling**:
   - Test your program with scenarios that could cause errors, like entering an invalid option or using a non-existent file name.
   - Ensure that your program handles these errors gracefully and provides a clear message to the user.

#### **Tips**:

- **Specific Exceptions**: Catch specific exceptions (like `FileNotFoundError` or `IOError`) to handle known error types effectively.
- **General Exception Handling**: Use a general `except Exception as e` to catch any unexpected errors and prevent your program from crashing.
- **User Guidance**: Provide clear and helpful error messages to guide the user on what went wrong and possibly how to correct it.

#### **Visual Aid**:
- Screenshots or a video showing the implementation of error handling in the code and examples of how the program behaves when an error occurs can be very instructive.

---

In this step, you're adding basic error handling to make your program more robust and user-friendly. This is a critical aspect of programming, ensuring that your application can gracefully handle unexpected situations and provide useful feedback to the user. The instructions are designed to introduce you to common error-handling patterns in Python.
[Back to Main README](README.md)
