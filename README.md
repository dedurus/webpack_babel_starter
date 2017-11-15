#### Initialize NPM
- Command
```npm init```

#### Install Webpack
- Command
```npm install webpack --save-dev```
```json
{
  "name": "webpack_babel",
  "version": "1.0.1",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "build": "webpack --progress -p",
    "watch": "webpack --progress --watch",
    "server": "webpack-dev-server --open"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {

  },
  "devDependencies": {
    "webpack": "^3.7.1"
  }
}
```
- Build command<br>
```npm run build```

```"build": "webpack --progress -p" --progress```<br>
option to show the percent progress and the -p option to minimize the code for production

- Watch<br>
```npm run watch```<br><br>

- Live reloading Webpack Dev server<br>
```npm run server```<br><br>

```"server": "webpack-dev-server --open"```<br>
live reloading Webpack dev server

- Webpack Dev server for live reloading<br>
    - Install:<br>
```npm install webpack-dev-server --save-dev ```


- Webpack Configuration<br>
```
// webpack.config.js
module.exports = {
  entry: './index.js',
  output: {
    filename: 'bundle.js'
  }
};
```

- Webpack Bundleing command (CLI)<br>
```./node_modules/.bin/webpack```

#### Install babel
- Command<br>
```npm install babel-core babel-preset-env babel-loader --save-dev```<br><br>

- Webpack configuration<br>
```
// webpack.config.js
module.exports = {
  entry: './index.js',
  output: {
    filename: 'bundle.js'
  },
  module: {
    rules: [
      {
        test: /\.js$/,
        exclude: /node_modules/,
        use: {
          loader: 'babel-loader',
          options: {
            presets: ['env']
          }
        }
      }
    ]
  }
};
```
