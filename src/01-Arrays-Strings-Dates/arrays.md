# Practice with Arrays

Arrays are just lists. In JS, an Array is a special ***iterable*** object that can contain items.

In an executable JS codeblock, I have declared and assigned an Array of Objects to the variable `dearGovernerLetters`. I logged it to the console, where we can look at it.

<p class="note">
  Be sure to open your console and ignore the warnings and errors for now.
</p>

Each item in the array is an object that represents 1 letter written to the governor of North Carolina during the Civil Rights Era. Specifically, this small snippet of the larger data are items that represent digitally archived letters, which two PhD students in the CRDM program downloaded, transcribed, and analyzed.

<!-- Declare `dearGovernerLetters` array of objects -->
```js
let dearGovernerLetters = [
  {
    "record_unit": 1,
    "title": "Letter: Albert D. Grauer and Paula M. Grauer to Gov. Dan K. Moore, April 5, 1968",
    "description": "Letter expressing support of civil rights legislation and opinions on the outbreak of violence throughout the country following the assassination of Dr. Martin Luther King, Jr. Includes a letter of response from Governor Moore.",
    "sent_date": "April 05 1968",
    "unformatted_date": "April 05 1968",
    "sender_1": "Albert D. Grauer",
    "sender_2": "Paula M. Grauer",
    "sender_race": "white",
    "event": "Assassination of Dr. Martin Luther King, Jr.; The Civil Rights Act of 1968",
    "stance": "Pro",
    "hyperlink": "View Item",
    "cleaning_status": "Clean",
    "notes": null,
    "transcript": "This is to inform you that two white North Carolina voters are in favor\nof passage of all legislation which will guarantee the rights of Negro\nAmericans. In particular we are in favor of the pending civil rights law,\nin the House of Representatives, with its open housing provision.\n\nIt is imperative that you and all in authority act as quickly as possible\nto end the injustice to the American Negro.\n\nViolence on the part of anyone should not be tolerated; but hollow calls\nfor law and order, from the white community while nothing is being done to\nchange the horrible plight of Negro Americans, are stupid and border on the\ncriminal.\n\nAll those who believe in and love America must now come forward and see to\nit that injustices against Negro Americans and all others are stopped.\n\nWith hope in the American\ndream,"
  },
  {
    "record_unit": 2,
    "title": "Letter: Albert W. Grauer and Norma J. Grauer to Gov. Dan K. Moore, April 8, 1968",
    "description": "Letter expressing opinions on current civil rights legislation and the outbreak of violence throughout the state following the assassination of Dr. Martin Luther King, Jr. Includes a letter of response from Governor Moore.",
    "sent_date": "April 08 1968",
    "unformatted_date": "April 08 1968",
    "sender_1": "Albert W. Grauer",
    "sender_2": "Norma J. Grauer",
    "sender_race": "white",
    "event": "Assassination of Dr. Martin Luther King, Jr ",
    "stance": "Pro",
    "hyperlink": "View Item",
    "cleaning_status": "Clean",
    "notes": null,
    "transcript": "Let us be fair! Let us give ALL Americans an equal opportunity. Let us all work together to provide decent housing, have open housing and do everything within our power to foster respect and dignity for ALL Americans regardless of their color.\n\nOn the other hand, violence on the part of anyone should NOT be tolerated, but hollow calls for law and order from the white community while they are doing relatively nothing to change the horrible plight of the Negro American are stupid and border on the criminal. Let us, in North Carolina, enforce the laws fairly but work to educate and change the plight, particularly of the children, born into a life in which they are doomed to poverty and ignorance.\n\nThank you, Governor Moore, for anything and everything you are attempting to do, Let us know if we can be of help in any way.\n\nTwo WHITE-PROPERTY-Owning Americans who are concerned. "
  },
  {
    "record_unit": 6,
    "title": "Letter: C. S. Alexander to Honorable William B. Umstead, July 12, 1954",
    "description": "Letter: C. S. Alexander to Honorable William B. Umstead, July 12, 1954",
    "sent_date": "July 12 1954",
    "unformatted_date": "July 12 1954",
    "sender_1": "Alexander, C. S.",
    "sender_2": null,
    "sender_race": "white",
    "event": "Brown vs. Board of Education",
    "stance": "Anti",
    "hyperlink": "View Item",
    "cleaning_status": "Clean",
    "notes": null,
    "transcript": "I have noticed in the paper that you are contemplating a Committee or a Commission to study the matter of segregation in North Carolina, particularly as it pertains to schools.\n\nIn Halifax County we are in excess of 60% colored and particularly in the agricultural section of this county where we are close to 70%, we are of course very much disturbed, and while I don't have the answer, I feel that under your wise leadership that there are sufficient men in North Carolina to devise some plan whereby the matter of mixing colored and white children in white schools can be avoided, and I hope you will permit me to suggest that on this Commission there be included men other than educators who will work out a2 solution satisfactory to both the white and colored population, and I therefore hope that you will search the field in Eastern North Carolina for some good level-headed businessmen to serve on this Committee.\n\nIn Halifax County we have made wonderful strides in the past six or seven years towards equalizing facilities of the white and colored. We now have in the county six negro high schools and six white high schools, and we have a program which over the next few years will equalize the facilities.\n\nI will be glad to sit with you if necessary in arriving at appointees of this most important undertaking.\n\nWith kind personal regards, I am sincerely yours"
  }
]
console.log(dearGovernerLetters)
```

## 1. Arrays have length and are indexed

Use .length to get the length of the array.

```javascript
dearGovernerLetters.length // 3
```

## 2. Array items are indexed

Use .length to get the length of the array.

```javascript
dearGovernerLetters[0] // First object in array
```

```javascript
dearGovernerLetters[1] // Second object in array
```

```javascript
dearGovernerLetters[2] // Third object in array
```

## 3. Use for loops to iterate across each item

Arrays are iterables, i.e., you can traverse them programmatically with special statements like for loops.

### for...in

You can access the item index with for...in loops.

```javascript
for (let ___ in dearGovernerLetters) {
  // log each item
  console.log()
}
```

### for...of

You can access the item value with for...of loops.

```javascript
for (let ___ of dearGovernerLetters) {
  // log each item
  console.log()
}
```

## 4. Use conditionals within for loops

We can do more interesting evaluations by combining for loops and conditional if...else statements.

### Conditionals with for...in

Since `for...in` loops can access the item index, you should use this structure when the position helps you create a condition with this value.

```javascript
for (let ___ in dearGovernerLetters) {
  if () {
    // Do something in here
    console.log()
  }
}
```

### Conditionals with for...of

You can access the item value with for...of loops.

```javascript
for (let ___ of dearGovernerLetters) {
  if () {
    // Do something in here
    console.log()
  }
}
```