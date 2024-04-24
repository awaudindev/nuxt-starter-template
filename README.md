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


<!--
*** Thanks for checking out my repository. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->

<br />
<div align="center">
  <img src="public/pwa-192x192.png" alt="Logo" width="192" height="192">
  <h3>Nuxt 3 Starter Project</h3>
  <p>A journey to improve Frontend development</p>
</div>

## About The Project

This project is a frontend part of integration between mobile apps and php framework data processing.

Here are the link to mobile apps and php framework repository:
* [![Laravel][Laravel-repo]][Laravel-url]
* [![Flutter][Flutter-repo]][Flutter-url]


## Getting Started

### Installation

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

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

please see [CONTRIBUTING.md](CONTRIBUTING.md) for more informatio

## License

Distributed under the MIT License. See `LICENSE` for more information.

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

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/awaudindev/nuxt-starter-template.svg?style=for-the-badge
[contributors-url]: https://github.com/awaudindev/nuxt-starter-template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/awaudindev/nuxt-starter-template.svg?style=for-the-badge
[forks-url]: https://github.com/awaudindev/nuxt-starter-template/network/members
[stars-shield]: https://img.shields.io/github/stars/awaudindev/nuxt-starter-template.svg?style=for-the-badge
[stars-url]: https://github.com/awaudindev/nuxt-starter-template/stargazers
[issues-shield]: https://img.shields.io/github/issues/awaudindev/nuxt-starter-template.svg?style=for-the-badge
[issues-url]: https://github.com/awaudindev/nuxt-starter-templatee/issues
[license-shield]: https://img.shields.io/github/license/awaudindev/nuxt-starter-template.svg?style=for-the-badge
[license-url]: https://github.com/awaudindev/nuxt-starter-template/blob/master/LICENSE.txt
[Laravel-repo]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://github.com/awaudindev/laravel-backend-project
[Flutter-repo]:  https://img.shields.io/badge/Flutter-0468d7?style=for-the-badge&logo=flutter&logoColor=white
[Flutter-url]: https://github.com/awaudindev/Flutter-Simple-Project