## Big O notation

Writinga function that calcilates de sum of all numbers from 1 to n

Solution 1:

```javascript
function addTo(n) {
    let total = 0;

    for(let i = 1; i <= n; i++) {
        total += i;
    }

    return total;
}
```

Solution 2:

```javascript
function addTo2(n) {
    return n + (n + 1) / 2;
}
```

Wich is faster?

```javascript

// Snippet for test perfomance
let test1 = performance.now();
addTo(100000000);
let test2 = performance.now();

console.log(`Time elapsed: ${(test2 - test1) / 1000} seconds`) // transform in seconds

// second solution
let test3 = performance.now();
addTo2(100000000);
let test4 = performance.now();

console.log(`Time elapsed: ${(test3 - test4) / 1000} seconds`) // transform in seconds
```

