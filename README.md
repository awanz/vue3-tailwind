# Vue 3 with Tailwind CSS Installation

## If clone this repo, you must install or update node_module wit command

`npm install`

`npm update`

## Create Vue 3
`vue create vue3-tailwind`

## Install Tailwind use NPM
`npm install tailwindcss`

Create file at `src/assets/styles/tailwind.css` and you fill that

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Open file `src/main.js`

```javascript
import { createApp } from 'vue'
import App from './App.vue'

import '@/assets/styles/tailwind.css';

createApp(App).mount('#app')
```

## Create a Tailwind config file

`npx tailwindcss init`

create file `postcss.config.js` at root with fill

```javascript
module.exports = {
  plugins: [
    // ...
    require('tailwindcss'),
    require('autoprefixer'),
    // ...
  ]
}
```

## Running

`npm run serve`

# If error

`Syntax Error: Error: PostCSS plugin tailwindcss require PostCSS 8.`

## Solve Error with command

`npm install tailwindcss@npm:@tailwindcss/postcss7-compat postcss@^7 autoprefixer@^9`