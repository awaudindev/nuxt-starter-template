# Nuxt 3 Minimal Starter

<!--
*** Thanks for checking out my repository. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

## Setup

Make sure to install the dependencies:

```bash
# npm
npm install

# pnpm
pnpm install

# yarn
yarn install

# bun
bun install
```

# Nuxt CLI (nuxi)

⚡️ [Nuxt](https://nuxt.com/) Generation CLI Experience.

## Commands

All commands are listed on https://nuxt.com/docs/api/commands

```bash
# Generate type stubs
pnpm run prepare

# And run any commands
pnpm nuxi <command>
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev

# pnpm
pnpm run dev

# yarn
yarn dev

# bun
bun run dev
```

## Production

Build the application for production:

```bash
# npm
npm run build

# pnpm
pnpm run build

# yarn
yarn build

# bun
bun run build
```

Locally preview production build:

```bash
# npm
npm run preview

# pnpm
pnpm run preview

# yarn
yarn preview

# bun
bun run preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.

## Features

- 💚 [Nuxt 3](https://nuxt.com/) - SSR, ESR, File-based routing, components auto importing, modules, etc.

- ⚡️ Vite - Instant HMR.

- 🎨 [UnoCSS](https://github.com/unocss/unocss) - The instant on-demand atomic CSS engine.

- 😃 Use icons from any icon sets in Pure CSS, powered by [UnoCSS](https://github.com/unocss/unocss).

- 🔥 The `<script setup>` syntax.

- 🍍 [State Management via Pinia](https://github.com/vuejs/pinia).

- 🦾 TypeScript, of course.

- 📲 [PWA](https://github.com/vite-pwa/nuxt) with offline support and auto-update behavior.

## Plugins

### Nuxt Modules

- [VueUse](https://github.com/vueuse/vueuse) - collection of useful composition APIs.
- [ColorMode](https://github.com/nuxt-modules/color-mode) - dark and Light mode with auto detection made easy with Nuxt.
- [UnoCSS](https://github.com/unocss/unocss) - the instant on-demand atomic CSS engine.
- [Pinia](https://github.com/vuejs/pinia) - intuitive, type safe, light and flexible Store for Vue.
- [VitePWA](https://github.com/vite-pwa/nuxt) - zero-config PWA Plugin for Nuxt 3.
- [DevTools](https://github.com/nuxt/devtools) - unleash Nuxt Developer Experience.

## IDE

recommend using [VS Code](https://code.visualstudio.com/) with [Volar](https://github.com/johnsoncodehk/volar) to get the best experience (You might want to disable [Vetur](https://vuejs.github.io/vetur/) if you have it).

## Pages Structure

```bash

| pages/
---| about.vue
---| index.vue
---| posts/
-----| [id].vue

```

## Layout Structure

```bash

| layouts/
---| home.vue
---| default.vue

```

## Pinia State Management Usage

For more detailed instructions, including [Nuxt configuration](https://pinia.vuejs.org/ssr/nuxt.html#nuxt-js), check the [Documentation](https://pinia.vuejs.org).

### Create a Store

You can create as many stores as you want, and they should each exist in different files:

```ts
import { defineStore } from 'pinia'

// main is the name of the store. It is unique across your application
// and will appear in devtools
export const useMainStore = defineStore('main', {
  // a function that returns a fresh state
  state: () => ({
    counter: 0,
    name: 'Eduardo',
  }),
  // optional getters
  getters: {
    // getters receive the state as first parameter
    doubleCounter: (state) => state.counter * 2,
    // use getters in other getters
    doubleCounterPlusOne(): number {
      return this.doubleCounter + 1
    },
  },
  // optional actions
  actions: {
    reset() {
      // `this` is the store instance
      this.counter = 0
    },
  },
})
```

`defineStore` returns a function that has to be called to get access to the store: