Date: 2024-07-16
Hub: [[c]]
Tags: #web 
URL/Title:  https://www.codequoi.com/en/errno-and-error-management-in-c/

Errno stands for error number and it an integer value stored in the <errno.h> library. The error code is to indicate where something went wrong. Some functions simply return -1 or some value on failure but some functions can also return this on success so its important to know.

The process:
1. Set the errno variable
2. function called that sets errno value
3. Give debug information based on value
