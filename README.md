## Overview
This project automates the creation of specific folders within a given directory. The script ensures that the necessary folders (`csv files`, `image files`, and `text files`) are created if they do not already exist.

## How it Works
1. **Folder Creation**:
   - The script iterates through a list of folder names (`csv files`, `image files`, `text files`).
   - For each folder name, the script constructs the full path by joining it with the base file path.
   - It checks if the folder already exists using `os.path.exists()`.
   - If the folder does not exist, it creates the folder using `os.makedirs()` and prints a confirmation message.
   - If the folder already exists, it prints a message indicating that the folder already exists.

2. **Moving Files**:
   - The script iterates through each file in the specified directory, checks its file extension, and moves it to the appropriate folder:
   - **CSV files** are moved to `csv files/` directory.
   - **PNG files** are moved to `image files/` directory.
   - **TXT files** are moved to `text files/` directory.
   - If a file type is not recognized, it is skipped.
