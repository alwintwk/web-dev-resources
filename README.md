<h1 align="center">Web development resources</h1>
<p align="center"><i>A curated list of open source frameworks, tools, and resources for modern web development.</i></p>
<p align="center">Inspired by <a href="https://github.com/milanaryal/web-development-resources">milanaryal/web-development-resources</a>. Last reviewed: September 2026.<br />New to the terms? See the companion glossary <a href="https://github.com/alwintwk/dev-knowledge">dev-knowledge</a>.<br /><a href="https://alwintwk.github.io/web-dev-resources/">Search it online</a></p>

## Table of contents

* [Learning & references](#learning--references)
* [UI frameworks](#ui-frameworks)
* [Meta-frameworks](#meta-frameworks)
* [Static sites & docs](#static-sites--docs)
* [Headless CMS](#headless-cms)
* [CSS frameworks & styling](#css-frameworks--styling)
* [Component libraries](#component-libraries)
* [Headless / unstyled components](#headless--unstyled-components)
* [State & data fetching](#state--data-fetching)
* [Forms & validation](#forms--validation)
* [Routing](#routing)
* [Animation](#animation)
* [3D, canvas & graphics](#3d-canvas--graphics)
* [Charts, maps & diagrams](#charts-maps--diagrams)
* [Icons](#icons)
* [Fonts & typography](#fonts--typography)
* [Accessibility](#accessibility)
* [Runtimes & version managers](#runtimes--version-managers)
* [Package managers & monorepos](#package-managers--monorepos)
* [Build tools & bundlers](#build-tools--bundlers)
* [Languages & compilers](#languages--compilers)
* [Linting & formatting](#linting--formatting)
* [Testing](#testing)
* [Backend frameworks](#backend-frameworks)
* [APIs, RPC & realtime](#apis-rpc--realtime)
* [Databases, ORMs & search](#databases-orms--search)
* [Auth](#auth)
* [Backend as a service](#backend-as-a-service)
* [Hosting & deployment](#hosting--deployment)
* [CDNs](#cdns)
* [Analytics & monitoring](#analytics--monitoring)
* [Mobile & desktop](#mobile--desktop)
* [Images & media](#images--media)
* [Performance & browser support](#performance--browser-support)
* [Placeholders & mock data](#placeholders--mock-data)
* [SEO, favicons & meta](#seo-favicons--meta)
* [Lists of lists](#lists-of-lists)

---

## Learning & references

| Name | Description |
|---|---|
| [MDN Web Docs](https://developer.mozilla.org/) | The reference for HTML, CSS, JavaScript, and Web APIs. |
| [web.dev](https://web.dev/) | Google's guides on modern web capabilities, performance, and Baseline. |
| [javascript.info](https://javascript.info/) | The Modern JavaScript Tutorial, from basics to advanced topics. |
| [Eloquent JavaScript](https://eloquentjavascript.net/) | Free book on JavaScript and programming. |
| [You Don't Know JS](https://github.com/getify/You-Dont-Know-JS) | Free book series on how JavaScript really works. |
| [The Odin Project](https://www.theodinproject.com/) | Free open source full-stack curriculum. |
| [Full Stack Open](https://fullstackopen.com/en/) | University of Helsinki's free course on React, Node, and more. |
| [freeCodeCamp](https://www.freecodecamp.org/) | Free interactive coding lessons and certifications. |
| [Frontend Mentor](https://www.frontendmentor.io/) | Real-world front-end challenges with designs. |
| [Exercism](https://exercism.org/) | Free coding practice with mentoring in 70+ languages. |
| [patterns.dev](https://www.patterns.dev/) | Design, rendering, and performance patterns for web apps. |
| [roadmap.sh](https://roadmap.sh/) | Community-made learning roadmaps for developers. |
| [CSS-Tricks](https://css-tricks.com/) | Articles and almanac for CSS and front-end. |
| [Josh W. Comeau](https://www.joshwcomeau.com/) | In-depth interactive articles on CSS and React. |
| [Smashing Magazine](https://www.smashingmagazine.com/) | Articles on web design and development. |
| [Web Almanac](https://almanac.httparchive.org/) | Yearly report on the state of the web, backed by real data. |
| [W3C standards](https://www.w3.org/standards/) | Official web standards. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## UI frameworks

| Name | Description |
|---|---|
| [React](https://react.dev/) | Library for building user interfaces from components. |
| [Vue](https://vuejs.org/) | Progressive, approachable framework for building UIs. |
| [Svelte](https://svelte.dev/) | Compiler-based framework with runes-based reactivity. |
| [Angular](https://angular.dev/) | Full-featured framework by Google with signals and SSR. |
| [Solid](https://www.solidjs.com/) | Fine-grained reactive UI library with JSX. |
| [Preact](https://preactjs.com/) | Fast 3kB alternative to React with the same API. |
| [Qwik](https://qwik.dev/) | Resumable framework for instant-loading apps. |
| [Lit](https://lit.dev/) | Simple library for building fast Web Components. |
| [Stencil](https://stenciljs.com/) | Compiler for reusable Web Components. |
| [Ember](https://emberjs.com/) | Convention-over-configuration framework for ambitious apps. |
| [Marko](https://markojs.com/) | Streaming-first UI language by eBay. |
| [Mithril](https://mithril.js.org/) | Tiny framework with routing and XHR built in. |
| [Alpine.js](https://alpinejs.dev/) | Lightweight JavaScript for sprinkling behavior into HTML. |
| [htmx](https://htmx.org/) | Access AJAX, WebSockets, and more directly from HTML attributes. |
| [Hotwire](https://hotwired.dev/) | HTML-over-the-wire: Turbo and Stimulus. |
| [Datastar](https://data-star.dev/) | Hypermedia framework combining backend-driven HTML and signals. |
| [Leptos](https://leptos.dev/) | Full-stack web framework in Rust. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Meta-frameworks

> Concepts behind this: [dev-knowledge → CSR vs SSR vs SSG](https://github.com/alwintwk/dev-knowledge#csr-vs-ssr-vs-ssg)

| Name | Works with | Description |
|---|---|---|
| [Next.js](https://nextjs.org/) | React | React framework with routing, SSR, and server components. |
| [React Router (framework mode)](https://reactrouter.com/) | React | Full-stack React framework (successor to Remix). |
| [TanStack Start](https://tanstack.com/start) | React, Solid | Full-stack framework built on TanStack Router. |
| [Waku](https://waku.gg/) | React | Minimal React framework with server components. |
| [Vike](https://vike.dev/) | React, Vue, Solid | Flexible Vite-based framework, bring your own tools. |
| [Gatsby](https://www.gatsbyjs.com/) | React | Static-first React framework with a data layer. |
| [Nuxt](https://nuxt.com/) | Vue | Full-stack Vue framework. |
| [SvelteKit](https://svelte.dev/docs/kit) | Svelte | Official full-stack Svelte framework. |
| [SolidStart](https://start.solidjs.com/) | Solid | Full-stack Solid framework. |
| [Analog](https://analogjs.org/) | Angular | Full-stack Angular meta-framework powered by Vite. |
| [Fresh](https://fresh.deno.dev/) | Preact | Deno framework with islands and zero JS by default. |
| [Astro](https://astro.build/) | Any | Content-driven framework with islands; use any UI library. |
| [Wasp](https://wasp.sh/) | React + Node | Full-stack framework with auth, jobs, and DB built in. |
| [Inertia.js](https://inertiajs.com/) | React, Vue, Svelte | Build SPAs with classic server routing (Laravel, Rails). |
| [Livewire](https://livewire.laravel.com/) | Laravel | Dynamic UIs in PHP without writing JavaScript. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Static sites & docs

| Name | Description |
|---|---|
| [Eleventy](https://www.11ty.dev/) | Simple, flexible static site generator. |
| [Hugo](https://gohugo.io/) | Very fast static site generator written in Go. |
| [Jekyll](https://jekyllrb.com/) | Blog-aware static site generator, powers GitHub Pages. |
| [Zola](https://www.getzola.org/) | Single-binary static site generator in Rust. |
| [Hexo](https://hexo.io/) | Fast blog framework powered by Node.js. |
| [Starlight](https://starlight.astro.build/) | Documentation site framework built on Astro. |
| [VitePress](https://vitepress.dev/) | Vite and Vue powered static site generator for docs. |
| [Docusaurus](https://docusaurus.io/) | React-based documentation websites by Meta. |
| [Nextra](https://nextra.site/) | Docs and blog framework built on Next.js. |
| [Fumadocs](https://fumadocs.dev/) | Flexible documentation framework for Next.js. |
| [Rspress](https://rspress.rs/) | Fast docs generator built on Rsbuild. |
| [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) | Popular Python-based documentation theme. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Headless CMS

| Name | Description |
|---|---|
| [Payload](https://payloadcms.com/) | TypeScript CMS and app framework that lives inside Next.js. |
| [Strapi](https://strapi.io/) | Leading open source headless CMS. |
| [Directus](https://directus.io/) | Instant API and admin app on top of any SQL database. |
| [Keystatic](https://keystatic.com/) | Content stored in Markdown/JSON files in your repo. |
| [TinaCMS](https://tina.io/) | Git-backed CMS with visual editing. |
| [Decap CMS](https://decapcms.org/) | Git-based CMS for static site generators (formerly Netlify CMS). |
| [Ghost](https://ghost.org/) | Publishing platform for blogs and newsletters. |
| [WordPress](https://wordpress.org/) | The classic CMS, usable headless via its REST API. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## CSS frameworks & styling

| Name | Description |
|---|---|
| [Tailwind CSS](https://tailwindcss.com/) | Utility-first CSS framework. |
| [Bootstrap](https://getbootstrap.com/) | Classic component-based HTML, CSS, and JS framework. |
| [Bulma](https://bulma.io/) | Modern CSS framework based on Flexbox. |
| [Foundation](https://get.foundation/) | Responsive front-end framework for sites and emails. |
| [UIkit](https://getuikit.com/) | Lightweight, modular front-end framework. |
| [UnoCSS](https://unocss.dev/) | Instant on-demand atomic CSS engine. |
| [Pico CSS](https://picocss.com/) | Minimal CSS framework for semantic HTML. |
| [Simple.css](https://simplecss.org/) | Classless CSS that makes plain HTML look nice. |
| [Water.css](https://watercss.kognise.dev/) | Drop-in classless CSS. |
| [Open Props](https://open-props.style/) | Supercharged CSS custom properties (design tokens). |
| [Panda CSS](https://panda-css.com/) | Build-time CSS-in-JS with type safety. |
| [StyleX](https://stylexjs.com/) | Meta's compile-time atomic styling system. |
| [vanilla-extract](https://vanilla-extract.style/) | Zero-runtime, type-safe stylesheets in TypeScript. |
| [styled-components](https://styled-components.com/) | CSS-in-JS for React with tagged template literals. |
| [Emotion](https://emotion.sh/) | Performant, flexible CSS-in-JS library. |
| [CSS Modules](https://github.com/css-modules/css-modules) | Locally scoped class names by default. |
| [Sass](https://sass-lang.com/) | Mature CSS preprocessor. |
| [Less](https://lesscss.org/) | Backwards-compatible CSS preprocessor. |
| [PostCSS](https://postcss.org/) | Tool for transforming CSS with JavaScript plugins. |
| [Lightning CSS](https://lightningcss.dev/) | Extremely fast CSS parser, transformer, and minifier. |
| [Modern Normalize](https://github.com/sindresorhus/modern-normalize) | Normalize browser default styles. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Component libraries

| Name | Works with | Description |
|---|---|---|
| [shadcn/ui](https://ui.shadcn.com/) | React | Copy-paste components built on Radix/Base UI and Tailwind. |
| [HeroUI](https://www.heroui.com/) | React | Beautiful Tailwind-based components (formerly NextUI). |
| [MUI](https://mui.com/) | React | React components implementing Material Design. |
| [Mantine](https://mantine.dev/) | React | Full-featured React components and hooks library. |
| [Chakra UI](https://chakra-ui.com/) | React | Accessible React component system. |
| [Ant Design](https://ant.design/) | React | Enterprise-class React UI library. |
| [Fluent UI](https://github.com/microsoft/fluentui) | React, Web Components | Microsoft's design system. |
| [Carbon](https://carbondesignsystem.com/) | React, Web Components | IBM's open source design system. |
| [Tremor](https://www.tremor.so/) | React | Components for charts and dashboards. |
| [Magic UI](https://magicui.design/) | React | Animated components for landing pages. |
| [shadcn-vue](https://www.shadcn-vue.com/) | Vue | Vue port of shadcn/ui. |
| [Vuetify](https://vuetifyjs.com/) | Vue | Material Design component framework for Vue. |
| [PrimeVue](https://primevue.org/) | Vue | Rich UI component suite for Vue. |
| [Element Plus](https://element-plus.org/) | Vue | Desktop-focused Vue 3 component library. |
| [Naive UI](https://www.naiveui.com/) | Vue | Themeable Vue 3 components in TypeScript. |
| [Quasar](https://quasar.dev/) | Vue | Vue framework for web, mobile, and desktop from one codebase. |
| [shadcn-svelte](https://www.shadcn-svelte.com/) | Svelte | Svelte port of shadcn/ui. |
| [Skeleton](https://www.skeleton.dev/) | Svelte, React | Adaptive design system with Tailwind. |
| [Angular Material](https://material.angular.dev/) | Angular | Material Design components for Angular. |
| [PrimeNG](https://primeng.org/) | Angular | Rich UI component suite for Angular. |
| [NG-ZORRO](https://ng.ant.design/) | Angular | Ant Design for Angular. |
| [Spartan](https://www.spartan.ng/) | Angular | shadcn-style accessible Angular components. |
| [daisyUI](https://daisyui.com/) | Any (Tailwind) | Component classes plugin for Tailwind CSS. |
| [Flowbite](https://flowbite.com/) | Any (Tailwind) | Tailwind components with framework integrations. |
| [Preline UI](https://preline.co/) | Any (Tailwind) | Tailwind components and examples. |
| [Web Awesome](https://webawesome.com/) | Any | Framework-agnostic Web Components (successor to Shoelace). |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Headless / unstyled components

| Name | Works with | Description |
|---|---|---|
| [Radix Primitives](https://www.radix-ui.com/primitives) | React | Unstyled, accessible components. |
| [Base UI](https://base-ui.com/) | React | Unstyled components from the Radix, MUI, and Floating UI teams. |
| [React Aria](https://react-spectrum.adobe.com/react-aria/) | React | Adobe's accessible UI primitives and hooks. |
| [Headless UI](https://headlessui.com/) | React, Vue | Unstyled components by the Tailwind team. |
| [Ark UI](https://ark-ui.com/) | React, Vue, Solid, Svelte | Headless components powered by state machines. |
| [Zag](https://zagjs.com/) | Any | Framework-agnostic UI component state machines. |
| [Reka UI](https://reka-ui.com/) | Vue | Unstyled, accessible Vue components (formerly Radix Vue). |
| [Bits UI](https://bits-ui.com/) | Svelte | Headless components for Svelte. |
| [Kobalte](https://kobalte.dev/) | Solid | Accessible, unstyled Solid components. |
| [Floating UI](https://floating-ui.com/) | Any | Positioning for tooltips, popovers, and dropdowns. |
| [TanStack Table](https://tanstack.com/table) | Any | Headless tables and datagrids. |
| [TanStack Virtual](https://tanstack.com/virtual) | Any | Virtualize long lists at 60 FPS. |
| [dnd kit](https://dndkit.com/) | React | Lightweight drag-and-drop toolkit. |
| [cmdk](https://cmdk.paco.me/) | React | Fast, composable command menu. |
| [Sonner](https://sonner.emilkowal.ski/) | React | Opinionated toast notifications. |
| [Downshift](https://github.com/downshift-js/downshift) | React | Accessible autocomplete, combobox, and select. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## State & data fetching

| Name | Works with | Description |
|---|---|---|
| [TanStack Query](https://tanstack.com/query) | React, Vue, Solid, Svelte, Angular | Server-state fetching, caching, and syncing. |
| [TanStack DB](https://tanstack.com/db) | Any | Reactive client store for sync-first apps. |
| [SWR](https://swr.vercel.app/) | React | Data fetching with stale-while-revalidate. |
| [Apollo Client](https://www.apollographql.com/docs/react) | React | GraphQL client with caching. |
| [urql](https://github.com/urql-graphql/urql) | React, Vue, Svelte | Lightweight, extensible GraphQL client. |
| [Zustand](https://zustand.docs.pmnd.rs/) | React | Small, fast state management. |
| [Jotai](https://jotai.org/) | React | Primitive, flexible atomic state. |
| [Valtio](https://valtio.dev/) | React | Proxy-based state that feels like mutation. |
| [Redux Toolkit](https://redux-toolkit.js.org/) | Any | Official, batteries-included Redux (includes RTK Query). |
| [MobX](https://mobx.js.org/) | Any | Simple, scalable observable state. |
| [Legend-State](https://github.com/LegendApp/legend-state) | React | Fast signal-based state with sync. |
| [Pinia](https://pinia.vuejs.org/) | Vue | Intuitive store for Vue. |
| [NgRx](https://ngrx.io/) | Angular | Reactive state management for Angular. |
| [XState](https://stately.ai/docs/xstate) | Any | State machines and actors for complex logic. |
| [Preact Signals](https://github.com/preactjs/signals) | Preact, React | Fine-grained reactive signals. |
| [Nano Stores](https://github.com/nanostores/nanostores) | Any | Tiny framework-agnostic state manager. |
| [nuqs](https://nuqs.dev/) | React | Type-safe state stored in the URL query string. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Forms & validation

| Name | Works with | Description |
|---|---|---|
| [React Hook Form](https://react-hook-form.com/) | React | Performant forms with easy validation. |
| [TanStack Form](https://tanstack.com/form) | React, Vue, Solid, Svelte, Angular | Headless, type-safe form state. |
| [Conform](https://conform.guide/) | React | Progressive-enhancement forms for server actions. |
| [Formik](https://formik.org/) | React | Classic React form library. |
| [VeeValidate](https://vee-validate.logaretm.com/) | Vue | Form validation for Vue. |
| [FormKit](https://formkit.com/) | Vue | Form framework with inputs, validation, and schema. |
| [Superforms](https://superforms.rocks/) | SvelteKit | Server and client form validation. |
| [Zod](https://zod.dev/) | Any | TypeScript-first schema validation. |
| [Valibot](https://valibot.dev/) | Any | Modular, tiny schema validation library. |
| [ArkType](https://arktype.io/) | Any | TypeScript's 1:1 validator, optimized from editor to runtime. |
| [Yup](https://github.com/jquense/yup) | Any | Long-standing schema builder for validation. |
| [Standard Schema](https://standardschema.dev/) | Any | Common interface shared by Zod, Valibot, ArkType, and others. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Routing

| Name | Works with | Description |
|---|---|---|
| [TanStack Router](https://tanstack.com/router) | React, Solid | Fully type-safe router. |
| [React Router](https://reactrouter.com/) | React | Declarative routing for React. |
| [Wouter](https://github.com/molefrog/wouter) | React, Preact | Minimalist 2kB router. |
| [Vue Router](https://router.vuejs.org/) | Vue | Official router for Vue. |
| [Solid Router](https://github.com/solidjs/solid-router) | Solid | Official router for Solid. |
| [Angular Router](https://angular.dev/guide/routing) | Angular | Built-in Angular routing. |
| [Expo Router](https://docs.expo.dev/router/introduction/) | React Native | File-based routing for native and web. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Animation

| Name | Description |
|---|---|
| [Motion](https://motion.dev/) | Animation library for JavaScript, React, and Vue (formerly Framer Motion). |
| [GSAP](https://gsap.com/) | Professional-grade animation toolkit, free to use. |
| [React Spring](https://www.react-spring.dev/) | Spring-physics animations for React. |
| [AutoAnimate](https://auto-animate.formkit.com/) | Zero-config drop-in animation utility. |
| [Anime.js](https://animejs.com/) | Lightweight JavaScript animation engine. |
| [Theatre.js](https://www.theatrejs.com/) | Motion design editor and animation library. |
| [Lenis](https://lenis.darkroom.engineering/) | Smooth scroll library. |
| [Barba.js](https://barba.js.org/) | Smooth page transitions for multi-page sites. |
| [AOS](https://michalsnik.github.io/aos/) | Animate elements on scroll. |
| [View Transitions API](https://developer.mozilla.org/en-US/docs/Web/API/View_Transition_API) | Native browser page and element transitions, no library needed. |
| [Lottie](https://airbnb.io/lottie/) | Render After Effects animations natively on web and mobile. |
| [Rive](https://rive.app/) | Interactive vector animations with a runtime for web. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## 3D, canvas & graphics

| Name | Description |
|---|---|
| [Three.js](https://threejs.org/) | Lightweight 3D library with WebGL and WebGPU renderers. |
| [React Three Fiber](https://r3f.docs.pmnd.rs/) | React renderer for Three.js. |
| [Drei](https://github.com/pmndrs/drei) | Ready-made helpers for React Three Fiber. |
| [Threlte](https://threlte.xyz/) | Three.js for Svelte. |
| [TresJS](https://tresjs.org/) | Three.js for Vue. |
| [Babylon.js](https://www.babylonjs.com/) | Powerful 3D engine for the web. |
| [PlayCanvas](https://playcanvas.com/) | WebGL/WebGPU game engine. |
| [A-Frame](https://aframe.io/) | Build VR/AR experiences with HTML. |
| [PixiJS](https://pixijs.com/) | Fast 2D WebGL/WebGPU renderer. |
| [Phaser](https://phaser.io/) | HTML5 game framework. |
| [Matter.js](https://brm.io/matter-js/) | 2D physics engine. |
| [Konva](https://konvajs.org/) | 2D canvas framework for interactive drawings. |
| [Fabric.js](https://fabricjs.com/) | Interactive canvas object model. |
| [p5.js](https://p5js.org/) | Creative coding for artists and beginners. |
| [Paper.js](http://paperjs.org/) | Vector graphics scripting on canvas. |
| [Excalidraw](https://github.com/excalidraw/excalidraw) | Hand-drawn style whiteboard, embeddable as a React component. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Charts, maps & diagrams

| Name | Description |
|---|---|
| [D3](https://d3js.org/) | Low-level toolkit for bespoke data visualization. |
| [Apache ECharts](https://echarts.apache.org/) | Powerful interactive charting library. |
| [Chart.js](https://www.chartjs.org/) | Simple, flexible canvas charts. |
| [Recharts](https://recharts.org/) | Composable charts built with React and D3. |
| [Nivo](https://nivo.rocks/) | Rich React chart components. |
| [visx](https://airbnb.io/visx/) | Low-level React visualization primitives by Airbnb. |
| [Unovis](https://unovis.dev/) | Modular charts for React, Vue, Svelte, Angular. |
| [LayerChart](https://layerchart.com/) | Composable Svelte charts. |
| [ApexCharts](https://apexcharts.com/) | Interactive SVG charts. |
| [Plotly.js](https://plotly.com/javascript/) | Scientific and 3D charts. |
| [Vega-Lite](https://vega.github.io/vega-lite/) | Declarative JSON grammar for charts. |
| [Observable Plot](https://observablehq.com/plot/) | Concise API for exploratory charts. |
| [uPlot](https://github.com/leeoniya/uPlot) | Tiny, fast time-series charts. |
| [Leaflet](https://leafletjs.com/) | Simple, lightweight interactive maps. |
| [MapLibre GL JS](https://maplibre.org/) | Open source vector maps with WebGL. |
| [deck.gl](https://deck.gl/) | GPU-powered large-scale data visualization on maps. |
| [React Flow](https://reactflow.dev/) | Node-based editors and diagrams (also Svelte Flow). |
| [Mermaid](https://mermaid.js.org/) | Diagrams from Markdown-like text. |
| [Cytoscape.js](https://js.cytoscape.org/) | Graph and network visualization. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Icons

| Name | Description |
|---|---|
| [Lucide](https://lucide.dev/) | Clean, consistent open source icon set. |
| [Heroicons](https://heroicons.com/) | SVG icons by the Tailwind team. |
| [Tabler Icons](https://tabler.io/icons) | 5000+ free MIT-licensed SVG icons. |
| [Phosphor Icons](https://phosphoricons.com/) | Flexible icon family with multiple weights. |
| [Remix Icon](https://remixicon.com/) | Neutral-style open source icons. |
| [Iconoir](https://iconoir.com/) | Large library of free SVG icons. |
| [Bootstrap Icons](https://icons.getbootstrap.com/) | Official Bootstrap icon library. |
| [Material Symbols](https://fonts.google.com/icons) | Google's variable icon font. |
| [Radix Icons](https://www.radix-ui.com/icons) | Crisp 15×15 icons. |
| [Feather](https://feathericons.com/) | Simple, beautiful open source icons. |
| [Font Awesome](https://fontawesome.com/) | Popular icon toolkit (free tier). |
| [Simple Icons](https://simpleicons.org/) | SVG icons for popular brands. |
| [SVGL](https://svgl.app/) | Library of SVG logos. |
| [Iconify](https://iconify.design/) | One API for 200k+ icons from many sets. |
| [unplugin-icons](https://github.com/unplugin/unplugin-icons) | Use any Iconify icon as a component, on demand. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Fonts & typography

| Name | Description |
|---|---|
| [Google Fonts](https://fonts.google.com/) | Free, open source font library. |
| [Fontsource](https://fontsource.org/) | Self-host open source fonts via npm packages. |
| [Bunny Fonts](https://fonts.bunny.net/) | Privacy-first Google Fonts drop-in replacement. |
| [Fontshare](https://www.fontshare.com/) | Free quality fonts by Indian Type Foundry. |
| [Font Squirrel](https://www.fontsquirrel.com/) | Free fonts licensed for commercial use. |
| [Inter](https://rsms.me/inter/) | Typeface designed for screens. |
| [Geist](https://vercel.com/font) | Open source sans and mono by Vercel. |
| [JetBrains Mono](https://www.jetbrains.com/lp/mono/) | Free monospace font for developers. |
| [Modern Font Stacks](https://modernfontstacks.com/) | System font stacks, no downloads needed. |
| [Utopia](https://utopia.fyi/) | Fluid type and space scale calculators. |
| [Capsize](https://seek-oss.github.io/capsize/) | Precise text sizing and trimming in CSS. |
| [Wakamai Fondue](https://wakamaifondue.com/) | See what a font file can do. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Accessibility

> Concepts behind this: [dev-knowledge → Frontend concepts](https://github.com/alwintwk/dev-knowledge#frontend-concepts)

| Name | Description |
|---|---|
| [ARIA Authoring Practices Guide](https://www.w3.org/WAI/ARIA/apg/) | How to build accessible widgets, with examples. |
| [WCAG quick reference](https://www.w3.org/WAI/WCAG22/quickref/) | Searchable accessibility guidelines. |
| [The A11Y Project](https://www.a11yproject.com/) | Community checklist and resources. |
| [Inclusive Components](https://inclusive-components.design/) | Articles on building accessible components. |
| [axe-core](https://github.com/dequelabs/axe-core) | Accessibility testing engine used by most tools. |
| [WAVE](https://wave.webaim.org/) | Web accessibility evaluation tool. |
| [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) | Check color contrast ratios. |
| [Pa11y](https://pa11y.org/) | Automated accessibility testing from the command line. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Runtimes & version managers

| Name | Description |
|---|---|
| [Node.js](https://nodejs.org/) | The standard server-side JavaScript runtime. |
| [Deno](https://deno.com/) | Secure runtime with built-in TypeScript and tooling. |
| [Bun](https://bun.sh/) | Fast all-in-one runtime, bundler, test runner, and package manager. |
| [workerd](https://github.com/cloudflare/workerd) | Cloudflare Workers runtime, self-hostable. |
| [LLRT](https://github.com/awslabs/llrt) | Lightweight JS runtime for fast serverless cold starts. |
| [mise](https://mise.jdx.dev/) | Manage Node, Python, and other tool versions per project. |
| [fnm](https://github.com/Schniz/fnm) | Fast Node.js version manager in Rust. |
| [nvm](https://github.com/nvm-sh/nvm) | Classic Node.js version manager. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Package managers & monorepos

| Name | Description |
|---|---|
| [npm](https://www.npmjs.com/) | Default package manager for Node.js. |
| [pnpm](https://pnpm.io/) | Fast, disk-efficient package manager. |
| [Yarn](https://yarnpkg.com/) | Package manager with workspaces and Plug'n'Play. |
| [JSR](https://jsr.io/) | Modern TypeScript-first package registry. |
| [Verdaccio](https://verdaccio.org/) | Lightweight private npm registry. |
| [Turborepo](https://turborepo.com/) | High-performance build system for monorepos. |
| [Nx](https://nx.dev/) | Smart monorepo build system. |
| [moon](https://moonrepo.dev/) | Rust-based repo management and task runner. |
| [Rush](https://rushjs.io/) | Microsoft's scalable monorepo manager. |
| [Lerna](https://lerna.js.org/) | Versioning and publishing for JS monorepos. |
| [Changesets](https://github.com/changesets/changesets) | Manage versions and changelogs in monorepos. |
| [Renovate](https://docs.renovatebot.com/) | Automated dependency update PRs. |
| [npm-check-updates](https://github.com/raineorshine/npm-check-updates) | Upgrade package.json dependencies to latest. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Build tools & bundlers

> Concepts behind this: [dev-knowledge → Frontend concepts (bundler, tree shaking)](https://github.com/alwintwk/dev-knowledge#frontend-concepts)

| Name | Description |
|---|---|
| [Vite](https://vite.dev/) | Fast dev server and build tool. |
| [Rolldown](https://rolldown.rs/) | Rust-based bundler powering Vite. |
| [esbuild](https://esbuild.github.io/) | Extremely fast JavaScript bundler. |
| [Rspack](https://rspack.rs/) | Rust-based webpack-compatible bundler. |
| [Rsbuild](https://rsbuild.rs/) | Rspack-based build tool with sane defaults. |
| [Turbopack](https://nextjs.org/docs/app/api-reference/turbopack) | Rust-based incremental bundler built into Next.js. |
| [Farm](https://www.farmfe.org/) | Rust-based, Vite-compatible build tool. |
| [Rollup](https://rollupjs.org/) | Module bundler for libraries. |
| [webpack](https://webpack.js.org/) | Highly configurable, battle-tested bundler. |
| [Parcel](https://parceljs.org/) | Zero-config build tool. |
| [tsdown](https://tsdown.dev/) | Library bundler powered by Rolldown. |
| [tsup](https://github.com/egoist/tsup) | Bundle TypeScript libraries with no config. |
| [unbuild](https://github.com/unjs/unbuild) | Unified library build system from UnJS. |
| [unplugin](https://unplugin.unjs.io/) | Write one plugin for Vite, Rollup, webpack, esbuild, and more. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Languages & compilers

| Name | Description |
|---|---|
| [TypeScript](https://www.typescriptlang.org/) | JavaScript with static types. |
| [TC39 proposals](https://github.com/tc39/proposals) | Track upcoming JavaScript features. |
| [tsx](https://github.com/privatenumber/tsx) | Run TypeScript files directly in Node.js. |
| [SWC](https://swc.rs/) | Rust-based JS/TS compiler. |
| [Babel](https://babeljs.io/) | JavaScript compiler for next-gen syntax. |
| [Effect](https://effect.website/) | TypeScript library for typed errors, concurrency, and more. |
| [Elm](https://elm-lang.org/) | Functional language for reliable web apps. |
| [ReScript](https://rescript-lang.org/) | Fast, type-safe language that compiles to JavaScript. |
| [Gleam](https://gleam.run/) | Type-safe language for the Erlang VM and JavaScript. |
| [WebAssembly](https://webassembly.org/) | Binary format to run C, Rust, Go and more in the browser. |
| [AssemblyScript](https://www.assemblyscript.org/) | TypeScript-like language for WebAssembly. |
| [Emscripten](https://emscripten.org/) | Compile C/C++ to WebAssembly. |
| [Pyodide](https://pyodide.org/) | Python in the browser via WebAssembly. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Linting & formatting

| Name | Description |
|---|---|
| [ESLint](https://eslint.org/) | Pluggable JavaScript/TypeScript linter. |
| [typescript-eslint](https://typescript-eslint.io/) | TypeScript support for ESLint. |
| [ESLint Stylistic](https://eslint.style/) | Formatting rules for ESLint. |
| [Prettier](https://prettier.io/) | Opinionated code formatter. |
| [Biome](https://biomejs.dev/) | Fast all-in-one formatter and linter. |
| [Oxc (oxlint)](https://oxc.rs/) | Rust-based high-performance JS tooling and linter. |
| [dprint](https://dprint.dev/) | Pluggable, fast code formatter. |
| [Stylelint](https://stylelint.io/) | CSS linter. |
| [markdownlint](https://github.com/DavidAnson/markdownlint) | Markdown linter. |
| [Knip](https://knip.dev/) | Find unused files, dependencies, and exports. |
| [publint](https://publint.dev/) | Lint npm packages for publishing issues. |
| [Are the Types Wrong?](https://arethetypeswrong.github.io/) | Check a package's TypeScript types resolve correctly. |
| [Husky](https://typicode.github.io/husky/) | Run scripts on git hooks. |
| [lint-staged](https://github.com/lint-staged/lint-staged) | Run linters on staged files only. |
| [Lefthook](https://github.com/evilmartians/lefthook) | Fast git hooks manager. |
| [commitlint](https://commitlint.js.org/) | Lint commit messages. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Testing

> Concepts behind this: [dev-knowledge → Testing](https://github.com/alwintwk/dev-knowledge#testing)

| Name | Description |
|---|---|
| [Vitest](https://vitest.dev/) | Vite-native unit test framework. |
| [Jest](https://jestjs.io/) | Popular JavaScript testing framework. |
| [Node.js test runner](https://nodejs.org/api/test.html) | Built-in `node:test`, no dependencies. |
| [Mocha](https://mochajs.org/) | Flexible, long-standing test framework. |
| [Playwright](https://playwright.dev/) | Cross-browser end-to-end testing. |
| [Cypress](https://www.cypress.io/) | Browser-based end-to-end and component testing. |
| [WebdriverIO](https://webdriver.io/) | Browser and mobile automation framework. |
| [Puppeteer](https://pptr.dev/) | Control Chrome and Firefox from Node.js. |
| [Selenium](https://www.selenium.dev/) | The original browser automation project. |
| [Testing Library](https://testing-library.com/) | Test UI the way users use it. |
| [Storybook](https://storybook.js.org/) | Build, document, and test UI components in isolation. |
| [MSW](https://mswjs.io/) | Mock APIs at the network level. |
| [BackstopJS](https://github.com/garris/BackstopJS) | Visual regression testing. |
| [Stryker](https://stryker-mutator.io/) | Mutation testing to measure test quality. |
| [k6](https://k6.io/) | Load testing with JavaScript scripts. |
| [Artillery](https://www.artillery.io/) | Load testing at scale. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Backend frameworks

> Concepts behind this: [dev-knowledge → Backend & APIs](https://github.com/alwintwk/dev-knowledge#backend--apis)

> Full-stack meta-frameworks like Next.js, Nuxt, and SvelteKit also run server code. See [Meta-frameworks](#meta-frameworks).

| Name | Language | Description |
|---|---|---|
| [Hono](https://hono.dev/) | JS/TS | Small, fast web framework for any JS runtime. |
| [Express](https://expressjs.com/) | JS/TS | Minimal, classic Node.js web framework. |
| [Fastify](https://fastify.dev/) | JS/TS | Fast, low-overhead Node.js framework. |
| [NestJS](https://nestjs.com/) | JS/TS | Structured, Angular-style Node.js framework. |
| [Koa](https://koajs.com/) | JS/TS | Lightweight middleware framework by the Express team. |
| [AdonisJS](https://adonisjs.com/) | JS/TS | Batteries-included TypeScript framework, Laravel-style. |
| [Nitro](https://nitro.build/) | JS/TS | Universal server toolkit that powers Nuxt; deploy anywhere. |
| [Elysia](https://elysiajs.com/) | JS/TS | Ergonomic, type-safe framework for Bun. |
| [Encore](https://encore.dev/) | TS/Go | Backend framework with built-in infrastructure and tracing. |
| [Django](https://www.djangoproject.com/) | Python | Batteries-included Python web framework. |
| [FastAPI](https://fastapi.tiangolo.com/) | Python | Modern, fast Python API framework. |
| [Flask](https://flask.palletsprojects.com/) | Python | Lightweight Python micro-framework. |
| [Litestar](https://litestar.dev/) | Python | High-performance ASGI framework. |
| [Gin](https://gin-gonic.com/) | Go | Fast HTTP web framework for Go. |
| [Echo](https://echo.labstack.com/) | Go | Minimalist, extensible Go web framework. |
| [Fiber](https://gofiber.io/) | Go | Express-inspired Go framework. |
| [Axum](https://github.com/tokio-rs/axum) | Rust | Ergonomic, modular framework built on Tokio. |
| [Actix Web](https://actix.rs/) | Rust | Powerful, very fast Rust web framework. |
| [Spring Boot](https://spring.io/projects/spring-boot) | Java/Kotlin | Production-ready Java apps with minimal config. |
| [Quarkus](https://quarkus.io/) | Java | Cloud-native, fast-startup Java framework. |
| [Ktor](https://ktor.io/) | Kotlin | Asynchronous Kotlin server framework by JetBrains. |
| [ASP.NET Core](https://dotnet.microsoft.com/apps/aspnet) | C# | Cross-platform .NET web framework. |
| [Laravel](https://laravel.com/) | PHP | Expressive PHP web framework. |
| [Symfony](https://symfony.com/) | PHP | Reusable PHP components and framework. |
| [Ruby on Rails](https://rubyonrails.org/) | Ruby | Full-stack Ruby web framework. |
| [Phoenix](https://www.phoenixframework.org/) | Elixir | Real-time web framework with LiveView. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## APIs, RPC & realtime

> Concepts behind this: [dev-knowledge → Backend & APIs](https://github.com/alwintwk/dev-knowledge#backend--apis)

| Name | Description |
|---|---|
| [tRPC](https://trpc.io/) | End-to-end type-safe APIs without schemas. |
| [oRPC](https://orpc.unnoq.com/) | Type-safe RPC with OpenAPI support. |
| [ts-rest](https://ts-rest.com/) | Type-safe REST contracts shared by client and server. |
| [GraphQL](https://graphql.org/) | Query language for APIs. |
| [GraphQL Yoga](https://the-guild.dev/graphql/yoga-server) | Fully-featured GraphQL server. |
| [Apollo Server](https://www.apollographql.com/docs/apollo-server) | Popular spec-compliant GraphQL server. |
| [Pothos](https://pothos-graphql.dev/) | Code-first, type-safe GraphQL schema builder. |
| [gRPC](https://grpc.io/) | High-performance RPC framework. |
| [Connect](https://connectrpc.com/) | Browser and gRPC-compatible HTTP APIs from Protobuf. |
| [OpenAPI](https://www.openapis.org/) | Standard for describing HTTP APIs. |
| [Hey API](https://heyapi.dev/) | Generate TypeScript clients from OpenAPI specs. |
| [Orval](https://orval.dev/) | Generate typed clients and hooks from OpenAPI. |
| [Scalar](https://github.com/scalar/scalar) | Beautiful interactive API references from OpenAPI. |
| [Swagger UI](https://swagger.io/tools/swagger-ui/) | Classic interactive API docs. |
| [Socket.IO](https://socket.io/) | Realtime bidirectional event-based communication. |
| [ws](https://github.com/websockets/ws) | Fast, simple WebSocket library for Node.js. |
| [PartyKit](https://www.partykit.io/) | Realtime multiplayer on Cloudflare. |
| [Hoppscotch](https://hoppscotch.io/) | Open source API development ecosystem. |
| [Bruno](https://www.usebruno.com/) | Offline-first, git-friendly API client. |
| [Insomnia](https://insomnia.rest/) | API client for REST, GraphQL, and gRPC. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Databases, ORMs & search

> Concepts behind this: [dev-knowledge → Databases](https://github.com/alwintwk/dev-knowledge#databases)

| Name | Description |
|---|---|
| [PostgreSQL](https://www.postgresql.org/) | Powerful open source relational database. |
| [MySQL](https://www.mysql.com/) | Popular open source relational database. |
| [MariaDB](https://mariadb.org/) | Community-developed fork of MySQL. |
| [SQLite](https://www.sqlite.org/) | Embedded SQL database engine. |
| [libSQL](https://github.com/tursodatabase/libsql) | Open-contribution fork of SQLite (powers Turso). |
| [PGlite](https://pglite.dev/) | Postgres in WASM, runs in the browser or Node. |
| [DuckDB](https://duckdb.org/) | In-process analytical SQL database. |
| [ClickHouse](https://clickhouse.com/) | Fast column-oriented analytics database. |
| [MongoDB](https://www.mongodb.com/) | Document database (source-available). |
| [Redis](https://redis.io/) | In-memory data store for caching and queues. |
| [Valkey](https://valkey.io/) | Open source (BSD) fork of Redis. |
| [pgvector](https://github.com/pgvector/pgvector) | Vector similarity search in Postgres. |
| [Drizzle ORM](https://orm.drizzle.team/) | Lightweight, SQL-like TypeScript ORM. |
| [Prisma](https://www.prisma.io/) | Type-safe ORM with schema-first modeling. |
| [Kysely](https://kysely.dev/) | Type-safe SQL query builder. |
| [TypeORM](https://typeorm.io/) | Decorator-based ORM for TypeScript. |
| [MikroORM](https://mikro-orm.io/) | TypeScript ORM with Unit of Work and Identity Map. |
| [Sequelize](https://sequelize.org/) | Long-standing Node.js ORM. |
| [Mongoose](https://mongoosejs.com/) | MongoDB object modeling for Node.js. |
| [SQLAlchemy](https://www.sqlalchemy.org/) | Python SQL toolkit and ORM. |
| [Meilisearch](https://www.meilisearch.com/) | Fast, typo-tolerant search engine. |
| [Typesense](https://typesense.org/) | Open source alternative to Algolia. |
| [BullMQ](https://bullmq.io/) | Redis-based job queue for Node.js. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Auth

> Concepts behind this: [dev-knowledge → Auth & identity (SSO, OAuth, JWT)](https://github.com/alwintwk/dev-knowledge#auth--identity)

| Name | Description |
|---|---|
| [Better Auth](https://www.better-auth.com/) | Framework-agnostic TypeScript auth library. |
| [Auth.js](https://authjs.dev/) | Authentication for web frameworks (formerly NextAuth). |
| [OpenAuth](https://openauth.js.org/) | Universal, standards-based auth provider. |
| [Lucia](https://lucia-auth.com/) | Guide to implementing sessions and auth yourself. |
| [Arctic](https://arcticjs.dev/) | OAuth 2.0 clients for 50+ providers. |
| [Passport.js](https://www.passportjs.org/) | Classic auth middleware for Node.js. |
| [SimpleWebAuthn](https://simplewebauthn.dev/) | Passkeys and WebAuthn made easy. |
| [SuperTokens](https://supertokens.com/) | Self-hostable auth with prebuilt UI. |
| [Logto](https://logto.io/) | Open source auth infrastructure (OIDC). |
| [Zitadel](https://zitadel.com/) | Identity management with multi-tenancy. |
| [Keycloak](https://www.keycloak.org/) | Self-hosted identity and access management. |
| [Authentik](https://goauthentik.io/) | Self-hosted identity provider. |
| [Ory](https://www.ory.sh/) | Open source identity infrastructure. |
| [CASL](https://casl.js.org/) | Isomorphic permission management. |
| [OpenFGA](https://openfga.dev/) | Fine-grained authorization inspired by Google Zanzibar. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Backend as a service

| Name | Description |
|---|---|
| [Supabase](https://supabase.com/) | Postgres development platform: DB, auth, storage, realtime. |
| [Appwrite](https://appwrite.io/) | Self-hostable backend for web and mobile. |
| [PocketBase](https://pocketbase.io/) | Backend in one file: SQLite, auth, realtime. |
| [Convex](https://www.convex.dev/) | Reactive database with TypeScript functions. |
| [Nhost](https://nhost.io/) | Postgres, GraphQL, auth, and storage. |
| [Hasura](https://hasura.io/) | Instant GraphQL and REST APIs on your data. |
| [InstantDB](https://www.instantdb.com/) | Realtime database for the frontend. |
| [Parse Platform](https://parseplatform.org/) | Long-running open source backend framework. |
| [Trigger.dev](https://trigger.dev/) | Background jobs and workflows in TypeScript. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Hosting & deployment

> Concepts behind this: [dev-knowledge → DevOps & cloud](https://github.com/alwintwk/dev-knowledge#devops--cloud)

| Name | Description |
|---|---|
| [Docker](https://www.docker.com/) | Package apps into containers. |
| [Coolify](https://coolify.io/) | Self-hosted Heroku/Netlify alternative. |
| [Dokploy](https://dokploy.com/) | Self-hosted PaaS for apps and databases. |
| [CapRover](https://caprover.com/) | Easy self-hosted app deployment. |
| [Kamal](https://kamal-deploy.org/) | Deploy containers to any server with zero downtime. |
| [Caddy](https://caddyserver.com/) | Web server with automatic HTTPS. |
| [Nginx](https://nginx.org/) | High-performance web server and reverse proxy. |
| [Traefik](https://traefik.io/traefik/) | Cloud-native reverse proxy. |
| [GitHub Pages](https://pages.github.com/) | Free static hosting from a repo. |
| [Cloudflare Pages](https://pages.cloudflare.com/) | Static and full-stack hosting (free tier). |
| [Netlify](https://www.netlify.com/) | Hosting for web projects (free tier). |
| [Vercel](https://vercel.com/) | Hosting from the creators of Next.js (free tier). |
| [Railway](https://railway.com/) | Deploy apps and databases in a few clicks (trial credit). |
| [Fly.io](https://fly.io/) | Run apps close to users worldwide. |
| [Render](https://render.com/) | Cloud hosting for apps and databases (free tier). |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## CDNs

| Name | Description |
|---|---|
| [jsDelivr](https://www.jsdelivr.com/) | Free CDN for npm and GitHub. |
| [unpkg](https://unpkg.com/) | Fast CDN for everything on npm. |
| [cdnjs](https://cdnjs.com/) | Free open source CDN by Cloudflare. |
| [esm.sh](https://esm.sh/) | npm packages as ES modules, no build step. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Analytics & monitoring

> Concepts behind this: [dev-knowledge → Observability](https://github.com/alwintwk/dev-knowledge#observability--reliability)

| Name | Description |
|---|---|
| [Plausible](https://plausible.io/) | Privacy-friendly, lightweight analytics. |
| [Umami](https://umami.is/) | Simple, privacy-focused analytics. |
| [PostHog](https://posthog.com/) | Product analytics, session replay, and feature flags. |
| [OpenTelemetry](https://opentelemetry.io/) | Standard for traces, metrics, and logs. |
| [Grafana](https://grafana.com/oss/grafana/) | Dashboards for metrics and logs. |
| [GlitchTip](https://glitchtip.com/) | Open source error tracking (Sentry-compatible). |
| [Sentry](https://sentry.io/) | Error and performance monitoring (free tier). |
| [Uptime Kuma](https://github.com/louislam/uptime-kuma) | Self-hosted uptime monitoring. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Mobile & desktop

| Name | Description |
|---|---|
| [React Native](https://reactnative.dev/) | Build native apps with React. |
| [Expo](https://expo.dev/) | Framework and tools for React Native. |
| [NativeWind](https://www.nativewind.dev/) | Tailwind CSS for React Native. |
| [Tamagui](https://tamagui.dev/) | Universal UI kit for React Native and web. |
| [Lynx](https://lynxjs.org/) | ByteDance's native UI framework with web tech. |
| [NativeScript](https://nativescript.org/) | Native mobile apps with JavaScript. |
| [Flutter](https://flutter.dev/) | Google's UI toolkit for mobile, web, and desktop. |
| [Kotlin Multiplatform](https://kotlinlang.org/docs/multiplatform.html) | Share Kotlin code across Android, iOS, web, and desktop. |
| [.NET MAUI](https://dotnet.microsoft.com/apps/maui) | Cross-platform native apps with C#. |
| [Capacitor](https://capacitorjs.com/) | Run web apps natively on iOS and Android. |
| [Ionic](https://ionicframework.com/) | Mobile UI toolkit for web technologies. |
| [Tauri](https://tauri.app/) | Small, secure desktop and mobile apps with a web frontend. |
| [Electron](https://www.electronjs.org/) | Cross-platform desktop apps with JS, HTML, and CSS. |
| [Wails](https://wails.io/) | Desktop apps with Go and web tech. |
| [Neutralinojs](https://neutralino.js.org/) | Lightweight portable desktop apps. |
| [PWABuilder](https://www.pwabuilder.com/) | Turn a web app into a store-ready PWA. |
| [Workbox](https://developer.chrome.com/docs/workbox) | Service worker libraries for offline support. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Images & media

| Name | Description |
|---|---|
| [Squoosh](https://squoosh.app/) | In-browser image compression. |
| [sharp](https://sharp.pixelplumbing.com/) | High-performance Node.js image processing. |
| [libvips](https://www.libvips.org/) | Fast, low-memory image processing library. |
| [ImageMagick](https://imagemagick.org/) | Create, edit, and convert images. |
| [imgproxy](https://imgproxy.net/) | Fast on-the-fly image resizing server. |
| [Unpic](https://unpic.pics/) | Responsive image components for many frameworks and CDNs. |
| [SVGO](https://github.com/svg/svgo) | Optimize SVG files. |
| [SVGOMG](https://jakearchibald.github.io/svgomg/) | Web GUI for SVGO. |
| [oxipng](https://github.com/shssoichiro/oxipng) | Multithreaded lossless PNG optimizer. |
| [ImageOptim](https://imageoptim.com/) | Lossless image compressor for macOS. |
| [BlurHash](https://blurha.sh/) | Compact placeholders for images. |
| [ThumbHash](https://evanw.github.io/thumbhash/) | Better image placeholders with alpha support. |
| [FFmpeg](https://ffmpeg.org/) | Record, convert, and stream audio and video. |
| [HandBrake](https://handbrake.fr/) | Open source video transcoder. |
| [Vidstack](https://vidstack.io/) | Modern video and audio player components. |
| [Plyr](https://plyr.io/) | Simple, accessible HTML5 media player. |
| [hls.js](https://github.com/video-dev/hls.js) | Play HLS streams in the browser. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Performance & browser support

> Concepts behind this: [dev-knowledge → Performance](https://github.com/alwintwk/dev-knowledge#performance)

| Name | Description |
|---|---|
| [Lighthouse](https://developer.chrome.com/docs/lighthouse) | Automated audits for performance, accessibility, and SEO. |
| [Lighthouse CI](https://github.com/GoogleChrome/lighthouse-ci) | Run Lighthouse on every commit. |
| [Unlighthouse](https://unlighthouse.dev/) | Scan a whole site with Lighthouse. |
| [PageSpeed Insights](https://pagespeed.web.dev/) | Lab and field performance data for any URL. |
| [WebPageTest](https://www.webpagetest.org/) | Detailed real-browser performance testing. |
| [sitespeed.io](https://www.sitespeed.io/) | Open source performance monitoring tools. |
| [web-vitals](https://github.com/GoogleChrome/web-vitals) | Measure Core Web Vitals in the field. |
| [Can I use](https://caniuse.com/) | Browser support tables for web features. |
| [Baseline](https://web.dev/baseline) | Which web features are safe to use across browsers. |
| [MDN browser-compat-data](https://github.com/mdn/browser-compat-data) | Browser compatibility data behind MDN and Can I use. |
| [Browserslist](https://browsersl.ist/) | Share target browsers between tools. |
| [Responsively App](https://responsively.app/) | Preview a site on many screen sizes at once. |
| [bundlephobia](https://bundlephobia.com/) | Find the cost of adding an npm package. |
| [pkg-size](https://pkg-size.dev/) | Check npm package install size. |
| [rollup-plugin-visualizer](https://github.com/btd/rollup-plugin-visualizer) | Visualize Vite/Rollup bundle contents. |
| [webpack-bundle-analyzer](https://github.com/webpack-contrib/webpack-bundle-analyzer) | Visualize webpack bundle contents. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Placeholders & mock data

| Name | Description |
|---|---|
| [Lorem Picsum](https://picsum.photos/) | Random placeholder photos. |
| [placehold.co](https://placehold.co/) | Custom-size placeholder images. |
| [Unsplash](https://unsplash.com/) | Free high-resolution photos. |
| [Pexels](https://www.pexels.com/) | Free stock photos and videos. |
| [unDraw](https://undraw.co/) | Free open source illustrations. |
| [DiceBear](https://www.dicebear.com/) | Open source avatar library. |
| [Faker](https://fakerjs.dev/) | Generate realistic fake data. |
| [JSONPlaceholder](https://jsonplaceholder.typicode.com/) | Free fake REST API for testing. |
| [DummyJSON](https://dummyjson.com/) | Fake REST API with products, users, and more. |
| [Random User](https://randomuser.me/) | Random user data API. |
| [json-server](https://github.com/typicode/json-server) | Full fake REST API from a JSON file. |
| [Mockoon](https://mockoon.com/) | Desktop app for mock APIs. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## SEO, favicons & meta

| Name | Description |
|---|---|
| [RealFaviconGenerator](https://realfavicongenerator.net/) | Generate favicons for every platform. |
| [favicon.io](https://favicon.io/) | Make favicons from text, emoji, or images. |
| [Maskable.app](https://maskable.app/) | Preview and create maskable PWA icons. |
| [Open Graph protocol](https://ogp.me/) | Rich link previews on social platforms. |
| [metatags.io](https://metatags.io/) | Preview and generate meta tags. |
| [Satori](https://github.com/vercel/satori) | Convert HTML/CSS to SVG, used for OG images. |
| [Schema.org](https://schema.org/) | Structured data vocabulary for search engines. |
| [Google Search Console](https://search.google.com/search-console) | Monitor your site in Google Search. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Lists of lists

| Name | Description |
|---|---|
| [Awesome](https://github.com/sindresorhus/awesome) | Awesome lists about all kinds of topics. |
| [Awesome React](https://github.com/enaqx/awesome-react) | React ecosystem resources. |
| [Awesome Vue](https://github.com/vuejs/awesome-vue) | Vue ecosystem resources. |
| [Awesome Svelte](https://github.com/TheComputerM/awesome-svelte) | Svelte ecosystem resources. |
| [Awesome Angular](https://github.com/PatrickJS/awesome-angular) | Angular ecosystem resources. |
| [Awesome Node.js](https://github.com/sindresorhus/awesome-nodejs) | Node.js packages and resources. |
| [Awesome TypeScript](https://github.com/dzharii/awesome-typescript) | TypeScript resources. |
| [Awesome CSS](https://github.com/awesome-css-group/awesome-css) | CSS frameworks, tools, and learning. |
| [Awesome Web Components](https://github.com/web-padawan/awesome-web-components) | Web Components resources. |
| [Awesome Web Performance](https://github.com/davidsonfellipe/awesome-wpo) | Web performance optimization resources. |
| [Awesome Self-Hosted](https://github.com/awesome-selfhosted/awesome-selfhosted) | Free software you can host yourself. |
| [Public APIs](https://github.com/public-apis/public-apis) | Free APIs for projects. |
| [free-for.dev](https://free-for.dev/) | SaaS and services with free tiers for developers. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

---

## Contributing

PRs welcome. Keep entries open source or free, one line each, most popular first within a section.

## License

[CC0 1.0](LICENSE): public domain. Copy, share, and reuse freely.
