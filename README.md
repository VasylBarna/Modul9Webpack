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
  "dev": "webpack-dev-server --mode=development", (dev-server -- запускає сервер) ||   "dev": "npx webpack serve --mode=development",
"prod": "webpack --mode=production"
},
7
npm install webpack-dev-server --save-dev

8
npm run dev; ||
npm run prod;

9
npx webpack serve (запускаю сервер в браузері)
10
npm install --save-dev css-loader
11
  module: {
    rules: [
      {
        test: /\.css$/i,
        use: ["style-loader", "css-loader"],
      },
    ],
  },
  12
npm install --save-dev style-loader
13
npm install --save-dev babel-loader @babel/core
14
  {
        test: /\.m?js$/,
        exclude: /node_modules/,
        use: ["babel-loader"],
      },
15
babel.config.json
{
  "presets": ["@babel/preset-env"]
}
16
npm install @babel/preset-env --save-dev
17
npm install sass-loader sass webpack --save-dev
18
 test: /\.s[ac]ss$/i,
 "sass-loader"
 19
 npm install --save-dev html-webpack-plugin

 const HtmlWebpackPlugin = require('html-webpack-plugin');

   plugins: [new HtmlWebpackPlugin()],
   plugins: [new HtmlWebpackPlugin({ template: "./src/index.html" })],
 20
index.html => src/index.html (перемістити)
21
npm install --save-dev mini-css-extract-plugin

MiniCssExtractPlugin.loader,

new MiniCssExtractPlugin({ filename: "style.css" })
22
clean-webpack-plugin

23
npm install --save-dev postcss-loader postcss
npm install postcss-loader
npm install autoprefixer
plugins: [autoprefixer()]

