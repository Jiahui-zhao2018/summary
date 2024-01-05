# Getting Started

## Input/Output

The C++ language does not define any statements to do input or output.
Instead, C++ includes an extensive `standard library` that provides IO (and many
other facilities).

The `iostream` library defines four IO objects. To handle input, we use an object of type
istream named `cin`. For output, we use an ostream object named `cout`. This object is also known as the standard output. The library also defines
two other ostream objects, named `cerr` and `clog`. We typically use `cerr`, referred to as the standard error, for warning
and error messages and `clog` for general information about the execution of the
program.

```C++
#include <iostream>
int main()
{
  std::cout << "Enter two numbers:" <<endl
  int v1 = 0, v2 = 0;
  std::cin >> v1 >> v2;
  std::cout << "The sum of " << v1 << " and "
            << v2 << "is" << v1 + v2 << std::endl;
}
```

The first line of the above program tells the compiler that we want to use the `iostream` library. The name inside angle
brackets refers to a `header`.

The `<<` operator takes two operands: The left-hand operand must be an **ostream
object**; the right-hand operand is a **value** to print, and the result of the output operator is its **left-hand operand**.

The prefix `std::` indicates that the names `cout` and `endl`
are defined inside the namespace named `std`. Namespaces allow us to avoid
inadvertent collisions between the names we define and uses of those same names
inside a library. All the names defined by the standard library are in the `std`
namespace.

## How to Write Comments

Similar to C and Java.

## Flow of Control

_while_, _for_

### Reading an Unknown Number of Inputs

```C++
#include <iostream>
int main()
{
  int sum = 0, value = 0;
  // read until end-of-file, calculating a running total of all values read
  while (std::cin >> value)
    sum += value;
  std::cout << "The sum is "
            << value
            << std::endl;
  return 0;
}
```

When we use an istream as a condition, the effect is to test the state of the
stream. If the stream is valid,
then the test succeeds.

## Arithmetic Types

| Type        | Meaning                           | Minimum Size          |
| ----------- | --------------------------------- | --------------------- |
| bool        | boolean                           | NA                    |
| char        | character                         | 8bits                 |
| wchar_t     | wide character                    | 16bits                |
| char16_t    | Unicode character                 | 16bits                |
| char32_t    | Unicode character                 | 32bits                |
| short       | short integer                     | 16bits                |
| int         | integer                           | 16bits                |
| long        | long integer                      | 32bits                |
| long long   | long integer                      | 64bits                |
| float       | single-precision floating-point   | 6 significant digits  |
| double      | double-precision floating-point   | 10 significant digits |
| long double | extended-precision floating-point | 10 significant digits |

## Type Conversions

- When we assign one of the nonbool arithmetic types to a _bool_ object, the
  result is _false_ if the value is 0 and _true_ otherwise.

- When we assign a _bool_ to one of the other arithmetic types, the resulting
  value is 1 if the _bool_ is _true_ and 0 if the _bool_ is _false_.

- If we assign an out-of-range value to an object of unsigned type, the result is
  the remainder of the value modulo the number of values the target type can
  hold.

- If we assign an out-of-range value to an object of signed type, the result is `undefined`. The program might appear to work, it might crash, or it might produce garbage values.

## Integer and Floating-Point Literals

We can write an integer literal using _decimal_, _octal_, or _hexadecimal_ notation. Integer literals that begin with `0` are interpreted as _octal_. Those that begin with
either `0x` or `0X` are interpreted as _hexadecimal_.

## List Initialization

We can use any of the
following four different ways to define an int variable named `units_sold` and
initialize it to 0:

```C++
  int units_sold = 0;
  int units_sold = {0};
  int units_sold{0};
  int units_sold(0);
```

The generalized use of `{}` for initialization is referred to as **list initialization**, this form of initialization has one
important property: The compiler will not let us list initialize variables of built-in
type if the initializer might lead to the loss of information:

```C++
  long double ld = 3.1415926536;
  int a{ld}, b = {ld}; // error: narrowing conversion required
  int c(ld), d = ld; // ok: but value will be truncated
```

## Default Initialization

Variables defined outside any function body are initialized to zero, while variables of built-in type defined inside a function are **uninitialized**. The value of an uninitialized variable of built-in type is `undefined`. It is an error to copy or otherwise
try to access the value of a variable whose value is undefined.

Each class controls how we initialize objects of that class type, and most classes let us define objects without explicit initializers. Such classes supply an appropriate default value for us.

## Variable Declarations and Definitions

**Separate compilation** lets us split our programs
into several files, each of which can be compiled independently.

A **declaration** makes a name known to the program. A file that wants
to use a name defined elsewhere includes a declaration for that name while a **definition**
creates the associated entity.

A **variable declaration** specifies the type and name of a variable. A **variable definition** is a declaration. In addition to specifying the name and type, a definition also allocates storage and may provide the variable with an initial value.

To obtain a declaration that is not also a definition, we add the `extern` keyword and may not provide an explicit initializer.

Any declaration that includes an explicit initializer is a definition, and it is an error to provide an initializer on an extern inside a function.

- **Note**:
  ```
  Variables must be defined exactly once but can be declared many times.
  ```

To use a variable in more than one file requires declarations that are separate from the variable’s definition. To use the same variable in multiple files, we must define that variable in one—and only one—file. Other files that use that variable must declare—but not define—that variable.

## Scope of a Name

- Names are visible from the point where they are declared until the end of the scope in which the declaration appears.

- Scopes can contain other scopes. The nested scope is an inner scope, the containing scope is the outer scope. Once a name has been declared in a scope, that name can be used by scopes nested inside that scope. Names declared in the outer scope can also be redefined in an inner scope.

## Compound Types

A _reference_ defines an alternative name for an object. A reference type “refers to” another type. We define a reference type by writing a declarator of the form `&d`, where `d` is the name being declared.

When we define a reference, instead of copying the initializer’s value, we bind the reference to its initializer. Once initialized, a reference remains bound to its initial object. There is no way to rebind a reference to refer to a different object. Because there is no way to rebind a reference, references **must** be initialized.
