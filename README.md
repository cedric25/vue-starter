# Vue + vite + prettier + tailwindcss

## How to use

The easiest is to click on "Use this template" on the top right of this page.

### or Manual cloning

 - Clone this project

```
// https
git clone https://github.com/cedric25/vue-starter.git my-vue-app
// ssh
git clone git@github.com:cedric25/vue-starter.git my-vue-app
cd my-vue-app
nvm use / fnm use / etc.
npm i
```

 - Remove git history and create your own:
```
rm -rf .git
git init
git add .
git commit -m ":zap: Init project"
```

 - Run app
```
npm run dev  
```

## Setup steps

### Node version

```
fnm use 20
```

### Create project with vite

```
npm create vite@latest my-vue-app -- --template vue
```

### Some cleanup

If using WebStorm or any IDE / text editor other than VSCode:
```
rm -rf .vscode
```

### git init

```
git init
```

### Set node version

```
touch .nvmrc
echo "20" > .nvmrc
```

### prettier

```
npm i -D prettier prettier-plugin-tailwindcss
```

Configuration taken from [here](https://gist.github.com/cedric25/93cc8ecbdb4300eabe9c78b2c75cc8b7)
```
touch .prettierrc.cjs
echo "module.exports = {
  arrowParens: 'avoid',
  printWidth: 100,
  semi: false,
  singleQuote: true,
  tabWidth: 2,
  trailingComma: 'es5',
}" > .prettierrc.cjs
```

### tailwind

```
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

Put this into `tailwind.config.js`:
```
content: [
  "./index.html",
  "./src/**/*.{vue,js,ts,jsx,tsx}",
],
``` 

Replace `style.css`:
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```
