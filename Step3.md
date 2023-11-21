[Back to Main README](README.md)

### Step 3: Basic File Operations - CSV File Handling

**Objective**: Learn and implement basic operations to read from and write to CSV (Comma-Separated Values) files using Python's built-in `csv` module. CSV files are simple text files used for storing tabular data.

#### **Instructions**:

1. **Understand CSV Files**:
   - A CSV file stores data in a simple text format where each line represents a row of data, and each value in the row is separated by a comma.
   - Example: `Name, Age, Country` is a header, and `Alex, 30, UK` is a data row.

2. **Open Your `main.py` File**:
   - Go to the "ELATT_Coursework" folder.
   - Double-click on `main.py` to open it in your text editor.

3. **Import the CSV Module**:
   - At the top of `main.py`, write `import csv`. This tells Python to use the CSV module, which has functions to handle CSV files.

4. **Writing Code to Read a CSV File**:
   - Below the import statement, write a function to read a CSV file.
   - Example function:
     ```python
     def read_csv_file(filename):
         with open(filename, mode='r', newline='', encoding='utf-8') as file:
             csv_reader = csv.reader(file)
             for row in csv_reader:
                 print(row)
     ```
   - This function opens a CSV file, reads each row, and prints it.

5. **Writing Code to Write to a CSV File**:
   - Write another function to write data to a CSV file.
   - Example function:
     ```python
     def write_csv_file(filename, data):
         with open(filename, mode='w', newline='', encoding='utf-8') as file:
             csv_writer = csv.writer(file)
             for row in data:
                 csv_writer.writerow(row)
     ```
   - This function writes each row of data to a CSV file.

6. **Testing the Functions**:
   - To test, first create a sample CSV file named `test.csv` with some data.
   - Call your `read_csv_file` and `write_csv_file` functions in `main.py` with `test.csv` as an argument.

7. **Run Your Code**:
   - Save `main.py`.
   - Open a command prompt or terminal, navigate to your "ELATT_Coursework" folder, and run `python main.py`.
   - Check if your code reads and writes to the CSV file correctly.

#### **Tips**:

- **Path to CSV File**: When specifying the filename in your functions, provide the correct path. If the CSV file is in the same folder as `main.py`, just the file name is enough.
- **Handling Errors**: You may encounter errors if the file doesn't exist or the path is wrong. Ensure the file is in the correct location and the file name is spelled correctly.

#### **Visual Aid**:
- Screenshots or a short video showing writing these functions in `main.py` and running them can be very helpful.

---

This step introduces basic file operations with a focus on CSV files. The instructions are designed to be simple and clear, guiding you through writing basic functions to read and write CSV files, an essential skill for handling data in many Python projects.
[Back to Main README](README.md)
