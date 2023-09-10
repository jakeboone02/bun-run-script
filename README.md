Demo for [Bun](https://github.com/oven-sh/bun) issue [4850](https://github.com/oven-sh/bun/issues/4850).

When [script.js](./script.js) has the Node shebang (`#!/usr/bin/env node`):

`bun script.js` and `bun --bun run script.js` act like `node script.js`, running the script.js file:

```
$ bun script.js
script.js file
```

```
$ bun --bun run script.js
script.js file
```

`bun run script.js` acts like `npm run script.js`, running the "script.js" script defined in [package.json](./package.json):

```
$ bun run script.js
$ echo 'package.json script "script.js"'
package.json script "script.js"
```

```
$ npm run script.js

> script.js
> echo 'package.json script "script.js"'

package.json script "script.js"
```

> This project was created using `bun init` in bun v1.0.0. [Bun](https://bun.sh) is a fast all-in-one JavaScript runtime.
