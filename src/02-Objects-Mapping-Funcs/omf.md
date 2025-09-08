# Objects, Mapping & Functions

Let's practice writing functions that do things with objects.

## Attach dataset

Attach the following CSV file with D3's `FileAttachment()` to a constant `ncVotersAll`: `/src/data/nc-voters/nc_absentee_mail_2024_random_n20000.csv`.

<p class="tip">
  Don't forget to add a <code>.csv()</code> function to the end of <code>FileAttachment()</code>, which will include the following object: <code>{typed: true}</code>.
</p>

```javascript
// Convert and attach!
```

## Render "ncVotersAll" to the page

Let's render the newly attached dataset to the page in a new codeblock.

```javascript
// Convert and render!
```

## First: A Refresher on Dates!

Let's assign a string date value that we know is also in the dataset.

```javascript
let testDateString = "09/01/2024"
```

```js
let testDateString = "09/01/2024"
```

Let's create a date parser with D3's `utcParse()` that requires a [date string specifier](https://d3js.org/d3-time-format#locale_format) scheme that matches our String representation of date data in the dataset: `00/00/0000`.

```javascript
// We need a specifier that matches `00/00/0000`
const dateParser = d3.utcParse("")

let testDateObj = dateParser(testDateString)

// Let's try it out on `testDateString`
console.log(
  "testDateString:", testDateString,
  "\ntestDateObj:", testDateObj,
)
```

## Write a function that maps new date objects and parts to our data

Ok, here's the goal. Let's write a function that we can reuse to map date objects to datasets. We want it to create a date object property and also new properties for the year, month number, and week number.

### 1. Planning our function

Let's plan it out:

1. Use `.map()` on `ncVotersAll` to create a new array of ballot objects.
2. For each ballot,
    1. Parse the date as a String and assign it to a new property on the object.
    2. Assign a week number to a new property
    3. Assign a month number to a new property
    4. Assign a year number to a new property
3. Return the updated ballot object to be mapped onto a new iterable Array of objects.

### 2. Planning our parameters to pass

Ok, with this plan in place, we need to remember that function is a scoped block of more generalizable code that we can call and use by passing along input parameters, if necessary, for the function to perform actions on before returning the end goal data.

What input parameters should we pass to our function?

1. ???

### 3. Writing our function

Let's actually write our function in a separate JS file, which we can import and use in this file. Refer to the `utils` folder and `utils.js` file inside of it.

Open up `utils.js` in a new column in VS Code, so we can write code in both files to test our work.

Let's start by naming our function. Naming functions follows a general scheme of being verb-oriented to highlight the actionable goal your function wilil achieve. In this case, we are mapping date objects and other date data, so let's keep it simple and call it `mapDateObjects`.

<div class="tip">
  <p>
    Your function's name should:
  </p>
  <ol>
    <li>Be verb-oriented and describe your singular main goal for it, and
    <li>Use camelCase casing.
  </ol>
</div>

```javascript
// Whatever I return from my function is what is assigned to our new variable
let ncVotersAllUpdated = mapDateObjects(????)
```

## Output our newly updated Array of objects

Let's see what we get by rendering `ncVotersAllUpdated` to the page:

```javascript
ncVotersAllUpdated
```