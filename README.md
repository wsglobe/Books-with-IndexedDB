# Books-with-IndexedDB
## What is IndexedDB? 
IndexedDB is a database that is built into browser, much more powerful than localStorage.IndexedDB is intended for offline apps, to be combined with ServiceWorkers and other technologies.
## Advantages:
* Stores almost any kind of values by keys, multiple key types.
* Supports transactions for reliability.
* Supports key range queries, indexes.
* Can store much bigger volumes of data than localStorage.
## Basic Usage:
1. Get a promise wrapper like idb.
2. Open a database: idb.openDb(name, version, onupgradeneeded)
3. Create object storages and indexes in onupgradeneeded handler or perform version update if needed.
4. Create transaction db.transaction('books') (readwrite if needed).
5. Get the object store transaction.objectStore('books').
6. Then, to search by a key, call methods on the object store directly.
To search by an object field, create an index.
7. If the data does not fit in memory, use a cursor.

