# Coding Tip #7: Avoid Mutating Objects in JavaScript

In JavaScript, mutating objects (i.e., modifying objects directly) can lead to unexpected side effects and bugs, especially when passing objects between different parts of your application.

**Tip**: Always use immutable practices when working with objects and arrays to prevent unintentional mutations.

Example:
```js
// Bad: Mutating an object directly
const user = { name: 'John' };
function changeName(user) {
  user.name = 'Jane'; // Mutating the original object
}

// Good: Avoid mutation by creating a new object
function changeName(user) {
  return { ...user, name: 'Jane' }; // Creating a new object with updated data
}
```


---

Thanks!


🚀Keep Coding, Keep Growing!!
