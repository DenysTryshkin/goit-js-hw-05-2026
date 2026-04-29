# Homework

## Topic 6: Arrays and Object Methods

---

## Task 1. Packing Goods

**COMPLETE THIS TASK IN THE FILE `task-1.js`**

Write a function `isEnoughCapacity(products, containerSize)` that determines whether all goods will fit into a container.

The function has two parameters:

* `products` — an object where keys are product names and values are their quantities. For example: `{ apples: 2, grapes: 4 }`.
* `containerSize` — a number representing the maximum number of product units the container can hold.

The function should return the result of checking whether all goods will fit into the container. That is, calculate the total number of items in the `products` object and return `true` if it is less than or equal to `containerSize`, otherwise return `false`.

Use the code below after declaring your function to verify its correctness. The results of the function calls will be logged to the console.

```js
console.log(
  isEnoughCapacity({ apples: 2, grapes: 3, carrots: 1 }, 8)
); // true

console.log(
  isEnoughCapacity({ apples: 4, grapes: 6, lime: 16 }, 12)
); // false

console.log(
  isEnoughCapacity({ apples: 1, lime: 5, tomatoes: 3 }, 14)
); // true

console.log(
  isEnoughCapacity({ apples: 18, potatoes: 5, oranges: 2 }, 7)
); // false
```

Leave this code for mentor review.

### What the mentor will check:

* The function `isEnoughCapacity(products, containerSize)` is declared
* `isEnoughCapacity({ apples: 2, grapes: 3, carrots: 1 }, 8)` returns `true`
* `isEnoughCapacity({ apples: 4, grapes: 6, lime: 16 }, 12)` returns `false`
* `isEnoughCapacity({ apples: 1, lime: 5, tomatoes: 3 }, 14)` returns `true`
* `isEnoughCapacity({ apples: 18, potatoes: 5, oranges: 2 }, 7)` returns `false`

---

## Task 2. Calorie Calculation

**COMPLETE THIS TASK IN THE FILE `task-2.js`**

Write a function `calcAverageCalories(days)` that returns the average daily number of calories consumed by an athlete during a week.

The function expects one parameter:

* `days` — an array of objects. Each object describes a day of the week and the number of calories (`calories`) consumed on that day.

Use the code below after declaring your function to verify correctness. The results will be logged to the console.

```js
console.log(
  calcAverageCalories([
    { day: "monday", calories: 3010 },
    { day: "tuesday", calories: 3200 },
    { day: "wednesday", calories: 3120 },
    { day: "thursday", calories: 2900 },
    { day: "friday", calories: 3450 },
    { day: "saturday", calories: 3280 },
    { day: "sunday", calories: 3300 }
  ])
); // 3180

console.log(
  calcAverageCalories([
    { day: "monday", calories: 2040 },
    { day: "tuesday", calories: 2270 },
    { day: "wednesday", calories: 2420 },
    { day: "thursday", calories: 1900 },
    { day: "friday", calories: 2370 },
    { day: "saturday", calories: 2280 },
    { day: "sunday", calories: 2610 }
  ])
); // 2270

console.log(
  calcAverageCalories([])
); // 0
```

Leave this code for mentor review.

### What the mentor will check:

* The function `calcAverageCalories(days)` is declared

* The following call returns `3180`:

```js
calcAverageCalories([
  { day: "monday", calories: 3010 },
  { day: "tuesday", calories: 3200 },
  { day: "wednesday", calories: 3120 },
  { day: "thursday", calories: 2900 },
  { day: "friday", calories: 3450 },
  { day: "saturday", calories: 3280 },
  { day: "sunday", calories: 3300 }
]);
```

* The following call returns `2270`:

```js
calcAverageCalories([
  { day: "monday", calories: 2040 },
  { day: "tuesday", calories: 2270 },
  { day: "wednesday", calories: 2420 },
  { day: "thursday", calories: 1900 },
  { day: "friday", calories: 2370 },
  { day: "saturday", calories: 2280 },
  { day: "sunday", calories: 2610 }
]);
```

* The following call returns `0`:

```js
calcAverageCalories([]);
```

---

## Task 3. Player Profile

**COMPLETE THIS TASK IN THE FILE `task-3.js`**

The `profile` object describes a user's profile on a gaming platform. It contains the username and the number of active hours (`playTime`) spent in the game.

```js
const profile = {
  username: "Jacob",
  playTime: 300,
};
```

Extend the `profile` object with methods to work with its properties:

* `changeUsername(newName)` — takes a string (`newName`) and updates the `username` property. Does not return anything.
* `updatePlayTime(hours)` — takes a number (`hours`) and increases the `playTime` by this value. Does not return anything.
* `getInfo()` — returns a string in the format:
  `<Username> has <amount> active hours!`
  where `<Username>` is the profile name and `<amount>` is the number of hours played.

Use the code below after declaring your object to verify correctness:

```js
console.log(profile.getInfo()); // "Jacob has 300 active hours!"

profile.changeUsername("Marco");
console.log(profile.getInfo()); // "Marco has 300 active hours!"

profile.updatePlayTime(20);
console.log(profile.getInfo()); // "Marco has 320 active hours!"
```

Leave this code for mentor review.

### What the mentor will check:

* The variable `profile` is declared
* `profile` is an object with properties: `username`, `playTime`, `getInfo`, `changeUsername`, `updatePlayTime`
* `getInfo` is a function
* `changeUsername` is a function
* `updatePlayTime` is a function
* The `this` keyword is used inside object methods to access properties

