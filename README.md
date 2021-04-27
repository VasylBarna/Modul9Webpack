# Modul9Webpack

Modul9Webpack-repeta
1
npm init -y
2
npm install webpack webpack-cli --save-dev
3
index.html
4
/src/index.js
5
webpack.config.js
const path = require("path");
module.exports = {
mode: 'development',
entry: "./src/index.js",
output: {
path: path.resolve(\_\_dirname, "build"),
filename: "bundle.js",
},
};
6
package.json:
"scripts": {
  "dev": "webpack-dev-server --mode=development", (dev-server -- запускає сервер)
"prod": "webpack --mode=production"
},
7
npm install webpack-dev-server --save-dev

8
npm run dev; ||
npm run prod;