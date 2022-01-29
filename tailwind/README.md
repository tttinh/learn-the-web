# Tailwind

How to setup a vanilla HTML/CSS/Javascript web project with TailwindCSS.

## Environment

Node version: v14.17.1

NPM version: 6.14.13

## Setup

Initialize project with Vite `vanilla` template.

```
$ npm init vite@latest tailwind --template vanilla
```

Install tailwindcss and its peer dependencies via npm, and then run the init command to generate both `tailwind.config.js` and `postcss.config.js`.

```
$ npm install -D tailwindcss@latest postcss@latest autoprefixer@latest
$ npx tailwindcss init -p
```

Add the paths to all of your template files in your `tailwind.config.js` file.

```
module.exports = {
  content: ['./index.html', './main.js'],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

Update the `style.css` file

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Now start development

```
npm install
npm run dev
```
