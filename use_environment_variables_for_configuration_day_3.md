# Coding Tip #3: Use Environment Variables for Configuration

When working with Node.js applications, it's a good practice to separate your environment-specific configurations (like database URLs, API keys, etc.) into environment variables. This keeps sensitive data out of your codebase and makes your application more flexible.

**Tip**: Use `.env` files in combination with the `dotenv` package to load environment variables.

Example:
```js
// Install dotenv: npm install dotenv
require('dotenv').config();

const dbUrl = process.env.DB_URL;
const apiKey = process.env.API_KEY;

console.log(`Database URL: ${dbUrl}`);
```


---

Thanks!


🚀Keep Coding, Keep Growing!!
