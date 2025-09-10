# Gettin' Funcy with Strings

Here's what you should understand by the end of the midterm. You should know ...

1. the basics about how variable assignment and scoping works in JS;
2. the differences between JS primitives, such as Strings, Arrays, Numbers, and Objects;
3. how to use loops and conditional statements;
4. how you can nest loops and conditional statements;
5. how to convert certain data types

## Attach the dataset

Use Observable's `FileAttachment()` to attach the `pb.txt` file with the `.text()` function.

**QUESTIONS**: 

1. What data type does your attached `pb.txt` file become?
2. How many characters are in the `pb.txt` file? HINT: Use the `.length` method.

## Counting Matched Strings

**Data to use**: `pb.txt`

Write a function that will:

1. Split a large String by a single whitespace;
2. Use an input String, e.g., `"basketball"`, to match against Strings in the split String; and
3. Return the total amount of matches as Number.

## Set of Match Info

Iterate on the previous function by writing a new function that returns a single object with the following properties:

1. Key of `keyword` with a String value of the searched for String;
2. Key of `totalMatches` with Number value of total matches found; and
3. Key of `matches` with a value of an Array that includes the matches.
4. **BONUS!** In the array of matches, create a String that also includes the String before and after the matched String:
    - EXAMPLE input of `"basketball"`:
      ```javascript
      [ "top basketball award", "womens basketball player", ... ]
      ```
