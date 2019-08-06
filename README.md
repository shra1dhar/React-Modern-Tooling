# React-Modern-Tooling

## Procedure

### Install Webpack
- `npm install --save-dependency webpack webpack-cli`
- Add `"scripts": { "build": "webpack" }` in *package.json*
- Run in dev mode using: `npm run build -- --mode development`

### Configuring Webpack
- Create *webpack.config.js* at root (preferably).
- Write custom preferences in it.
- **dist** folder contains our build file. It can be run using `node dist/app.bundle.js`

### Install Babel
- `npm i -D @babel/core @babel/cli @babel/preset-env` *(-D means dev dependancy)*
- `node_modules/.bin/babel` or `$(npm bin)/babel ./src/greet.js` to run it.
- `$(npm bin)/babel ./src/greet.js --presets=@babel/preset-env` using preset flags.

### Configure Babel
- `npm i -D babel-loader`
- Add module( with req props) in *webpack.config.js* to couple babel and webpack together.
- `npm run build` can be used to see the build file on which babel has spitted out oldbrowser compatible code.

### Install React 
- `npm i -S react react-dom prop-types` *(-S is for runtime dependancy)*
- To make babel work with react code use: `npm i -D @babel/preset-react`

### Futher Steps
- For letting webpack generate html for use install **html-webpack-plugin** `npm i -D html-webpack-plugin`

### Two Webpack configs (dev and production)
- `npm i -D webpack-merge` to maintain two separate configs without duplicating any of the settings that are shared.
- `npm install -D webpack-dev-server` to save it as a dev dependency.
- `$ npm i -D @babel/plugin-proposal-class-properties` to support proposed JavaScript Features with Babel Plugins.

## Additional Packages
- `$ npm i -D css-loader style-loader` for style and css loader.
- **css-loader** is going to let webpack handle the .css syntax, and then **style-loader** is actually going to take that, inject CSS, and inject a <style> tag into our HTML at runtime.
- `$ npm i -S react-hot-loader` for installing hot-reload package.
- `$ npm i -D webpack-bundle-analyzer` to Analyze a Production JavaScript Bundle with webpack-bundle-analyzer.



