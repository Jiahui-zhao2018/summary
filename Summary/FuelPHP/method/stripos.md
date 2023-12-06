# stripos

[Back to Top Page](/FuelPHP/00_index.md)

## Usage

**stripos()** in PHP is a function used for case-insensitive substring searches within a string. It's similar to the strpos() function, but it doesn't differentiate between uppercase and lowercase characters when searching for a substring within a string.

The function returns the numeric position of the first occurrence of the $needle string within the $haystack string, starting from **0**. If the substring is not found, it returns **false**.

## Example

```php
$string = "Hello, this is a sample string.";
$substring = "sample";

$position = stripos($string, $substring);

if ($position !== false) {
    echo "Substring found at position: $position";
} else {
    echo "Substring not found.";
}
```

In this example, **stripos()** searches for the substring "sample" within the $string. Since it's case-insensitive, it would find the word "sample" regardless of whether it's in uppercase, lowercase, or a mix of both. If found, it returns the position; otherwise, it returns false.

## Be Careful

If the target substring is located at the beginning of the input string, the **stripos()** will return **0**, which will be treated as **false**.

So you should use

```php
if (stripos($string, $substring) !== false)
```

instead of

```php
if (!stripos($string, $substring))
```
