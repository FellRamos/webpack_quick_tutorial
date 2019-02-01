# webpack_quick_tutorial

Quick tutorial of webpack from youtube channel [Traversy Media](https://www.youtube.com/watch?v=lziuNMk_8eQ) (check it!)

## Tips

- Because the version of webpack is now diferent, it's needed to install also **webpack-cli**. I installed globally (both webpack and webpack-cli) and it works for me, but some people just installed locally as a dev-dependency (and it works also).

- To create the bundle.js from app.js with webpack, use command **webpack --mode=development app.js -o bundle.js**. It works without **--mode=development**, but you get a warning. To keep webpack running and waiting for changes on your files, just use **webpack --mode=development app.js -o bundle.js --watch**

- On the config file, the syntaxe is a bit diferent to import the loaders:
```javascript
module.exports = {
  entry: './src/js/app.js',
  output: {
    path: __dirname+'/dist',
    filename: 'bundle.js'
  },
  module: {
    rules: [
      {
        test: /\.css$/,
        use: [
          {loader: 'style-loader'},
          {loader: 'css-loader'}
        ]
      }
    ]
  }
}
```

## Notes

> css-loader is the npm module that would help webpack to collect CSS from all the css files referenced in your application and put it into a string. 
>
> And then style-loader would take the output string generated by the above css-loader and put it inside the <style> tags in the index.html file.
>
> [Medium](https://medium.com/a-beginners-guide-for-webpack-2/webpack-loaders-css-and-sass-2cc0079b5b3a)
