# react-parcel

Setting up a React project with Parcel as a bundler.

## Specification

* Git
* Parcel
* Babel 
* React
* SCSS
* CSS Modules
* Build for Production

## Procedure

* $ google-chrome https://github.com/shinesincere
~ `Repository name: react-parcel`
~ `Initialize this repository with a README`
~ `Create repository`

* $ git clone https://github.com/shinesincere/react-parcel

* $ cd react-parcel && code .

* react-parcel $ npm i -S react react-dom

* react-parcel $ npm i -D babel-preset-react babel-preset-env node-sass postcss-modules autoprefixer

* react-parcel $ code .gitignore 
~ `.env .cache dist node_modules`

* react-parcel $ code .babelrc
~ `
  {
    "presets": [
      "env", 
      "react"
    ]
  }
`

* react-parcel $ code .postcssrc
~ `
  {
    "modules": true,
    "plugins": {
      "autoprefixer": {
        "browsers": [
          "> 1%",
          "Last 2 versions",
          "IE 10"
        ]
      }
    }
  }
`  

* react-parcel $ code index.html 
~ `<script src="./index.js"></script>`

* react-parcel $ code index.js
~ `import classes from './index.css';`

* react-parcel $ code index.css
~ `body {background: pink;}`

* react-parcel $ code package.json
~ `
  "scripts": {
    "start": "parcel index.html",
    "build": "parcel build index.html -d build --public-url ./"
  },
`

* react-parcel $ npm start
~ http://localhost:1234

* react-parcel $ code src/App.js
~ `
  import React from 'react';
  export default () => <div>App</div>
`

* react-parcel $ code index.js
~ `
  import classes from './index.css';
  import React from 'react';
  import ReactDOM from 'react-dom';
  import App from './src/App';
  ReactDOM.render(<App/>, document.getElementById("app"));
`

* react-parcel $ code index.html
~ `<div id="app"></div><script src="./index.js"></script>`

* react-parcel $ code src/app.scss
~ `
  .title {
    color: white;
  }
`

* react-parcel $ code src/App.js
~ `
  import React from 'react';
  import app from './app.css';
  export default () => <div className={app.title}>App</div>
`

* react-parcel $ npm build
~ `file:///home/s/Code/2019/Github/react-parcel/build/index.html`

* react-parcel $ git status

* react-parcel $ git add .