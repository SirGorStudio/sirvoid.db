# void.db
**Support:** https://github.com/SirGorStudio/sirvoid.db/issues
**NPM:** [npmjs.com/package/sirvoid.db](https://www.npmjs.com/package/sirvoid.db)<br>

```js
const Database = require("void.db");
const db = new Database("./db.json");

db.set('serverStatus', { status: 'Online' })
/*
"serverStatus": {
  "status": "Online"
}
*/
db.add("money_sirgor", 500)
/* 
  "money_sirgor": 500
*/
db.push("serverSettings", { whitelist: "on", playerCount: "24" })
/*
"serverSettings": [
    {
      "whitelist": "on",
      "playerCount": "24"
    }
  ]
*/
db.has("money_sirgor") // true
db.has("money_sirgor") // false

db.get("money_sirgor")
// => 500

db.sub("money_sirgor", 100)
// => 400

db.fetch("serverStatus")
// => { status: "Online" }

db.get("serverStatus")
// => { status: "Online" }

db.delete("serverStatus")
// => {}

db.all()
/*
{
  money_sirgor: 500,
  serverSettings: [ { whitelist: 'on', playerCount: '24' } ]
}
*/

db.clear()
// {}
```
## Installation
*If you have trouble with the installation, please feel free to visit https://github.com/SirGorStudio/sirvoid.db/issues address.*
- `npm i sirvoid.db`