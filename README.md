# Node-Bring-Shopping
[![NPM version](http://img.shields.io/npm/v/bring-shopping.svg)](https://www.npmjs.com/package/bring-shopping)
[![Downloads](https://img.shields.io/npm/dm/bring-shopping.svg)](https://www.npmjs.com/package/bring-shopping)
[![Build Status](https://travis-ci.org/foxriver76/bring-api.svg?branch=master)](https://travis-ci.org/foxriver76/bring-api)


A node module for Bring! shopping lists.

## Installation
```npm install bring --production```

## Usage Example

```javascript
const bringaApi = require(`bring-shopping`);

// alternative you can use uuid as attribute, thus you wont need to login
const bring = new bringApi({mail: `example@example.com`, password: `secret`});

// login to get your uuid
await bring.login();

// get all lists and their listUuid
const lists = await bring.loadLists();
```

More important methods are `getItems(listUUID)`, `saveItem(listUuid, itemName, specificaiton)`, 
`moveToRecentList(listUuid, itemName)` and `getAllUsersFromList(listUuid)`.

## Changelog

### 1.0.0
* (foxriver76) offical release
