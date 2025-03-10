# 🚀 Deploy React App to GitHub Pages

1️⃣ Install gh-pages package:

````bash
npm install gh-pages --save-dev
````

2️⃣ Update package.json:

Add the following fields to your package.json:

````json
{
  "homepage": "https://<your-github-username>.github.io/<repository-name>",
  "scripts": {
    "predeploy": "npm run build",
    "deploy": "gh-pages -d dist”
  }
}
````

Notice that build is changed to dist because Vite outputs production files in dist/ by default.

````json
"homepage": "https://ImperviousDeveloper.github.io/url-shortner-react",
````

3️⃣ Update vite.config.js (Set base path for GitHub Pages):

````javascript
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';

export default defineConfig({
  plugins: [react()],
  base: '/url-shortner-react/', // <-- Important for GitHub Pages subpath
});
````

4️⃣ Deploy:

````bash
npm run deploy
````

This will build your project and deploy the contents of the build folder to the gh-pages branch.

## ✅ Solutions to Fix Image Path Issue

### Option 1: Use import for Static Images

The recommended approach with Vite and React is importing the image like this:

````jsx
import img2 from '/images/img2.png';

<motion.img
  initial={{ opacity: 0 }}
  whileInView={{ opacity: 1 }}
  viewport={{ once: true }}
  transition={{ duration: 0.8 }}
  className="sm:w-[480px] w-[400px] object-cover rounded-md"
  src={img2}
  alt="Demo Image"
/>
````

### Option 2: Use base Path in vite.config.js

Ensure that your vite.config.js has the correct base for GitHub Pages:

````javascript
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';

export default defineConfig({
  plugins: [react()],
  base: '/url-shortner-react/', // <-- Adjust this to your repo name
});
````

Then in your component:

````jsx
<motion.img
  initial={{ opacity: 0 }}
  whileInView={{ opacity: 1 }}
  viewport={{ once: true }}
  transition={{ duration: 0.8 }}
  className="sm:w-[480px] w-[400px] object-cover rounded-md"
  src={`${import.meta.env.BASE_URL}images/img2.png`}
  alt="Demo Image"
/>
````

- How import.meta.env.BASE_URL Works

When you set base: '/url-shortner-react/', import.meta.env.BASE_URL will be /url-shortner-react/, so it dynamically handles the path for both:

- Local development → /
- GitHub Pages → /url-shortner-react/
