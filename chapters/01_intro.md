# Intro to Sass


## High Level Overview of CSS and JS Trends
- [State of CSS Survey 2019](https://2019.stateofcss.com/)
- [State of JS Survey 2019](https://2019.stateofjs.com/)



## What is Sass?
- [Site for Sass](https://sass-lang.com/)
- [Sassmeister Playground](https://www.sassmeister.com/)


## How to set Sass up
The browser does not understand sass, so we need to convert or compile our sass into normal css. There are a number of ways to do this, the most popular being with NodeJS. If you would like a demo of how to handle your sass compiling with NodeJS, you can watch [this video here](https://www.youtube.com/watch?v=eRv8jUz2FgI).

We are going to use a VSCode plugin called [Live Sass Compiler](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass) to handle the sass compilation.

- [Docs for how to setup Live Sass Compiler](https://github.com/ritwickdey/vscode-live-sass-compiler/blob/master/docs/settings.md)
- [Article on Source Maps](http://thesassway.com/intermediate/using-source-maps-with-sass)

The Sass Live Compiler settings I use in VSCode:
```json
"liveSassCompile.settings.formats": [
    {
      "format": "compressed",
      "extensionName": ".min.css",
      "savePath": "/css/",
    }
  ]
```
