# Q3 - Convert "INDIA" to "INDONESIA" Using `array.splice()`

## Problem Statement

Given a string:

```javascript
let string = "INDIA";
```

Convert it into:

```javascript
"INDONESIA"
```

using the `array.splice()` method.

### Expected Output

```javascript
INDONESIA
```

---

## Solution

```javascript
let string = "INDIA";

// Convert string to array
let arr = string.split("");

// Insert "ONES" after "IND"
arr.splice(3, 0, "O", "N", "E", "S");

// Convert array back to string
let result = arr.join("");

console.log(result);
```

---

## Explanation

### Step 1: Convert String into Array

```javascript
let arr = string.split("");
```

Output:

```javascript
["I", "N", "D", "I", "A"]
```

---

### Step 2: Use `splice()`

Syntax:

```javascript
array.splice(startIndex, deleteCount, item1, item2, ...)
```

In our code:

```javascript
arr.splice(3, 0, "O", "N", "E", "S");
```

Meaning:

* Start at index `3`
* Delete `0` elements
* Insert `"O"`, `"N"`, `"E"`, `"S"`

Array becomes:

```javascript
["I", "N", "D", "O", "N", "E", "S", "I", "A"]
```

---

### Step 3: Convert Array Back to String

```javascript
let result = arr.join("");
```

Output:

```javascript
"INDONESIA"
```

---

## Dry Run

Initial Array:

```javascript
["I", "N", "D", "I", "A"]
```

After `splice(3, 0, "O", "N", "E", "S")`:

```javascript
["I", "N", "D", "O", "N", "E", "S", "I", "A"]
```

After `join("")`:

```javascript
"INDONESIA"
```

---

## Output

```javascript
INDONESIA
```

---

## Methods Used

### `split()`

Converts a string into an array.

```javascript
"INDIA".split("")
```

### `splice()`

Adds, removes, or replaces elements in an array.

```javascript
arr.splice(3, 0, "O", "N", "E", "S");
```

### `join()`

Converts an array back into a string.

```javascript
arr.join("")
```

---

## Conclusion

Using `split()`, `splice()`, and `join()`, we can easily insert characters into a string by first converting it into an array. The `splice()` method is particularly useful for adding elements at a specific position.
