# Directory Space Calculator

This program calculates the total size of files in a directory and its subdirectories. It is implemented in C.

## Usage

To use the program, simply compile and run the `dirspace.c` file using a C compiler. The program will display the total size of files in the specified directory.

```bash
gcc dirspace.c -o dirspace
./dirspace
```

## Implementation

The program uses the following libraries:

- `stdio.h` for standard input/output operations.
- `stdlib.h` for dynamic memory allocation and other general-purpose functions.
- `dirent.h` for directory operations.
- `string.h` for string manipulation functions.
- `unistd.h` for directory-related constants.

The program defines several functions:

- `char **new_2D_arr()` - Allocates space for a new 2D array.
- `void free_2D_arr(char **arr)` - Frees the memory allocated for the 2D array.
- `int getEntries(char **entries, struct dirent *entity, int entry_types[MAX], char path[MAX])` - Fills a 2D array with a list of entries in the current directory.
- `int dirspace(char path[MAX])` - Calculates the total size of files in directories and subdirectories recursively.

The `dirspace` function is the main function of the program. It initializes the files' total and current path, calls the `dirspace` function recursively, and prints the total size of files.

The `dirspace` function uses the `getEntries` function to retrieve the list of entries in the current directory. It then iterates through the entries and calculates the size of files using the `fopen` and `ftell` functions.

## Implementations in Java and Python

Implementations of the directory space calculator are also available in Java and Python. You can find the source code for these implementations in the `java` and `python` directories, respectively.

- `DirectorySpaceCalculator.java` - Java implementation of the directory space calculator.
- `directory_space_calculator.py` - Python implementation of the directory space calculator.

Feel free to explore these implementations and use them according to your needs.

## Author

- Aman Hogan-Bailey
- Student ID: 1001830469
- gcc Version: 9.3.0
- Ubuntu: 20.04.1 LTS (Focal Fossa)
- CSE 1320 Virtual Machine
