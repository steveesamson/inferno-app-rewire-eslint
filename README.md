# Create your inferno app using `create-inferno-app my-app` or use an CRA app

# Rewire it

## 1) Install inferno-app-rewired + inferno-app-rewire-eslint

```bash
npm install inferno-app-rewired inferno-app-rewire-eslint --save
```

## 2) Create a config-overrides.js file in the root directory

```javascript
const rewireEslint = require('inferno-app-rewire-eslint');

/* config-overrides.js */
module.exports = function override(config, env) {
  config = rewireEslint(config, env);
  return config;
}
```

## 3) Create your own .eslintrc in the root directory

**Sample Structure**

```
+-- your-project
|   +-- .eslintrc
|   +-- config-overrides.js
|   +-- node_modules
|   +-- package.json
|   +-- public
|   +-- README.md
|   +-- src
```
