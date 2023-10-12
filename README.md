# CS-330 Getting-Started-With-MATLAB
This repository was created to provide an introduction to the programming language MATLAB, for the use of a class project at Simmons University.

By Hel Nguyen

# Language Overview and Setup
MATLAB, an abriviation for Matrix Laboratory, is a high-level programming language and interactive environment designed primarily for numerical and scientific computing , data analysis, and visualization. 
## History
MATLAB was initially developed as an interactive matrix calculator written in Fortran in the late 1970s by Cleve Moler, a mathematician and computer programmer, relying on a limited set of subroutines from the LINPACK and EISPACK matrix libraries. In 1984, MATLAB transitioned into a commercial product under MathWorks, co-founded by Cleve Moler and Jack Little. John Little and programmer Steve Bangert played a key role in reprogramming MATLAB in C, crafting the MATLAB programming language, by enhancing toolbox features, user function, and graphics. MATLAB continue to evolved as versatile tool for scientists and engineers in fields like mathemathics, physics, and data science. Despite its age, MATLAB remains widely used in academia and industry due to its extensive toolboxes and simplicity, exceling in mathematical modeling, data analysis, signal and image processing, as well as machine learning and control system design.

## MATLAB® Editor 
One of the most widely used Integrated Development Environments (IDEs) for MATLAB programming is the built-in MATLAB Editor. It provides comprehensive support for MATLAB code development, including features like syntax highlighting, code completion, debugging tools, and integration with the MATLAB environment. Another option for MATLAB development is Visual Studio Code (VS Code), which offers extensive support for the MATLAB programming language through has a large library of many MATLAB-specific extensions. However, for the sake of simplicity and accessibility to a broad user base, we will focus on using the built-in MATLAB Editor for this purpose.

## Setting Up MATLAB on MacOS
To install and set up MATLAB on MacOS, you can follow these steps:

### Obtaining MATLAB License
1. **Create a MathWorks Account**: Before you begin, ensure that you have created a MathWorks account on the MathWorks website: https://www.mathworks.com/mwaccount/account/create
2. **Sign In MathWorks Account**: Once you have an account, sign in on the MATLAB website with your username and password: https://www.mathworks.com/login.
3. **Link License to MathWorks Account**: Some organizations (school or business) offer MATLAB license, if so enter the organization’s license number/activation key. Make sure your to use your work or university email. If that is not an option, MathWorks offers various license types, including individual licenses, academic licenses for students and educators for purchase in the [MathWork Store](https://www.mathworks.com/store/?ef_id=CjwKCAjwmbqoBhAgEiwACIjzEHmv933T4RiKWJfoOA1vOsfiwg6BslfC-SgBnpGTdDd9t0DEmYBHdRoCQTcQAvD_BwE:G:s&s_kwcid=AL!8664!3!548869762449!e!!g!!matlab%20license&s_eid=ppc_62715810137&q=matlab%20license&gclid=CjwKCAjwmbqoBhAgEiwACIjzEHmv933T4RiKWJfoOA1vOsfiwg6BslfC-SgBnpGTdDd9t0DEmYBHdRoCQTcQAvD_BwE).

### Installing
4. **Install MATLAB and Simulink Products**: Click the `Install MATLAB` button. Unzip the downloaded DMG file and double-click it to mount the virtual disk. Then, double-click the executable and follow the prompts to install products. 
5. **Install Java Runtime**: Native Apple Silicon MATLAB requires a Java runtime be installed on your Mac. To get a compatible runtime, install [Amazon Corretto 8](https://www.mathworks.com/support/requirements/apple-silicon.html?s_tid=pi_mpi_macajre_R2023b_maca64)

### Writing "Hello World!" Program

6. **Open MATLAB:** Launch MATLAB on your computer if it's not already open.
7. **Create a New Script:** In the `Current Folder` panel, click on the folder where you want to create the script. From the context menu, click `New Scipt` icon. This action will create a new, untitled script file in the selected folder.
8. **Write MATLAB Code**: Build code following the code below:  
   ```matlab
   disp('Hello, World!');

   ```
9. **Save the Script:** After writing your code, make sure to save the script by clicking on the "Save" icon in the MATLAB Editor's toolbar. Provide a name for the script (`.m` files). In our case write `hello_world.m`.

### Commenting In MATLAB

1. **Single-Line Comments:** Use the percent symbol `%` to create single-line comments.Anything following the `%` symbol on the same line is treated as a comment and is not executed.
   ```matlab
   x = 8
   % This is a single-line comment
   y = 9; % Assign the value 10 to the variable x
   ```
   Single-line comments are typically used for short comments or explanations on the same line as the code.
2. **Multi-Line Comments:** For multi-line comments or block comments, you can enclose your comments within `%{` and `%}` delimiters. Anything between these delimiters is considered a comment.
   ```matlab
   x = 8
   %{
   This is a
   multi-line comment
   in MATLAB
   %}
   y = 9
   ```
   Multi-line comments are often used for documenting code or providing more extensive explanations.

# Data Types and Naming Conventions

### Keywords
The below keywords cannot be used for naming variables or constants in MATLAB.

|  addpath   |   case    |   continue   |    doc     |    else    |  elseif   |      end     |   exist    |  function  |   global  |
|-------------|--------------|--------------|--------------|--------------|-------------|--------------|--------------|--------------|--------------|
|   if       |  isempty   |  length    |    load   |     max      |    min     |   ones     |    path   |     pwd      |   return   |
|    size    |    spmd   |    switch    |    true    |   false    |   zeros   |    break     |   catch    | classdef  |    for    |
|    help      |  parfor    | persistent |   try    |   while      |   cell     |   disp     |    eval   |    help      |    rand    |

### Naming Conventions:
   - MATLAB is case-sensitive
   - Structure names should begin with a capital letter.
   - Named constants (including globals) should be all uppercase using underscore to separate words.
   - Names of functions should be written in lower case.
   - Variable names should be in mixed case starting with lower case. Varibles could also be written in lowercase with words separated by underscores (snake_case). 
   - Variable names must start with a letter, followed by letters, digits, or underscores.
   - Acronyms, even if normally uppercase, should be mixed or lower case.


### Data Types   
```matlab
% Integer
myInteger = 42;

% String
myString = 'Hello, MATLAB!';

% Floating-Point Number
myFloat = 3.14159;

% Boolean
myBoolean = true;

% Array/List 
myArray = [1, 2, 3, 4, 5];

% Dictionary/Map 
myMap = containers.Map;
myMap('key1') = 'value1';
myMap('key2') = 'value2';
```

### MATLAB is Dynamically Typed 
MATLAB is dynamically typed, which means variable types are determined at runtime.
``` matlab
x = 10;
x = 'Hello';
display(x); % display hello
```
### MATLAB is Mutable
MATLAB follows a mutable variable model, which is common in dynamically typed languages.

### MATLAB is Weakly Typed
MATLAB is a weakly typed programming language because types are implicitly converted.
```matlab
x = 5;
result = x + '10'; % MATLAB will raise an error.
% You cannot concatenate an integer with a character (string) without explicit conversion
```

### MATLAB is Implicitity Type
In MATLAB, variables are implicitly typed. This means that you do not need to explicitly specify the data type of a variable when you declare it. MATLAB automatically determines the data type based on the value you assign to the variable. 

```matlab
% MATLAB promotes integers to floating-point numbers to preserve precision.
result = 5 + 2.5; % Implicitly converts 5 to 5.0 (float)

% MATLAB may implicitly convert numeric types and characters if possible.
result = '5' + 2; % Implicitly converts '5' to 5 (numeric)
```

### MATLAB Explicitly Type Conversions:
While MATLAB primarily uses implicit typing, you can use explicit type casting when you need to control the data type of a variable for specific operations.
- `double()`: Converts a value to double precision (floating-point).
- `single()`: Converts a value to single precision (floating-point).
- `int8()`, `int16()`, `int32()`, `int64()`: Converts a value to different integer types with specified bit widths.
- `uint8()`, `uint16()`, `uint32()`, `uint64()`: Converts a value to unsigned integer types with specified bit widths.
- `char()`: Converts a value to a character array.
```matlab
integerValue = 50;
doubleValue = double(integerValue); % Explicitly convert an integer to a double
```


### Operators 
| Operators | Symbols |
| --- | --- |
| Arithmetic Operators | + , - , .* , * , ./ , / , .\ , \ , .^ , ^ , .' , ' |
| Relational Operators| == , ~= , > , >= , < , <= |
| Logical Operators | & , | , && , || , ~ |


**Mixed Type Operations**: MATLAB allows mixed-type operations. When performing operations involving different data types, the program will automatically promote the data types to the most compatible type for the operation. This can sometimes lead to unexpected results if not handled carefully.
```matlab
% Mixed type operation
a = 5;
b = 3.14;
c = a + b; % Mixed type operation, c will be automatically promoted to a double
```


# Loops & Subroutinue 

## Loops

MATLAB supports `while` loops and `for` loops. It doesn't have built-in `do/while` or `foreach` loops. However, you can achieve similar functionality with `for` loops and iterate through elements.

### While Loop:
In MATLAB, the standard while loop works by first checking the condition before execution. The code ensures that the code block inside the loop runs at least once using a seperate condition.
   ```matlab
   count = 1;
   while count <= 5
       disp(count);
       count = count + 1;
   end
   ```

### For Loop:

MATLAB for loop iterates through a range of values, and you can use it as previously shown. for loop is more suitable for iterating through a predefined range of values, and the loop condition is based on this range. 
   
   ```matlab
   for i = 1:5
       disp(i);
   end
   ```


## Functions 


### Function Declaration Syntax:

In MATLAB, a typical function declaration includes the `function` keyword followed by the output variable(s) and the input parameters enclosed in parentheses. The function body is encapsulated within the `function` block.

Here's an example of a simple MATLAB function declaration:

```matlab
function output = myFunction(input1, input2)
    % Function body
    output = input1 + input2;
end
```

In the example above, `myFunction` is a MATLAB function that takes two input parameters, `input1` and `input2`, and returns a result stored in the `output` variable.

MATLAB functions can also be created without input arguments and curly brackets for simple, one-liner operations. Here's an example of such a function:

```matlab
function result = addTwoNumbers(a, b)
    result = a + b;
end
```

### Function Placement Rules:

   Functions should be placed in separate files with the same name as the function. The function file should be located in the same directory as the script calling the function. This naming and location convention helps MATLAB identify and execute functions when they are called from other scripts or functions.

### Recursive Functions:

MATLAB supports recursive functions. Recursive functions are useful for solving problems that can be broken down into smaller, similar sub-problems. In the example provided, a factorial function calculates the factorial of a number 'n' recursively. It checks a base case (n <= 1) and then calls itself with a smaller argument (n - 1) until the base case is reached. Here's an example of a factorial function:

   ```matlab
   function result = factorial(n)
       if n <= 1
           result = 1;
       else
           result = n * factorial(n - 1);
       end
   end
   ```

### Functions with Multiple Parameters and Data Types:

   MATLAB functions can accept multiple parameters, and these parameters can be of different data types. This flexibility allows you to pass various types of data to functions, making them versatile and suitable for a wide range of applications. You can have input parameters that are numbers, strings, arrays, or any other data type.

### Functions Returning Multiple Values:

  MATLAB functions can return multiple values by encapsulating them in square brackets and separating them with commas. This feature is handy when you want to return more than one result from a function. In the provided example, a function named multiValueFunction returns two values, output1 and output2. These values can be of different data types, and they can be used in the calling code for further processing or analysis.

   ```matlab
   function [output1, output2] = multiValueFunction(input1, input2)
       % Function body
       output1 = someValue1;
       output2 = someValue2;
   end
   ```

### Pass-by Reference or Value:

   MATLAB uses a combination of pass-by-value and pass-by-reference. When you pass a variable to a function, the function receives a copy of the variable, but MATLAB optimizes memory usage with copy-on-write mechanisms. This means vlues are passed by reference by value. When you pass an argument to a function, you're passing a reference to the original data in memory, allowing modifications to affect the original data outside the function. This is a combination of pass-by-reference and pass-by-value semantics.
  ```matlab
function modifiedValue = modifyValue(inputValue)
    inputValue = inputValue * 2;
    modifiedValue = inputValue;
end

originalValue = 5;
result = modifyValue(originalValue);
disp(originalValue); % The value of originalValue is still 5
disp(result); % The value of result is 10
   ```
### Storage of Arguments, Parameters, and Local Variables: 
In MATLAB, arguments, parameters, and local variables are typically stored in memory, and their storage location depends on their scope and lifetime. Function arguments are stored in memory when a function is called, and they are typically placed on the stack. Parameters are local variables within the function, and they also reside on the stack, where their memory space is allocated during the function call. Local variables declared within a function are similarly stored on the stack, and their memory is allocated when the function is executed. The stack is a region of memory specifically designated for function call management, ensuring that arguments, parameters, and local variables are efficiently managed during program execution. This stack-based memory allocation allows MATLAB to handle the creation and destruction of variables and data structures with scope limited to their respective function or block.

### Scoping Rule: 
Scoping rules in programming dictate the boundaries within which variables can be accessed and how they interact with other variables. There are two main types of scope: local and global. In local scope, variables are confined to specific blocks or functions and cannot be accessed from outside those boundaries. Global scope, on the other hand, allows variables to be accessed from anywhere within the program, including within functions or blocks.

### Side Effects:
Side effects in programming refer to unintended and often undesirable changes that occur during the execution of a program or function. These changes can affect the state of variables and data, potentially leading to unexpected or unpredictable behavior. Common examples of side effects include modifying variables unintentionally, producing excessive console output that clutters the program's output, and performing file operations without proper validation and handling. Avoiding side effects is considered a best practice as it makes code more predictable and easier to maintain. Functions that have no side effects and only produce output based on their inputs are known as "pure functions" and are easier to reason about.


[1] https://www.mathworks.com/company/newsletters/articles/a-brief-history-of-matlab.html \
[2] https://dl.acm.org/doi/10.1145/3386331 \
[3] https://en.wikipedia.org/wiki/MATLAB \
[4] https://www.geeksforgeeks.org/installing-matlab-on-macos/ \
[5] https://www.mathworks.com/videos/how-to-install-matlab-1525083586145.html \
[6] https://www.mathworks.com/help/install/ug/install-products-with-internet-connection.html \
[7] https://www.mathworks.com/help/matlab/data-types.html \
[8] https://www.mathworks.com/help/matlab/ref/iskeyword.html \
[9] https://www.ee.columbia.edu/~marios/matlab/MatlabStyle1p5.pdf \
[10] https://www.mathworks.com/help/matlab/matlab_prog/matlab-operators-and-special-characters.html \
[11] https://www.mathworks.com/help/matlab/matlab_oop/matlab-vs-other-oo-languages.html# \
[12] https://www.mathworks.com/help/matlab/numeric-types.html \
[13] 
