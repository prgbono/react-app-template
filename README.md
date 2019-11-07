# react-app-template

Folder structure for a React app containing several useful tools (linter, prettier and more).

# FILES

In terms of files, the project has a pretty standard HTML5 document, a CSS which applied the HTML and an App.js file where some components are declared.
We're adding a root div. It doesn't have to be called root, just a common practice.
We have two script tags.

- The first is the React library. This library is the interface of how to interact with React; all the methods (except one) will be via this library. It contains no way of rendering itself though; it's just the API.
- The second library is the rendering layer. Since we're rendering to the browser, we're using React DOM. There are other React libraries like React Native, React 360 (formerly React VR), A-Frame React, React Blessed, and others. You need both script tags. The order is not important.
- The last script tag is where we're going to put our code. You don't typically do this but it is the simplest way. This script tag must come after the other two.

# Node.js must be installed.

### TOOLS

All this tools are installed as npm packages. You can see them on package.json devDependencies

# npm

Basic package.json created with npm init

# Prettier

This formats the code consistenly (tabs, spaces, etc). We automatically run it due to package.json scripts tag 'format'. If we want to run it through the command line just type npm run format

We can set up Code for running Prettier each time a file is saved. Install complement Prettier - Code formatter. Once installed, allow these 2 features in Code settings:

- Editor: Format On Save
- Prettier: Require Config

After this we also will need a config file, called '.prettierrc' (all config files contain 'rc') and located at root folder.
Prettier website https://prettier.io/

# Eslint

Find syntax or style errors before execution.

Config file -> .eslintrc.json
We need an extension here because you can confire this in YAML.
Add another script element to the package.json. This one will be called 'lint'. we can always run this script automatically typing npm run lint.

We also use the Code complement ESLint by Dirk Baeumer. This complements let you see what Lint warns you, otherwise you wouldn't know Lint warnings (res underlines)

# Gitignore

# Parcel

This tool has no configuration at all. You only need to point it to index.html file and it discovers all the paths just by figuring everything out. It makes the build and run up a server for the different environments (http://localhost:1234). You can change code and see how affects now dynamically (like '-lcs' option with Ionic).

Also goes to package devDependencies and add another element to package script tag.

# React and ReactDOM libraries

npm install react react-dom
React libraries are dependencies in package.json. This avoids to bring the libraries from a CDN.
After doing this we can delete the script tags on index.html which import these libraries.

Install at this point also the Code complement 'npm Intellisense' by Christian Kohler1, which autocomoplete as you type the possible imports.

# Separate into modules

A file for component. This makes the code more maintainable.
Examples of components: src/Pet.js

### This repository is all extracted from https://github.com/btholt/complete-intro-to-react-v5 by Brian Holt. Thanks Brian for such a great material!
