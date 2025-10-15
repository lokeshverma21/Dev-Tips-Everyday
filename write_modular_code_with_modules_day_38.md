# Coding Tip #38: Write Modular Code with JavaScript Modules

As your application grows, keeping the code organized becomes essential. JavaScript modules allow you to split your code into smaller, reusable pieces that can be imported and exported between files.

**Tip**: Use `import` and `export` to write modular code that is easier to maintain and debug.

Example:
```js
// In math.js (module file)
export function add(a, b) {
  return a + b;
}

export function subtract(a, b) {
  return a - b;
}
```

```js
// In app.js (main file)
import { add, subtract } from './math.js';

console.log(add(2, 3));       // 5
console.log(subtract(5, 3));  // 2
```

Modules help isolate concerns, improve code reusability, and enhance maintainability. They're especially useful in larger projects where different parts of the application need to be logically divided into smaller units.


---

Thanks!


🚀Keep Coding, Keep Growing!!
