# webpack_quick_tutorial

Quick tutorial of webpack from youtube channel [Traversy Media](https://www.youtube.com/watch?v=lziuNMk_8eQ) (check it!)

## Tips

- Because the version of webpack is now diferent, it's needed to install also **webpack-cli**. I installed globally (both webpack and webpack-cli) and it works for me, but some people just installed locally as a dev-dependency (and it works also).

- To create the bundle.js from app.js with webpack, use command **webpack --mode=development app.js -o bundle.js**. It works without **--mode=development**, but you get a warning. To keep webpack running and waiting for changes on your files, just use **webpack --mode=development app.js -o bundle.js --watch**

