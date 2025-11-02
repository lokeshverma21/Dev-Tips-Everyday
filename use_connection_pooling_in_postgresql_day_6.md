# Coding Tip #6: Use Connection Pooling in PostgreSQL

When working with PostgreSQL and Node.js, establishing a new database connection for each query can be slow and inefficient. Connection pooling can significantly improve performance by reusing existing connections.

**Tip**: Use a connection pool to manage database connections efficiently. Libraries like `pg-pool` help you implement connection pooling.

Example:
```js
const { Pool } = require('pg');
const pool = new Pool({
  user: 'dbuser',
  host: 'localhost',
  database: 'mydb',
  password: 'password',
  port: 5432,
});

// Query using connection pool
async function getUserById(userId) {
  const res = await pool.query('SELECT * FROM users WHERE id = $1', [userId]);
  return res.rows[0];
}
```


---

Thanks!


🚀Keep Coding, Keep Growing!!
