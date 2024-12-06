# Instalasi dan Konfigurasi Tailwind CSS

Framework CSS Utility-first yang terdapat banyak class yang bisa digunakan

## Pre requisite

- VSCode
- Extension:
  - Tailwind CSS Intellisense
  - Live preview
  - PostCSS laanguage support
- NPM (Node.JS)
- Terminal

http://tailwindcss.com

## CDN (Content Deliverry Network)

Tinggal pasang tag script berikut di bagian head.

```html
<script src="https://cdn.tailwindcss.com"></script>
```

## Tailwind CLI

Inisialisasi file npm

```sh
npm init -y
```

Akan terbuat sebuah file package.json

```sh
npm install -D tailwindcss postcss autoprefixer
```

```sh
npx tailwindcss init
```

tailwind.config.js

```js
module.exports = {
  content: ["./public/**/*.{html, js}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

input.css

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Build tailwindcss

```sh
npx tailwindcss -i ./src/css/input.css -o ./public/css/output.css --watch
```

Tambahin di bagian head

```html
<link href="public/css/output.css" rel="stylesheet" />
```
