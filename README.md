# gun-sqlite

A Gun <> SQLite Adapter for NodeJs apps to enable long-term storage for Gun data.

This is a nodejs-ified version of https://github.com/lolotrgeek/gun-react-native-sqlite.

## Installation

`npm install gun-sqlite --save` or `yarn add gun--sqlite`.

This module depends on `sqlite3` for SQLite bindings.

## Run

```javascript
const Gun = require('gun')
const GunSQLite = require('gun-sqlite');
const adapter = GunSQLite.bootstrap(Gun);

const gun = new Gun({
    ...
    file: false,
    radisk: false,
    localStorage: false,
    // Defaults
    sqlite: {
        database_name: "GunDB.db",
    }
})
```