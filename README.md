# Vue 3 + Vite + prettier + tailwindcss

## Setup steps:

```
fnm use 20
```

```
npm create vite@latest my-vue-app -- --template vue
```

If using WebStorm or any IDE / text editor other than VSCode:
```
rm -rf .vscode
```

```
git init
```

```
touch .nvmrc
echo "20" > .nvmrc
```

```
npm i -D prettier prettier-plugin-tailwindcss
```

Taken from [here](https://gist.github.com/cedric25/93cc8ecbdb4300eabe9c78b2c75cc8b7)
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
