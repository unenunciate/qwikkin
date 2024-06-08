# Qwikkin

**Qwikkin** is a free and open-source template to make your website using **[Qwik](https://qwik.builder.io/) + [Tailwind CSS](https://tailwindcss.com/)** and hosting via **[KinodeOS](https://kinode.org/)** node for the frontend presentation for a KinodeOS application. Ready to start a new project and designed taking into account best practices.

## Features

- ✅ Integration with **Tailwind CSS** supporting **Dark mode**
- ✅ Integration with **Farcaster Frames** and **ReFrame** expansion
- ✅ Integration with **Coinbase Smart Wallet**, **OnChainKit**, and **Base**
- ✅ Integration with **SIWE**
- ✅ Integration with **Ceramic Network** and **OrbisDB**
- ✅ Basic Implementation of **ClientDB**
- ✅ Backwards compatiblity with traditional link previews and handling via public gateway

<br>

//To Do: Screenshot

<img src="./screenshot.jpg" alt="Qwikkin Theme Screenshot">

//To Do: Logos/License/Contribuations/Know Issues

[![onWidget](https://custom-icon-badges.demolab.com/badge/made%20by%20-onWidget-556bf2?style=flat-square&logo=onwidget&logoColor=white&labelColor=101827)](https://onwidget.com)
[![License](https://img.shields.io/github/license/onwidget/qwind?style=flat-square&color=dddddd&labelColor=000000)](https://github.com/onwidget/qwind/blob/main/LICENSE.md)
[![Maintained](https://img.shields.io/badge/maintained%3F-yes-brightgreen.svg?style=flat-square)](https://github.com/onwidget)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat-square)](https://github.com/onwidget/qwind#contributing)
[![Known Vulnerabilities](https://snyk.io/test/github/onwidget/qwind/badge.svg?style=flat-square)](https://snyk.io/test/github/onwidget/qwind)

<br>

<details open>
<summary>Table of Contents</summary>

- [Demo](#demo)
- [Getting started](#getting-started)
  - [Project structure](#project-structure)
  - [Commands](#commands)
  - [Configuration](#configuration)
  - [Deploy](#deploy)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [Acknowledgements](#acknowledgements)
- [License](#license)

</details>

<br>

## Demo

📌 [https://qwikkin.unenunciate.com/](https://qwikkin.unenunciate.com/)

<br>

## Getting started

This project is using Qwik with [QwikCity](https://qwik.builder.io/qwikcity/overview/). QwikCity is just a extra set of tools on top of Qwik to make it easier to build a full site, including directory-based routing, layouts, and more.

### Project structure

Inside **Qwikkin** template, you'll see the following folders and files:

```
/
├── adaptors/
|   └── static/
|       └── vite.config.ts
├── public/
│   ├── favicon.svg
│   ├── manifest.json
│   └── robots.txt
├── src/
│   ├── assets/
│   │   ├── images/
|   |   └── styles/
|   |       └── global.css
│   ├── components/
│   │   ├── atoms/
│   │   ├── core/
│   │   ├── icons/
|   |   └── widgets/
|   |       ├── Hero.tsx
|   |       ├── Features.tsx
|   |       └── ...
│   ├── content/
│   |   └── blog/
│   |       ├── post-slug-1.md
│   |       ├── post-slug-2.md
│   |       └── ...
│   ├── routes/
│   |   ├── blog/
│   |   ├── index.tsx
|   |   ├── layout.tsx
|   |   ├-- service-worker.ts
│   |   └-- ...
│   ├── config.mjs
│   ├── entry.dev.tsx
│   ├── entry.preview.tsx
│   ├── entry.ssr.tsx
│   └── root.tsx
├── package.json
└── ...
```

- `src/routes`: Provides the directory based routing, which can include a hierarchy of `layout.tsx` layout files, and an `index.tsx` file as the page. Additionally, `index.ts` files are endpoints. Please see the [routing docs](https://qwik.builder.io/qwikcity/routing/overview/) for more info.

- `src/components`: Recommended directory for components.

- `public`: Any static assets, like images, can be placed in the public directory. Please see the [Vite public directory](https://vitejs.dev/guide/assets.html#the-public-directory) for more info.

//To Do: Make a CodeSandbox if possible with KinodeOS

[![Edit Qwikkin on CodeSandbox](https://codesandbox.io/static/img/play-codesandbox.svg)](https://githubbox.com/onwidget/qwind/tree/main)

> **Seasoned qwik expert?** Delete this file. Update `config.mjs` and contents. Have fun!

<br>

//To Do: Add Yarn + Add Kinode Commands

### Commands

All commands are run from the root of the project, from a terminal:

| Command            | Action                                         |
| :----------------- | :--------------------------------------------- |
| `npm install`      | Installs dependencies                          |
| `npm run dev`      | Starts local dev server at `127.0.0.1:5173/`   |
| `npm run build`    | Build your production site to `./dist/`        |
| `npm run preview`  | Preview your build locally, before deploying   |
| `npm run fmt`      | Format codes with Prettier                     |
| `npm run lint`     | Run Eslint                                     |
| `npm run qwik ...` | Run CLI commands like `qwik add`, `qwik build` |

<br>

### Configuration

//To Do: Define config properties

Basic configuration file: `./src/config.mjs`

```javascript
export const SITE = {
  name: "Example",

  origin: "https://example.com",
  basePathname: "/", // Change this if you need to deploy to Github Pages, for example
  trailingSlash: true, // Generate permalinks with or without "/" at the end
};
```

<br>

### Deploy

//TO DO: All Instructions

#### Deploy to Devlopment Enviorment 



#### Deploy KinodeOS Application



#### Deploy KinodeOS Node & Installing KinodeOS Application (via Kinode Vallet)



#### Deploy KinodeOS Node as Public Application Gateway (via AWS)

You can create an optimized production build with:

```shell
npm run build //TO DO
```

Now, your website is ready to be deployed. All generated files are located at
`dist` folder, which you can deploy the folder to any hosting service you
prefer.

<br>

## Roadmap

### Base

- [ ] Create utilities to generate permalinks tailored to the domain and base pathname.
- [ ] Create utilities to generate IPFS pinned Farcaster Frames tailored to context and user customizations.
- [ ] Create utilities to enable switching between media content's hosting location (Traditional Cloud  Vs. dStorage [IPFS/Storj] + dDistrobution [Crust Network])
- [ ] Create basic context system for referencing elements of content
- [ ] Create basic context system visualization
- [ ] Create component to enable building sharing frames and contextual frames via client
- [ ] Create configurable blog with categories, tags and authors using MDX
- [ ] Authentication via SIWE and Coinbase Smart Wallet
- [ ] Add more frequently used pages (About, Services, Contact, Docs ...)
- [ ] Inital ClientDB intergration
- [ ] Link previews, frame portal, and IPFS Gateway via hosted domain utilized for backwards compatiablity to resolve frames stored on IPFS without the link's frontend client requiring special handling (URL format: https://domain.example/frame-portal/:CID)

### Advanced

- [ ] Create component to enable building custom frames via client
- [ ] Create multimedia context system
- [ ] Sitemap and SEO Improvements
- [ ] ClientDB Basic Fog of Data Optimization
- [ ] Utilize Oasis OPL Layer in Attributation system
- [ ] Create advanaced visualization of context system
- [ ] Add Multi-tab Service Work Leader Elections
- [ ] ClientDB Advanced Fog of Data Optimization and Service worker optimization
- [ ] Define a KinodeOS mode for operating as centralized public gateway and service still as a KinodeOS app
- [ ] Admin backend for operating as centralized public platform
- [ ] Traui Desktop Application
- [ ] ClientDB Traui Intergration
- [ ] Mobile Application and ClientDB SQLite

<br>

## Contributing

If you have any idea, suggestions or find any bugs, feel free to open a discussion, an issue or create a pull request.
That would be very useful for all of us and we would be happy to listen and take action.

## Acknowledgements

Initially created and maintained by [Unenunciate](https://unenunciate.com) [X](https://x.com/unenunciate)

## License

**Qwikkin** is licensed under the MIT license — see the [LICENSE](https://github.com/unenunciate/qwikkin/blob/main/LICENSE.md) file for details.
