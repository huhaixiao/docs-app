# modules

## CommonJS modules

- https://nodejs.org/docs/latest/api/modules.html

### The module wrapper

### The module scopel

## ECMAScript modules

- https://nodejs.org/docs/latest/api/esm.html

```mjs title="addTwo.mjs"
function addTwo(num) {
  return num + 2;
}

export { addTwo };
```

```mjs title="app.mjs"
import { addTwo } from './addTwo.mjs';

// Prints: 6
console.log(addTwo(4));
```

### Enabling

- `.mjs` extension
- `package.json` "type" field with a value "module"

## `node:module` API

- https://nodejs.org/docs/atest/api/module.html

## Packages

- https://nodejs.org/docs/latest/api/packages.html
