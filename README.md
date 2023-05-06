# eslint-config-varp-common

<a href="https://www.npmjs.com/package/eslint-config-varp-common">
    <img src="https://nodei.co/npm/eslint-config-varp-common.png?mini=true">
</a>

### Go in

1. [Setup](#setup)

2. [User cases](#user-cases):
    * [Override rules](#override-rules)
    * [Ignore path](#ignore-path)

3. [Notes](#notes)



## Setup

1. Install with peer dependencies:

```js
npm install -D eslint-config-varp-common
```

2. Create `.prettierrc.js` file with content:

```js
module.exports = {
  /* Rrettier rules */
};
```

3. Create `.eslintrc.js` file with content:
```js
module.exports = {
  extends: ["varp-common"],
  rules: {
    /* Eslint rules */
  }
};
```

4. Add `.vscode/settings.json` file with content:
```json
{
  "editor.defaultFormatter": "dbaeumer.vscode-eslint",
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "eslint.validate": ["typescript", "typescriptreact", "javascript", "javascriptreact", "markdown", "json"],
}
```

5. Add new scripts to package.json:

```json
"scripts": {
  "lint": "eslint .",
  "lint:fix": "eslint . --fix"
}
```

## User cases

### Override rules

* Create file in selected folter: `.eslintrc.js`
* Add content:
```js
module.exports = {
  extends: '../.eslintrc.js',
  rules: {
    /* Overrided rules */
  }
};
```

### Ignore path

* Create file: `.eslintignore`
* Add content:

```
disc
```

