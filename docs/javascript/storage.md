# `Storage`

```js
/**
 * Storage
 * localStorage
 * 
 * sessionStorage
 * survivies in same browsing context(usually a tab)
 * 需求记录刷新状态的时候使用？
 * 
 * Application Tab
 */

window.localStorage.setItem('keyName', 'keyValue')
window.localStorage.getItem('keyName')
window.localStorage.removeItem('keyName')
window.localStorage.clear()

// returns the name of the nth, U should not rely on it.
window.localStorage.key(0)
```

## `Storage.length`

## `Storage.getItem(keyName)`

## `Storage.setItem(keyName, keyValue)`

## `Storage.removeItem(keyName)`

## `Storage.clear()`

# `window.localStorage`

- `localStorage` data for a document loaded in a "private browsing" or "incognito" session is cleared when the last "private" tab is closed.

# `window.sessionStorage`

- `sessionStorage` data gets cleared when the page session ends