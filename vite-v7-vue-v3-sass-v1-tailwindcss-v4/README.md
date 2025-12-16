# Vite v7 (with TypeScript) + Vue v3 + Sass v1 + TailwindCSS v4

This template is a Vite-based Vue project using TypeScript, with Sass and TailwindCSS employed for styling.

TailwindCSS v4 no longer supports preprocessors, so Sass can only be used side-by-side. They do not work together when integrated. This limitation inspired the creation of the template, providing a very small example for demonstration purposes.

## Create yourself

```none
pnpm create vite@latest {project_name} -- --template vue-ts
cd {project_name}
pnpm i -D sass@1 tailwindcss@4 @tailwindcss/vite
```

It may be necessary to perform some configuration in addition to installing the dependencies.

**vite.config.ts**
```diff
  import { defineConfig } from 'vite'
  import vue from '@vitejs/plugin-vue'
+ import tailwindcss from '@tailwindcss/vite'
  
  // https://vite.dev/config/
  export default defineConfig({
    plugins: [
      vue(),
+     tailwindcss(),
    ],
  })
```

**./src/tailwind.css** (NEW)
```css
@import "tailwindcss";
```

**./src/styles.scss** (RENAMED from **style.css**)
```css
/* Your SCSS code here; without TailwindCSS */
```

**./src/main.ts**
```diff
  import { createApp } from 'vue'
- import './style.css'
+ import './style.scss'
+ import './tailwind.css'
  import App from './App.vue'
  
  createApp(App).mount('#app')
```

**./package.json**
```diff
  {
+   "imports": {
+     "#tailwind.css": "./src/tailwind.css"
+   },
  }
```

Make sure that Sass code never references TailwindCSS classes, and TailwindCSS code never references Sass classes or variables. These are separate, isolated code sections.
