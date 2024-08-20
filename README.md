# IceT.js

![iceT logo](public/iceT.png)

A full stack Nuxt web app template configured with pnpm, Vitest, and TailwindCSS. The example app shown here is a basic calculator app, however other apps can be created to the user's liking.

## Instructions

1. Go to StackBlitz
2. Create a new Nuxt project
3. npm install -g pnpm
4. pnpm add --save-dev @nuxtjs/tailwindcss
5. pnpm add -D vitest
6. Optional: pnpm i image (if the user need images in the app)
7. Optional: pnpm i @nuxt/fonts (to use a variety of cool fonts)
8. Add this to nuxt.config.ts
```ts
modules: [
  '@nuxtjs/tailwindcss',
  '@nuxt/fonts', // optional
  '@nuxt/image', // optional
]
```
9. Copy the code from this Github repo's package.json, remove the old code from the StackBlitz project's package.json, and paste in the repo's code
10. Create tailwind.config.js and add this (user can adjust colors as needed):
```js
import colors from 'tailwindcss/colors'

export default {
  theme: {
    extend: {
      colors: {
        'hot-pink': "#E3346F",
        'light-pink': "#F798B1",
        'dark-magenta': "#90354E",
        'dark-grape': "#512D34",
        'pumpkin': "#CD7230",
        'pea-green': "#88A849",
      }
    }
  }
}
```
11. Copy the code from the repo's app.vue, remove the StackBlitz project's app.vue code, and paste the repo's Vue code in
12. The website should be up and running! (you may need to save and refresh the project to load the custom colors)


## Vitest setup

For information on how to use Vitest, visit [this link](https://vitest.dev/guide/) and skip to the "Writing Tests" section

![coding signature](public/sig.jpeg)
