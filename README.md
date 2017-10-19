#### Initialize NPM
- Command
```npm init```

#### Install Webpack
- Command
```npm install webpack --save-dev```
```json
{
  "name": "modern-javascript-example",
  "version": "1.0.0",
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
    Build command
```npm run build```

```"build": "webpack --progress -p" --progress``` option to show the percent progress and the -p option to minimize the code for production

    Watch
```npm run watch```

    Live reloading Webpack Dev server
```npm run server```

```"server": "webpack-dev-server --open"```  live reloading Webpack dev server

    Webpack Dev server for live reloading
        Install:
```npm install webpack-dev-server --save-dev ```


    Webpack Configuration
```
// webpack.config.js
module.exports = {
  entry: './index.js',
  output: {
    filename: 'bundle.js'
  }
};
```

    Webpack Bundleing command (CLI)
```./node_modules/.bin/webpack```

#### Install babel
- Command
```npm install babel-core babel-preset-env babel-loader --save-dev```

    Webpack configuration
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
