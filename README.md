<h3 align="center"><a href="https://github.com/learnwithsumit/think-in-a-react-way">Install React- app </a></h3>

## react-app setup

Please follow the below instructions to run this project in your computer:

1. For Remove react-app
   ```sh
   yarn global remove create-react-app
   ```
2. For install react-app
   ```sh
   npx create-react-app myreact
   ``` 
3. For install react router dom

   ```sh
   yarn add react-router-dom@6
   ```
4. For install styled component

   ```sh
   npm install --save styled-components
   ```
5. For install owl carousel

   ```sh
   npm i react-owl-carousel
   ```
   
    7. For implement owl carousel
   ```sh
   import OwlCarousel from 'react-owl-carousel';
   import 'owl.carousel/dist/assets/owl.carousel.css';
   import 'owl.carousel/dist/assets/owl.theme.default.css';
   ```
otstrap/dist/js/bootstrap.bundle";
   ```
   
6. For install react bootstrap
   
   ```sh
   npm install react-bootstrap bootstrap
   ```
   
 7. For implement react bootstrap
   <h3>css</h3>
   
   ```sh
   import 'bootstrap/dist/css/bootstrap.min.css';
   ```
   <h3>js</h3>
   
   ```sh
   import "bootstrap/dist/js/bootstrap.bundle";
   ```
   
 <h3 align="center">github link remote add</h3>
 
 ```sh
 git remote add origin 
 ```
 
<h3 align="center"><a href="https://github.com/learnwithsumit/think-in-a-react-way">For React Error</a></h3>

## Resolve the Errors

Please follow the below instructions to run this project in your computer:

1. For "babel/eslint-parser" Error
   ```sh
   yarn add eslint @babel/core @babel/eslint-parser -D
   ```
2. For "react" was conflicted between ".eslintrc" Error
   ```sh
   npm install --dev eslint-config-react-app
   ``` 

[![Youtube][youtube-shield]][youtube-url]
[![Facebook-Page][facebook-shield]][facebook-url]
[![Facebook-Group][facebook-shield]][facebook-group-url]
[![Instagram][instagram-shield]][instagram-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- PROJECT Title -->
<br />
<p align="center">
  <h3 align="center"><a href="https://github.com/learnwithsumit/think-in-a-react-way">Lesson 3 - Think in a React way Tutorial Series [ in Bangla ]</a></h3>

<!-- TABLE OF CONTENTS -->

## Table of Contents

- [How to run](#how-to-run)
- [Editor Setup](#editor-setup)
  - [Plugins](#plugins)
  - [Settings](#settings)
  - [Set Line Breaks](#set-line-breaks)
- [Linting Setup](#linting-setup)
  - [Install Dev Dependencies](#install-dev-dependencies)
  - [Create Linting Configuration file manually](#create-linting-configuration-file-manually)
- [Contact](#contact)

<!-- HOW TO RUN -->

## How to run

Please follow the below instructions to run this project in your computer:

1. Clone this repository
   ```sh
   git clone https://github.com/learnwithsumit/think-in-a-react-way.git
   ```
2. Checkout to branch "lesson-3"
   ```sh
   git checkout lesson-3
   ```
3. Run
   ```sh
   yarn
   ```
4. Your app should be available in http://localhost:5500

<!-- Editor Setup -->

## Editor Setup

You can use any editor but as I personally prefer VS Code. I will give some instructions about how I prefer VS code to be setup for React applications.

### Plugins

You need to install the below plugins:

- ESLint by Dirk Baeumer
- Prettier - Code formatter by Prettier
- Dracula Official Theme (optional)

### Settings

Follow the below settings for VS Code -

1. Create a new folder called ".vscode" inside the project root folder
2. Create a new file called "settings.json" inside that folder.
3. Paste the below json in the newly created settings.json file and save the file.

```json
{
  // Theme
  // "workbench.colorTheme": "Dracula",
  "liveSassCompile.settings.formats": [
    {
      "format": "compressed",
      "extensionName": ".css",
      "savePath": "/assets/css"
    }
  ],
  "liveSassCompile.settings.generateMap": false,
  // config related to code formatting
  "editor.mouseWheelZoom": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "[javascript]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascriptreact]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "javascript.validate.enable": true, //disable all built-in syntax checking
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true,
    "source.fixAll.tslint": true,
    "source.organizeImports": true
  },
  "eslint.alwaysShowStatus": true,
  // emmet
  "emmet.triggerExpansionOnTab": true,
  "emmet.includeLanguages": {
    "javascript": "javascriptreact"
  },
  "editor.fontFamily": "'Fira Code'"
}


```

If you followed all previous steps, the theme should change and your editor should be ready.

### Set Line Breaks

Make sure in your VS Code Editor, "LF" is selected as line feed instead of CRLF (Carriage return and line feed). To do that, just click LF/CRLF in bottom right corner of editor, click it and change it to "LF". If you dont do that, you will get errors in my setup.

<img src="public/line-feed.jpg" alt="Line Feed" width="700">

## Linting Setup

In order to lint and format your React project automatically according to popular airbnb style guide, I recommend you to follow the instructions below.

### Install Dev Dependencies

```sh
yarn add -D prettier
yarn add -D babel-eslint
npx install-peerdeps --dev eslint-config-airbnb
yarn add -D eslint-config-prettier eslint-plugin-prettier
```

or You can also add a new script in the scripts section like below to install everything with a single command:

<h4>script </h4>

```json
    "lint": "yarn add -D prettier && yarn add -D babel-eslint && npx install-peerdeps --dev eslint-config-airbnb && yarn add -D eslint-config-prettier eslint-plugin-prettier"

```

and then simply run the below command in the terminal -

```sh
yarn lint #or 'npm run lint'
```

### Create Linting Configuration file manually

Create a `.eslintrc` file in the project root and enter the below contents:

```json
{
  "extends": [
    "airbnb",
    "airbnb/hooks",
    "eslint:recommended",
    "prettier",
    "plugin:jsx-a11y/recommended"
  ],
  "parser": "@babel/eslint-parser",
  "parserOptions": {
    "ecmaVersion": 8,
    "requireConfigFile": false,
    "babelOptions": {
      "presets": ["@babel/preset-react"]
    }
  },
  "ignorePatterns": [
    "**/Server/*",
    "**/node_modules/*",
    "**/library/**",
    "/sw.js"
  ],
  "env": {
    "browser": true,
    "node": true,
    "es6": true,
    "jest": true
  },
  "rules": {
    // "react/sort-comp": 0,
    // "react/jsx-no-bind": 0,
    "jsx-a11y/mouse-events-have-key-events": 0,
    "react/prefer-stateless-function": 0,
    "class-methods-use-this": 0,
    "react/no-access-state-in-setstate": 0,
    "react/destructuring-assignment": 0,
    "react/react-in-jsx-scope": 0,
    "react-hooks/rules-of-hooks": 0,
    "react/no-unescaped-entities": 0,
    "no-console": 0,
    "react/state-in-constructor": 0,
    "indent": 0,
    "linebreak-style": 0,
    "react/prop-types": 0,
    "jsx-a11y/click-events-have-key-events": 0,
    "jsx-a11y/no-static-element-interactions": 0,
    "jsx-a11y/no-noninteractive-element-interactions": 0,
    "consistent-return": 0,
    "no-plusplus": 0,
    "prefer-promise-reject-errors": 0,
    "no-useless-escape": 0,
    "react-hooks/exhaustive-deps": 0,
    "no-underscore-dangle": 0,
    "import/prefer-default-export": 0,
    "react/jsx-filename-extension": [
      1,
      {
        "extensions": [".js", ".jsx"]
      }
    ],
    "prettier/prettier": [
      "warn",
      {
        "trailingComma": "es5",
        "singleQuote": false,
        // "printWidth": 100,
        "tabWidth": 2,
        "semi": true,
        "endOfLine": "auto"
      }
    ]
  },
  "plugins": ["prettier", "react", "react-hooks"]
}

```

<!-- CONTACT -->

## Contact

Sumit Saha - [sumit@learnwithsumit.com](mailto:sumit@learnwithsumit.com)

Project Link: [https://github.com/learnwithsumit/think-in-a-react-way](https://github.com/learnwithsumit/think-in-a-react-way)

Youtube Playlist Link: [https://www.youtube.com/playlist?list=PLHiZ4m8vCp9M6HVQv7a36cp8LKzyHIePr](https://www.youtube.com/playlist?list=PLHiZ4m8vCp9M6HVQv7a36cp8LKzyHIePr)

Youtube Channel: [https://youtube.com/LearnwithSumit](https://youtube.com/LearnwithSumit)

<!-- MARKDOWN LINKS & IMAGES -->

[youtube-shield]: https://img.shields.io/badge/-Youtube-black.svg?style=flat-square&logo=youtube&color=555&logoColor=white
[youtube-url]: https://youtube.com/LearnwithSumit
[facebook-shield]: https://img.shields.io/badge/-Facebook-black.svg?style=flat-square&logo=facebook&color=555&logoColor=white
[facebook-url]: https://facebook.com/letslearnwithsumit
[facebook-group-url]: https://facebook.com/groups/learnwithsumit
[instagram-shield]: https://img.shields.io/badge/-Instagram-black.svg?style=flat-square&logo=instagram&color=555&logoColor=white
[instagram-url]: https://instagram.com/learnwithsumit
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/company/learnwithsumit
