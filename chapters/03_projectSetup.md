# How a team can work on a Sass Project

1. Everyone needs to write code with similar formatted, we can take care of that with prettier
2. We dont want to check in our generated code (css) because we will get none meaningful merge conflicts all the time, so we want to ignore those files.
3. Because our css will not be included in our gitub repo, we need a way for Netlify to build our css before it deploys.

## 1. Enforce Team Conventions with Prettier
- [Prettier VSCode Plugin](https://github.com/prettier/prettier-vscode)
- [How to configure prettier in your project](https://prettier.io/docs/en/configuration.html)

Example Prettier Config
```json
{
    "tabWidth": 4,
    "semi": true,
    "singleQuote": true
}
```


## 2. Avoid unmeaningful merge conflicts by git ignoring our generated css

Make a `.gitignore` file which includes our css folder. This file could look like this:
```bash
/scss
```

## 3. Setup Sass Build script for Netlify
In the root of your folder, make a `package.json` file with the following.
```json
{
    "scripts": {
        "build": "node-sass scss/app.scss css/app.css --output-style=compressed"
    },
    "devDependencies": {
        "sass": "^1.25.0"
    }
}

```

Insure that when you setup your site on Netlify, that you specify the build command to be:
```bash
npm run build
```

