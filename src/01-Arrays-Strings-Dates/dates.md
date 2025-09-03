# Practice with Date() Objects

```js
// We'll cover what this code means in the D3.js section :-)
import {utcParse,utcFormat} from "d3-time-format";
```

## Create a new branch

<p class="note">
  Like always, let's start by creating a branch for this page, so we can separate our work. Use the following scheme: <code>PRAC/01-dates--lastname</code>.
</p>

## Goal

Let's practice working with Date() objects.

For your reference, here are the common String methods:

## Temporal Access Methods

The below methods for Temporal() objects help you access particular parts of dates.

| Method | Retrieved | Output  |
|--------|-------------|---------|
| `stringDateTime.year`  | year as a Number. | `2025`|
| `stringDateTime.month`  | month as a Number. | `7`|
| `stringDateTime.day`  | day of month as a Number. | `17`|
| `stringDateTime.dayOfWeek`  | day of week as a Number. | `4`|
| `stringDateTime.dayOfYear`  | day of year as a Number. | `198`|
| `stringDateTime.weekOfYear`  | week number of the year as a Number. | `29`|
| `stringDateTime.hour`  | hour as a Number. | `9`|
| `stringDateTime.minute`  | minute as a Number. | `51`|
| `stringDateTime.second`  | second as a Number. | `42`|
| `stringDateTime.millisecond`  | millisecond as a Number. | `651`|
| `stringDateTime.microsecond`  | microsecond as a Number. | `0`|
| `stringDateTime.nanosecond`  | nanosecond as a Number. | `0`|

## D3.js String Conversion Methods

We will be using D3.js a lot in this class, since they are the folks who also created Observable Framework and Plot.

It may seem silly to learn an external library, if JS has built-in methods for both Date() and the newer Temporal() objects. However, D3's d3-time-format library still includes a few more helpful methods to ultimately render prettier outputs to use in our data and charts.

We will learn the two main functions by D3 to do this parsing and formatting work:

1. [utcParse()](https://d3js.org/d3-time-format#locale_utcParse) -- Parses a `String` and can customize the format of the expected input `String` value.
2. [utcFormat()](https://d3js.org/d3-time-format#locale_format) -- Parses Date object and given a set of "specifiers", you can custom an output format.

### List of D3 specifiers

Remember that you can reference D3's docs to lookup these specifiers to use in `utcParse()` and `utcFormat()`.

- `%a` - abbreviated weekday name.\*
- `%A` - full weekday name.\*
- `%b` - abbreviated month name.\*
- `%B` - full month name.\*
- `%c` - the locale’s date and time, such as `%x, %X`.\*
- `%d` - zero-padded day of the month as a decimal number \[01,31\].
- `%e` - space-padded day of the month as a decimal number \[ 1,31\]; equivalent to `%_d`.
- `%f` - microseconds as a decimal number \[000000, 999999\].
- `%g` - ISO 8601 week-based year without century as a decimal number \[00,99\].
- `%G` - ISO 8601 week-based year with century as a decimal number.
- `%H` - hour (24-hour clock) as a decimal number \[00,23\].
- `%I` - hour (12-hour clock) as a decimal number \[01,12\].
- `%j` - day of the year as a decimal number \[001,366\].
- `%m` - month as a decimal number \[01,12\].
- `%M` - minute as a decimal number \[00,59\].
- `%L` - milliseconds as a decimal number \[000, 999\].
- `%p` - either AM or PM.\*
- `%q` - quarter of the year as a decimal number \[1,4\].
- `%Q` - milliseconds since UNIX epoch.
- `%s` - seconds since UNIX epoch.
- `%S` - second as a decimal number \[00,61\].
- `%u` - Monday-based (ISO 8601) weekday as a decimal number \[1,7\].
- `%U` - Sunday-based week of the year as a decimal number \[00,53\].
- `%V` - ISO 8601 week of the year as a decimal number \[01, 53\].
- `%w` - Sunday-based weekday as a decimal number \[0,6\].
- `%W` - Monday-based week of the year as a decimal number \[00,53\].
- `%x` - the locale’s date, such as `%-m/%-d/%Y`.\*
- `%X` - the locale’s time, such as `%-I:%M:%S %p`.\*
- `%y` - year without century as a decimal number \[00,99\].
- `%Y` - year with century as a decimal number, such as `1999`.
- `%Z` - time zone offset, such as `-0700`, `-07:00`, `-07`, or `Z`.
- `%%` - a literal percent sign (`%`).

## 1. Creating Date() or Temporal() Objects

Let's create some dates. Normally, we won't need to do these actions, since we're going to be dealing with dates within datasets. Yet, it's important to understand this very nuanced data type.

<!-- Rendered date creation code -->
```javascript
// Old school JS Date() object
const dateObject = new Date("2025-09-03T19:00:00.000")
// Note: dateObject.toString() == Wed Sep 03 2025 19:00:00 GMT-0400 (Eastern Daylight Time)

// New school (and experimental) Temporal() date object
const temporalDate = Temporal.PlainDate.from("2021-08-20")
const temporalDateTime = temporalDate.toPlainDateTime("12:34:56")
const temporalDTString = temporalDateTime.toString()
// Note: temporalDTString == 2021-08-20T12:34:56
```

<!-- Executable date creations -->
```js
// Date object to demo
const dateObject = new Date("2025-09-03T19:00:00.000")

// Temporal object
const temporalDate = Temporal.PlainDate.from("2021-08-20")
const temporalDateTime = temporalDate.toPlainDateTime("12:34:56")
const temporalDTString = temporalDateTime.toString() // 2021-08-20T12:34:56
```

## 2. Accessing Date Info & Convert Strings to Date Objects with D3.js

Look in your code editor to see the JS codeblock. Let's practice accessing and converting.

### Accessing parts of date objects

Date objects are annoyingly complex, but also very helpful when you understand them. For example, let's practice accessing different parts of the date object across Date(), Temporal(), and D3's `utcFormat()`.

```js
// D3 formatters
const formatYear = utcFormat("%Y")
const formatMonthNumber = utcFormat("%m")
const formatMonthName = utcFormat()
const formatDayOfMonth = utcFormat()
// "Wed, September 03, 2025"
const formatPrettyDate = utcFormat("%a, %B %d, %Y")

// LOG VARIATIONS
console.log(
  "## ----------------------------- ##",
  "\n## Compare Date() and Temporal() ##",
  "\n## ----------------------------- ##",
  "\n\ndateObject:", dateObject,
  "\ntemporalTime:", temporalDateTime,
  "\ntemporalDTString:", temporalDTString
)

// CONVERSIONS
console.log(
  "\n\n## ------------------- ##",
  "\n## Compare Conversions ##",
  "\n## ------------------- ##",
  "\n\nTEMP .year:", temporalDateTime.year,
  "\nDATE .getFullYear():", dateObject.getFullYear(),
  "\nD3 DATE formatYear:", formatYear(dateObject),

  "\n\nTEMP .month number:", temporalDateTime.month,
  "\nDATE .getMonth():", dateObject.getMonth(),
  "\nD3 DATE formatMonthNumber:", formatMonthNumber(dateObject),
)

// PRETTY D3 DATE OUTPUT
console.log(
  "\n\n## ----------- ##",
  "\n## PRETTY DATE ##",
  "\n## ----------- ##",
  "\nD3 DATE formatPrettyDate -->", formatPrettyDate(dateObject),
)
```
