# String Formatting

[Back to the Top](./contents.md)

`\\` : Display a single backslash.

```C#
Console.WriteLine("c:\\source\\repos");
// Output: c:\source\repos
```

A **verbatim** string literal will keep all whitespace and characters without the need to escape the backslash. To create a verbatim string, use the `@` directive before the literal string.

```C#
Console.WriteLine(@"    c:\source\repos
        (this is where your code goes)");
// Output: c:\source\repos
//        (this is where your code goes)
```

An **interpolation** expression is indicated by an opening and closing curly brace symbol `{}`. You can put any C# expression that returns a value inside the braces. The literal string becomes a template when it's prefixed by the `$` character.

```C#
string message = $"{greeting} {firstName}!";
```

