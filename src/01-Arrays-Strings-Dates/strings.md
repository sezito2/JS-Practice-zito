# Practice with Strings

<!-- IMPORTS -->
```js
import wtf from "wtf_wikipedia"
```

<p class="warning">
  If your notebook is erroring out, you may need to add new packages by running <code>yarn add .</code> in your terminal.
</p>

## Create a new branch

<p class="note">
  Like always, let's start by creating a branch for this page, so we can separate our work. Use the following scheme: <code>PRAC/01-strings--lastname</code>.
</p>

## Goal

Let's practice working with Strings. For your reference, here are the common String methods:

## Common String Methods

Try out the following common methods for strings located in the table below. Start by defining the variable, `str1` below in your browser's console.

```javascript
// Running string example
let str1 = "Cat In The Hat"
```

| Method | Action | Output  |
|--------|--------|---------|
| `str1.toUpperCase()`  | Converts all chars to uppercase. | `"CAT IN THE HAT"`|
| `str1.toLowerCase()`  | Converts all chars to lowercase. | `cat in the hat`|
| `str1.length`  | Retrieves the total length of String.<br>Returns Number value. | `14`|
| `str1.split(" ")`  | Splits String by given delimiter value.<br>Returns Array list of Strings. | `[ "Cat", "In", "The", "Hat" ]`|
| `str1.includes("The Hat")`  | Checks if the given String value is in the string.<br>Returns Boolean `true` or `false`. | `true`|
| `str1.startsWith("c")`  | Checks if String starts with character.<br>Returns Boolean `true` or `false`. | `false`|
| `str1.endsWidth("t")`  | Checks if String ends with character.<br>Returns Boolean `true` or `false`. | `true`|
| `str1.replace("Cat", "Dog")`  | If the method finds any matches of the<br>first `String` parameter (`"Cat"`),<br>it replaces the first matched instance ONLY<br>with the second `String` parameter (`"Dog"`).<br>Returns a `String`. | `"Dog In The Hat"`|
| `str1.replaceAll("a", "u")`  | If the method finds any matches of the<br>first `String` parameter (`"a"`),<br>it replaces ALL matched instance<br>with the second `String` parameter (`"u"`).<br>Returns a `String`. | `"Cut In The Hut"`|

## 1. Get Wikipedia Article

Let's work with a Wikipedia article about Paige Bueckers. We're going to use the `wtf_wikipedia` code library that will scrape the article from Wikipedia. We can then save the fetched article as a plain text String to the variable `pbText`.

```js
const paigeBueckersDoc = await wtf.fetch('Paige Bueckers')
```

```js
const pbText = paigeBueckersDoc.plaintext()
```

```js
pbText
```

## 2. Fun with .replaceAll()

Let's have fun and use the .replaceAll() method within this String/Wikipedia article:

```javascript
pbText.replaceAll("", "")
```

## 3. Splitting strings

How would we split this string into something that we can parse and loop through more methodically?

```javascript
// Convert and code here
```

## 4. Fun with loops, conditional statements, and `.includes()`

Ok, let's start doing some easy counting of terms. There are more sophisticated and necessary steps to take to process/clean the data. But, I just want you to get an idea about what it's like to work with textual data.

```javascript
// Convert and code here
```