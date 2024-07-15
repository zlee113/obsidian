Date: 2024-07-15
Hub: [[c]]
Tags: #web
URL/Title:  https://www.tutorialspoint.com/c_standard_library/c_function_fscanf.htm

Reads a formatted input from a file with a format specifier. Can read into a variable amount of locations in memory (good for filling out structs).

```c
int fscanf(FILE *stream, const char *format, ...);
```

Parameters:
- FILE \*stream: pointer to file object to indicate to the function where to be reading from
- const char \* format: Format string to specify how the stream should handle different variables
- ...: Variable amount of additional arguments pointing to location(s) where the parsed variables should be stored.

Example:
```c
#include <stdio.h>
#include <stdlib.h>

int main() {
   const char *filename = "example1.txt";
   FILE *file = fopen(filename, "r");

   int number;
   char word[50];

   if (fscanf(file, "%d %49s", &number, word) == 2) {
       printf("Number: %d, Word: %s\n", number, word);
   } else {
       printf("Failed to read data from file.\n");
   }

   fclose(file);
   return 0;
}
```

From a file reads an int and 49 characters max of a string until the end of the line.

Outputs: `Number: 123, Word: HelloWorld`
