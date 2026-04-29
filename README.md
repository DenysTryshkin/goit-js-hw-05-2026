# Homework

## Topic 8: Iterative Array Methods

---

## Task 1: User Names

Work on this task in the file `task-1.js`.

Write an arrow function `getUserNames(users)` that takes one parameter `users` — an array of user objects.

The function should return an array of all user names (the `name` property) from the `users` array.

Use the code below after your function declaration to verify that it works correctly. The results of the function calls will be printed to the console.

```js
console.log(
  getUserNames([
    {
      name: "Moore Hensley",
      email: "moorehensley@indexia.com",
      balance: 2811
    },
    {
      name: "Sharlene Bush",
      email: "sharlenebush@tubesys.com",
      balance: 3821
    },
    {
      name: "Ross Vazquez",
      email: "rossvazquez@xinware.com",
      balance: 3793
    },
    {
      name: "Elma Head",
      email: "elmahead@omatom.com",
      balance: 2278
    },
    {
      name: "Carey Barr",
      email: "careybarr@nurali.com",
      balance: 3951
    },
    {
      name: "Blackburn Dotson",
      email: "blackburndotson@furnigeer.com",
      balance: 1498
    },
    {
      name: "Sheree Anthony",
      email: "shereeanthony@kog.com",
      balance: 2764
    },
  ])
); // ["Moore Hensley", "Sharlene Bush", "Ross Vazquez", "Elma Head", "Carey Barr", "Blackburn Dotson", "Sheree Anthony"]
```

Leave this code for mentor review.

### Mentor checklist:

* The variable `getUserNames` is declared
* `getUserNames` is assigned an arrow function with parameter `(users)`
* The `map()` method is used to iterate over `users`
* The function returns the correct array of names
* The function works correctly with valid random inputs

---

## Task 2: Users with a Friend

Work on this task in the file `task-2.js`.

Write an arrow function `getUsersWithFriend(users, friendName)` that takes two parameters:

* `users` — an array of user objects
* `friendName` — the name of a friend to search for

The function should return an array of all users who have a friend with the name `friendName`.
Each user's friends are stored in the `friends` property.

If no users have such a friend, return an empty array.

### Tips:

* Use the `filter()` method to create a new array with matching elements
* Use the `includes()` method to check if `friends` contains `friendName`

Use the code below to test your function:

```js
const allUsers = [
  {
    name: "Moore Hensley",
    friends: ["Sharron Pace"]
  },
  {
    name: "Sharlene Bush",
    friends: ["Briana Decker", "Sharron Pace"]
  },
  {
    name: "Ross Vazquez",
    friends: ["Marilyn Mcintosh", "Padilla Garrison", "Naomi Buckner"]
  },
  {
    name: "Elma Head",
    friends: ["Goldie Gentry", "Aisha Tran"]
  },
  {
    name: "Carey Barr",
    friends: ["Jordan Sampson", "Eddie Strong"]
  },
  {
    name: "Blackburn Dotson",
    friends: ["Jacklyn Lucas", "Linda Chapman"]
  },
  {
    name: "Sheree Anthony",
    friends: ["Goldie Gentry", "Briana Decker"]
  }
];

console.log(getUsersWithFriend(allUsers, "Briana Decker"));
console.log(getUsersWithFriend(allUsers, "Goldie Gentry"));
console.log(getUsersWithFriend(allUsers, "Adrian Cross")); // []
```

Leave this code for mentor review.

### Mentor checklist:

* The variable `getUsersWithFriend` is declared
* It is an arrow function with parameters `(users, friendName)`
* The `filter()` method is used
* Returns correct users for "Briana Decker" and "Goldie Gentry"
* Returns an empty array when no matches are found
* Works correctly with valid random inputs

---

## Task 3: Sort by Number of Friends

Work on this task in the file `task-3.js`.

Write an arrow function `sortByDescendingFriendCount(users)` that takes one parameter `users` — an array of user objects.

The function should return a new array of users sorted in descending order by the number of their friends (`friends` property).

Use the code below to test your function:

```js
console.log(
  sortByDescendingFriendCount([
    {
      name: "Moore Hensley",
      friends: ["Sharron Pace"],
      gender: "male"
    },
    {
      name: "Sharlene Bush",
      friends: ["Briana Decker", "Sharron Pace"],
      gender: "female"
    },
    {
      name: "Ross Vazquez",
      friends: ["Marilyn Mcintosh", "Padilla Garrison", "Naomi Buckner"],
      gender: "male"
    },
    {
      name: "Elma Head",
      friends: ["Goldie Gentry", "Aisha Tran"],
      gender: "female"
    },
    {
      name: "Carey Barr",
      friends: ["Jordan Sampson", "Eddie Strong"],
      gender: "male"
    },
    {
      name: "Blackburn Dotson",
      friends: ["Jacklyn Lucas", "Linda Chapman"],
      gender: "male"
    },
    {
      name: "Sheree Anthony",
      friends: ["Goldie Gentry", "Briana Decker"],
      gender: "female"
    }
  ])
);
```

Leave this code for mentor review.

### Mentor checklist:

* The variable `sortByDescendingFriendCount` is declared
* It is an arrow function with parameter `(users)`
* The `toSorted()` method is used
* Returns a new array sorted by descending number of friends
* Works correctly with valid random inputs

---

## Task 4: Total Balance

Write an arrow function `getTotalBalanceByGender(users, gender)` that takes two parameters:

* `users` — an array of user objects
* `gender` — a string representing gender

The function should use a chain of methods and return the total balance (`balance` property) of users whose `gender` matches the given parameter.

Use the code below to test your function:

```js
const clients = [
  {
    name: "Moore Hensley",
    gender: "male",
    balance: 2811
  },
  {
    name: "Sharlene Bush",
    gender: "female",
    balance: 3821
  },
  {
    name: "Ross Vazquez",
    gender: "male",
    balance: 3793
  },
  {
    name: "Elma Head",
    gender: "female",
    balance: 2278
  },
  {
    name: "Carey Barr",
    gender: "male",
    balance: 3951
  },
  {
    name: "Blackburn Dotson",
    gender: "male",
    balance: 1498
  },
  {
    name: "Sheree Anthony",
    gender: "female",
    balance: 2764
  }
];

console.log(getTotalBalanceByGender(clients, "male")); // 12053
console.log(getTotalBalanceByGender(clients, "female")); // 8863
```

Leave this code for mentor review.

### Mentor checklist:

* The variable `getTotalBalanceByGender` is declared
* It is an arrow function with parameters `(users, gender)`
* A correct method chain is used
* The `users` array is not modified
* Returns `12053` for "male"
* Returns `8863` for "female"
* Works correctly with valid random inputs

