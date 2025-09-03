# ENG 498/583 JS Practice

Let's start our JS journey by creating our own sandbox of primitives.

<p class="note">
  Like always, let's start by creating a branch for this page, so we can separate our work. Use the following scheme: <code>PRAC/0-prims--lastname</code>.
</p>

## 1. Primitives: Declaring & Assigning Variables

In your group, create a suite of the following primitives about a topic of your choice. For example, if the Strings are about ingredients to make a dish, then numbers could represent the measurement amount.

- 5 Strings with `let`
- 5 Numbers  with `const`
- 1 array for the Strings
- 1 array for the Numbers
- 1 array of 5 objects that combines the Strings and Numbers into 1

```js
// 5 Strings
let strawberry = "Fruit"
let carrot = "Vegetable"
let cheese = "Dairy"
let chicken = "Protein"
let bread = "Grain"

// 5 const numbers
const shot = 4
const small = 12
const medium = 16
const large = 18
const extraLarge = 24


// 1 array for the Strings with the variable names
let foods = [strawberry, carrot, cheese, chicken, bread]

// 1 array for the Numbers with the variable names
let cupSizes = [shot, small, medium, large, extraLarge]

/**
 * 1 array of 5 objects that combines the Strings
 * and Numbers into 1 object as 2 properties of
 * each object
**/
let foodOrder = [
  {foodGroup: strawberry, drink: shot},
  {foodGroup: carrot, drink: small},
  {foodGroup: cheese, drink: medium},
  {foodGroup: chicken, drink: large},
  {foodGroup: bread, drink: extraLarge},
]

console.log(foodOrder)
```

## 2. Playing with Our Data in the Web Console

### Strings

Concatenate them with `+` operator.

```js
// Convert and play
cheese+" and "+chicken
```

Access position of individual characters at index.

```js
strawberry[0]
```

### Numbers

Use arithmetic operators to yield computations: `+`, `-`, `*`, `/`, etc.

```js
extraLarge/shot
```

## 3. Finding Built-In Docs Arrays & Objects in the Web Console

### Array

Log your simple Array of Strings to the console, so we can check out what built-in methods we can use for Arrays.

```javascript
console.log(cupSizes)
```

Log your Array of Objects to the console, so we can check out what built-in methods we can use for Objects.

### Array of Objects

```js
console.log(foodOrder[2].foodGroup)
```

## 4. (Block) Scope & Conditional Statements

Let's learn about ***scope***.

In any programming language environment, you need to be aware of how, when, and where you write your code and use variables. Scope is essential to understanding what parts of the code will have access to data versus other parts.

Scope is the current context of execution in which values and expressions are "visible" or can be referenced. If a variable or expression is not in the current scope, it will not be available for use. Scopes can also be layered in a hierarchy, so that child scopes have access to parent scopes, but not vice versa.

JS has the following kinds of scopes:

- **Global scope**: The default scope for all code running across all folders/files in the program's project architecture.
- **Module scope**: The scope for code running in module mode, i.e., reserved for that singular file.
- **Function scope**: The scope created with a function: `() => {...}`
- **Block scope**: The scope created with a pair of curly braces (a block): `{...}`.

Let's focus on ***block scope*** for now by writing conditional statements. Please write the following code:

1. Create at least 3 conditional statements in the provided codeblock.
    <p class="note">One conditional statement should include 2 conditions to evaluate</p>
2. Log an output to the console to verify that your conditional statement was evaluated the way that you had hoped it would.

```javascript
// Convert and write your conditional statement

```
