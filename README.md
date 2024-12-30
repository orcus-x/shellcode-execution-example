
# Shellcode Execution Example

This project demonstrates the execution of shellcode using a simple C++ program. The main functionality is implemented in `main.cpp`.

## Overview

The program includes:
- A `code` array containing shellcode in hexadecimal format.
- A function pointer that points to the shellcode.
- Execution of the shellcode through the function pointer.

### **Warning**
This project is for educational purposes only. Executing arbitrary shellcode can be dangerous and may compromise system security. Ensure you fully understand the code and its implications before running it on your machine.

## Files

- `main.cpp`: Contains the main code for executing the shellcode.

## How It Works

1. The shellcode is stored in the `code` array as hexadecimal values.
2. A function pointer `func` is assigned to the shellcode.
3. The shellcode is executed by calling the function pointer.

### Shellcode Example

```c
char code[] = "\x31\xc9\x51\x68\x2e\x65\x78\x65\x68\x63\x61"
              "\x6c\x63\x89\xe0\x41\x51\x50\xbb\xfd\xe5\xf0"
              "\x76\xff\xd3\x31\xc0\x50\xb8\x4f\x21\xed\x76"
              "\xff\xe0";
```

## Compilation and Execution

### Requirements
- A C++ compiler (e.g., `gcc` or `g++`).
- A supported operating system.

### Compile
To compile the program, use the following command:
```bash
g++ main.cpp -o shellcode_exec
```

### Run
Execute the compiled binary:
```bash
./shellcode_exec
```

### Expected Behavior
If the shellcode executes successfully, the program returns `0`. Otherwise, it returns `1`.

## Disclaimer
This program is provided "as is" without any warranty. The author is not responsible for any misuse or damage caused by the execution of this code. Use responsibly and at your own risk.