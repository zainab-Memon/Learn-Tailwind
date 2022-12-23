# Learn-Tailwind
- Tailwind CSS makes it quicker to write and maintain the code of your application. 
- By using this utility-first framework, you don't have to write custom CSS to style your application. 
- Instead, you can use utility classes to control the padding, margin, color, font, shadow, and more of your application.
## Install Tailwind CSS
### For Development 
Use the Play CDN to try Tailwind right in the browser without any build step. The Play CDN is designed for development purposes only, and is not the best choice for production.
#### Add the Play CDN script to your HTML
- Add the Play CDN script tag to the <head> of your HTML file, and start using Tailwind’s utility classes to style your content.
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <script src="https://cdn.tailwindcss.com"></script>
  </head>
  <body>
    <nav class="px-4 py-4 bg-purple-900 text-white">
      <ul class="flex">
        <li class="mx-2 cursor-pointer">Home</li>
        <li class="mx-2 cursor-pointer">About</li>
        <li class="mx-2 cursor-pointer">Blog</li>
        <li class="mx-2 cursor-pointer">Contact</li>
      </ul>
    </nav>
  </body>
</html>
```
### For Production
- Installing Tailwind CSS as a PostCSS plugin is the most seamless way to integrate it with build tools like webpack, Rollup, Vite, and Parcel.
#### 1. Install Tailwind 
``` npm install -D tailwindcss postcss autoprefixer ```
- Note: You need to install node.js else this command won't work.
#### 2. Install Vite
``` npm install vite ``` 
#### 3. Make These Changes Into Package.json file 
```json 
{
  "scripts": {
    "start": "vite"
  },
  "devDependencies": {
    "autoprefixer": "^10.4.13",
    "postcss": "^8.4.20",
    "tailwindcss": "^3.2.4"
  },
  "dependencies": {
    "vite": "^4.0.3"
  }
}

```
#### 4. Initialize Tailwind 
```   npx tailwindcss init  ```
- This will create tailwind.config.js file. 
#### 5. Make These Changes Into tailwind.config.js File 
```js 
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["*"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```
- It will reflect that we want to use tailwind for whole content. 
#### 6. Install Extention [Optional But Recommended] 
- Install Tailwind CSS IntelliSense 
