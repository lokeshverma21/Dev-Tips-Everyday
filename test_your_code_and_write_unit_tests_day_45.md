# Coding Tip #45: Test Your Code and Write Unit Tests

Testing your code is essential for ensuring that it works as expected and that future changes don’t break functionality. Writing unit tests is a key part of this.

**Tip**: Always write unit tests for critical parts of your application to catch errors early.

Example using Jest for unit testing:
```js
// simple.js
function add(a, b) {
  return a + b;
}

module.exports = add;
```
```js
// simple.test.js
const add = require('./simple');

test('adds 1 + 2 to equal 3', () => {
  expect(add(1, 2)).toBe(3);
});
```

Testing ensures you don’t inadvertently break something while refactoring or adding new features.


---

Thanks!


🚀Keep Coding, Keep Growing!!
