# A tiny node mysql module
## A module that eases the process of connecting to a mysql database in node.js.
### What is easier now?
  1. No need to deal with create connection or passing localhost, etc.
  2. It automatically reconnects to the database in case of connection failure or something like that.
### How to use?
Simply run:
```shell
$ npm install emran-mysql
```
Then:
```js
const EmranMysql = require('emran-mysql');

let mysqlAgent = new EmranMysql("my-username", "my-password", "my-database-name");

mysqlAgent.query("select * from googleTable", (err, rows) => {
  if(err)
    console.log("Oops! Can't read. Cause: " + err);
  else
    console.log(rows[0].myAttribute);
}
```
