# arrays handling

[Back to Top Page](/FuelPHP/00_index.md)

## explode()

1. **Description**  
   It splits a string into an array by using a specified delimiter.

1. **Usage**  
   explode(separator, string, limit)

1. **Example**
   ```php
    $string = "apple,banana,orange";
    $array = explode(",", $string);
    // $array is now ['apple', 'banana', 'orange']
   ```

## implode()

1. **Description**  
   It joins the elements of an array into a single string using a specified delimiter.

1. **Usage**  
   implode(delimiter, array)

1. **Example**

   ```php
    $array = ['apple', 'banana', 'orange'];
    $string = implode(", ", $array);
    // $string is now "apple, banana, orange"
   ```

## array_map()

1. **Description**  
   It applies a callback function to each element in an array and returns a new array with the modified elements.

1. **Usage**  
   array_map(callback, array)

1. **Example**
   ```php
    $array = [1, 2, 3, 4, 5];
    $squared = array_map(function($x) { return $x * $x; }, $array);
    // $squared is now [1, 4, 9, 16, 25]
   ```
