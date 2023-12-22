# Variables

[Back to the Top](./contents.md)

## Declare a variable

To create a new variable, you must first declare the **data type** of the variable, and then give it a **name**.

Here's a few important considerations about variable names:

- Variable names **can** contain alphanumeric characters and the underscore character. Special characters like the hash symbol # or dollar symbol $ are **not** allowed.

- Variable names must begin with an alphabetical letter or an underscore, not a number.

- Variable names are **case-sensitive**, meaning that `string Value;` and `string value;` are two different variables.

- Variable names must not be a C# keyword. For example, you cannot use the following variable declarations: `decimal decimal`; or `string string;`.

Here are some coding conventions for variables:

- Variable names should use camel case

- Variable names should begin with an alphabetical letter (Underscore is used for a special purpose).

- Variable names should be descriptive and meaningful in your app.

- Variable names should be one or more entire words appended together. Don't use contractions or abbreviations because the name of the variable.

- Variable names shouldn't include the data type of the variable.

### Variable name examples

```C#
char userOption;

int gameScore;

decimal particlesPerMillion;

bool processedCustomer;
```

## Declare implicitly typed local variables

An implicitly typed local variable is created by using the `var` keyword followed by a variable initialization.

The `var` keyword tells the C# compiler that the data type is implied by the assigned value. After the type is implied, the variable acts the same as if the actual data type had been used to declare it.

In the example:

```C#
var message = "Hello world!";
```

the `message` variable is typed to be a string and can never be changed.

The `var` keyword is dependent on the value you use to initialize the variable. If you try to use the var keyword without initializing the variable, you'll receive an error when you attempt to compile your code.

The `var` keyword has an important use in C#. Many times, the type of a variable is obvious from its initialization. In those cases, it's simpler to use the `var` keyword. The `var` keyword can also be useful when planning the code for an application. When you begin developing code for a task, you may not immediately know what data type to use. Using var can help you develop your solution more dynamically.
