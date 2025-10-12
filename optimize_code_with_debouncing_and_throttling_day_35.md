# Coding Tip #35: Optimize Code with Debouncing and Throttling

When building web applications, you often deal with events that trigger frequently, such as scrolling, resizing, or typing. These events can overwhelm your app if not handled properly. That's where debouncing and throttling come in.

**Tip**: Use debouncing to limit how often a function is triggered during user input, and throttling to limit how frequently a function can be called over time.

- **Debouncing** is useful when you want to limit the number of times an event handler is executed during rapid events (e.g., typing in a search bar).
- **Throttling** is useful when you want to execute a function at fixed intervals, such as on a scroll event.

Example of debouncing:
```js
function debounce(fn, delay) {
  let timer;
  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn(...args), delay);
  };
}

const handleSearch = debounce(function(query) {
  console.log('Searching for:', query);
}, 500);

document.getElementById('search').addEventListener('input', (e) => {
  handleSearch(e.target.value);
});
```

Example of throttling:
```js
function throttle(fn, delay) {
  let lastCall = 0;
  return function (...args) {
    const now = new Date().getTime();
    if (now - lastCall >= delay) {
      fn(...args);
      lastCall = now;
    }
  };
}

const handleScroll = throttle(function() {
  console.log('Scroll event triggered');
}, 200);

window.addEventListener('scroll', handleScroll);
```


---

Thanks!


🚀Keep Coding, Keep Growing!!
