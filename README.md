# Functional JavaScript Cheatsheet

Do you know that JavaScript has some amazing parts, making it suitable for Functional Programming. 

Let's say I have 10 bank accounts.

```javascript
let accounts = [
  { id: 1, balance: 15.111 },
  { id: 2, balance: 7703.5 },
  { id: 3, balance: 9333.2 },
  { id: 4, balance: 1472.111 },
  { id: 5, balance: 993.5 },
  { id: 6, balance: 0.222 },
  { id: 7, balance: 1599.111 },
  { id: 8, balance: 779.5 },
  { id: 9, balance: 93.2 }
];
```

This is how I get total balance of all 10.

```javascript
let totalBalance = accounts.reduce((sum, account) => sum + account.balance, 0);
```

Now, what if I need to get all the accounts with balance higher than 700.00?

```javascript
let filteredAccounts = accounts.filter(account => account.balance > 700);
```

What if I don't care about balances, but only need the id's? 

```javascript
let ids = accounts.map(account => account.id);
```

Finally, I can sort accounts by the balances in decreasing oreder.

```javascript
accounts.sort((first, second) => first.balance < second.balance);
```

Amazing, is not it? Now let's use ES6 destructuring operator!

I have 10 numbers here.

```javascript
let numbers = [0,1,2,3,4,5,6,7,8,9];
```

This is how you can itterate and print them using Head and Tail recursion.

```javascript
function printArray(array) {
  if(array.length > 0) {
    let [head, ...tail] = array;
    console.log(head);
    printArray(tail);
  }
}
```

### TODO add more Destructing Operators, and Closures examples
