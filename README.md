<h1 align="center">It`s my page for Rose collection dresses</h1>

<h2 align="center">Install with npm:</h2>

You should download and instal webpack: 4.16.5

For local run the following commands:
```bash
   npm init -y
   npm install webpack webpack-cli --save-dev
```

And of curse you should run webpack-dev-server. For installation run the following command:
```bash
npm install --save-dev webpack-dev-server
```

All plugins you can see in my package.json

It is "css-loader". For installation run the following command:
```bash
npm install --save-dev css-loader
```
It is "less-loader". For installation run the following command:
```bash
npm install less-loader --save-dev
```

It is "less". For installation run the following command:
```bash
npm i less -D
```

It is "style-loader". For installation run the following command:
```bash
npm install style-loader --save-dev
```

In your package-lock.json should be the following scripts:
```bash
"dist": "webpack",
"dev": "webpack-dev-server --hot --open --inline"

In your webpack.config.js should be the following options:
  mode: 'development',
  entry: './src/index.js',
  output: {
    filename: 'main.js',
    path: path.resolve(__dirname, 'dist')
  },
  devServer: {
    contentBase: path.resolve(__dirname, 'dist'),
    hot: true
  },
  module: {
    rules:[
      {
        test: /\.less$/,
        use: ['style-loader', 'css-loader','less-loader']
      }
    ]
  },
  watch: true
```

  For pack you should run the following command:
```bash
  npm run dist
  npm run dev
```