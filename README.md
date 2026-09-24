<h1 align="center">Web development resources</h1>
<p align="center"><i>A curated list of open source frameworks, tools, and resources for modern web development.</i></p>
<p align="center">Inspired by <a href="https://github.com/milanaryal/web-development-resources">milanaryal/web-development-resources</a>. Last reviewed: September 2026.<br />New to the terms? See the companion glossary <a href="https://github.com/alwintwk/dev-knowledge">dev-knowledge</a>.<br /><a href="https://alwintwk.github.io/web-dev-resources/">Search it online</a></p>

## Table of contents

* [Which should I pick?](#which-should-i-pick)
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

## Which should I pick?

These are the choices beginners ask about most. There is rarely one right answer, so each guide compares the popular options side by side and ends with a sensible default.

### React vs Vue vs Svelte vs Angular

All four build interactive user interfaces from reusable pieces called components; they differ in how much they decide for you.

| | React | Vue | Svelte | Angular |
|---|---|---|---|---|
| Learning curve | Moderate; JSX (HTML inside JavaScript) plus hooks | Gentle; templates look like plain HTML | Gentle; Svelte 5 "runes" mark reactive values | Steep; many built-in concepts to learn |
| Job market | Largest by far | Solid, strong in Europe and Asia | Smaller but growing | Large, especially at big companies |
| Ecosystem size | Very large; a library for everything | Large, with official router and state tools | Smaller; fewer ready-made libraries | Large; most tools built in |
| How it feels | Flexible; you choose your own tools | Balanced; clear official defaults | Little code; compiler does the work | Structured; one official way to do things |
| Best for | Most jobs and big ecosystems | Beginners and gradual adoption | Small, fast apps and side projects | Large enterprise teams |

**Verdict:** Start with React if you want the widest job options and the most tutorials; React 19 also brings server components (parts that render on the server and send no JavaScript). Pick Vue or Svelte if you want the gentlest start and less code to write. Pick Angular if you are joining a large company or team that already uses it; its newer signals (values that update the page automatically when they change) have made it simpler than it used to be.

See all options: [UI frameworks](#ui-frameworks).

### Next.js vs Astro vs Nuxt vs SvelteKit

A meta-framework wraps a UI framework and adds routing (URLs to pages), server rendering and deployment setup; you need one once your app has more than a few pages or needs good SEO.

| | Next.js | Astro | Nuxt | SvelteKit |
|---|---|---|---|---|
| Built on | React | Any (React, Vue, Svelte, or none) | Vue | Svelte |
| Best for | Full apps with logins and dashboards | Content sites: blogs, docs, marketing | Full apps for Vue users | Full apps for Svelte users |
| JavaScript sent to browser | Moderate; server components help trim it | Almost none by default ("islands" add it where needed) | Moderate | Small |
| Learning curve | Steeper; App Router and server/client split | Gentle; mostly HTML and Markdown | Moderate; lots of helpful conventions | Gentle to moderate |
| Hosting | Easiest on Vercel, works elsewhere | Anywhere, including free static hosts | Anywhere via adapters | Anywhere via adapters |

**Verdict:** For a mostly-content site (blog, portfolio, docs), pick Astro; it is simpler and faster than the rest for that job. For a full app, pick the meta-framework that matches your UI framework: Next.js for React, Nuxt for Vue, SvelteKit for Svelte. A single-page tool with no SEO needs may not need a meta-framework at all; plain Vite (a fast dev server and build tool) is enough.

See all options: [Meta-frameworks](#meta-frameworks).

### Tailwind vs plain CSS / CSS Modules vs a component library

This is really a choice about how much styling you write yourself versus reuse.

| | Tailwind CSS | Plain CSS / CSS Modules | Component library (e.g. MUI, Mantine) |
|---|---|---|---|
| How you style | Small utility classes in your HTML | Your own CSS files; Modules keep class names local | Ready-made buttons, forms, dialogs |
| Learning curve | Learn class names; still need CSS basics | Just CSS; the skill that transfers everywhere | Learn the library's components and theming |
| Speed to a decent UI | Fast once you know the classes | Slowest; you design everything | Fastest; looks finished out of the box |
| Custom look | Easy; any design is possible | Total control | Harder; fighting the default style takes work |
| Watch out for | Long class lists in markup | Naming and organizing grows hard | Larger bundles; tied to one framework |

**Verdict:** Learn plain CSS first no matter what, because every other option builds on it. For most new projects, Tailwind (v4 is configured in your CSS file, no JavaScript config needed) is a good default. Pick a component library like MUI or Mantine when you need a working admin panel or internal tool fast and a custom look matters less.

See all options: [CSS frameworks & styling](#css-frameworks--styling) and [Component libraries](#component-libraries).

### Prisma vs Drizzle vs plain SQL (Kysely)

These tools let your TypeScript code talk to a database with autocomplete and type checks instead of raw strings.

| | Prisma | Drizzle | Kysely |
|---|---|---|---|
| What it is | ORM (maps tables to objects) with its own schema file | Lightweight ORM; schema written in TypeScript | Query builder (type-safe SQL, not an ORM) |
| How queries look | Object style: `findMany({ where })` | Close to SQL, in TypeScript | Almost exactly SQL, in TypeScript |
| Learning curve | Gentle; best docs for beginners | Moderate; easier if you know some SQL | Needs real SQL knowledge |
| Migrations (schema changes) | Generated for you | Generated for you (drizzle-kit) | You write them, with helpers |
| Best for | Beginners and fast prototypes | Serverless apps; people who like SQL | Complex queries; full control |

**Verdict:** Pick Prisma if you are new to databases; its schema file and docs make the first steps easy. Pick Drizzle if you know some SQL and want something lighter that stays close to it. Pick Kysely when you want to write SQL yourself but still get type safety.

See all options: [Databases, ORMs & search](#databases-orms--search).

### Supabase vs Firebase vs PocketBase

A backend as a service gives you a database, user logins and file storage without writing your own server.

| | Supabase | Firebase | PocketBase |
|---|---|---|---|
| Database | PostgreSQL (relational, uses SQL) | Firestore (NoSQL documents) | SQLite (relational, in one file) |
| Open source / self-host | Yes, open source; self-hosting possible | No; Google's proprietary service | Yes; one program you run yourself |
| Strengths | SQL, row-level security, realtime | Mature mobile SDKs, offline sync | Tiny, simple, free to run |
| Watch out for | Must learn some SQL and security policies | Lock-in; costs grow with reads | Pre-1.0; you handle hosting and backups |
| Best for | Web apps that may grow | Mobile apps in the Google ecosystem | Small projects and side projects |

**Verdict:** Supabase is a good default for web apps: you learn real SQL and can move away later because it is plain Postgres. Pick Firebase if you are building a mobile app and value its offline sync and Google integrations. Pick PocketBase for small projects where one cheap server is all you need.

See all options: [Backend as a service](#backend-as-a-service).

### Vitest vs Jest, and Playwright vs Cypress

Unit test runners check small pieces of code; end-to-end (E2E) tools click through your real app in a browser.

| Unit tests | Vitest | Jest |
|---|---|---|
| Setup | Near zero in Vite projects | More config for TypeScript and ES modules |
| Speed feel | Fast, with instant re-runs | Fine, slower on big projects |
| API | Almost the same as Jest | The original; most tutorials use it |
| Best for | New projects, anything using Vite | Existing projects and React Native |

| E2E tests | Playwright | Cypress |
|---|---|---|
| Browsers | Chromium, Firefox, WebKit (Safari's engine) | Chrome-family and Firefox; WebKit experimental |
| Running in parallel | Built in and free | Via paid Cypress Cloud or add-ons |
| Debugging | Trace viewer, UI mode, code generator | Visual runner with time-travel snapshots |
| Best for | Most new projects; multi-tab and multi-browser | Teams already using it |

**Verdict:** For new projects, pick Vitest for unit tests and Playwright for end-to-end tests. Stay with Jest or Cypress if your project already uses them; switching rarely pays off by itself.

See all options: [Testing](#testing).

### npm vs pnpm vs Yarn vs Bun

A package manager downloads the libraries your project depends on and records exact versions in a lockfile.

| | npm | pnpm | Yarn | Bun |
|---|---|---|---|---|
| Comes with | Node.js; nothing to install | Separate install (or via Corepack) | Separate install (or via Corepack) | Bun runtime |
| Install speed | Slowest of the four | Fast | Fast | Fastest |
| Disk use | A full copy per project | Shared store; saves lots of space | Depends on mode (Plug'n'Play saves space) | A full copy per project, cached |
| Monorepos (many packages in one repo) | Workspaces, basic | Workspaces, strong | Workspaces, strong | Workspaces, newer |
| Best for | Beginners; works everywhere | Most teams and monorepos | Existing Yarn projects | Projects already using Bun |

**Verdict:** Use npm while learning; it is already installed and every tutorial uses it. Switch to pnpm when installs feel slow or you start a monorepo. Pick Bun if you use the Bun runtime, and Yarn if your team already does; always use whatever the project's lockfile says.

See all options: [Package managers & monorepos](#package-managers--monorepos).

### Express vs Hono vs Fastify vs NestJS

These frameworks help you write a web server or API in JavaScript or TypeScript.

| | Express | Hono | Fastify | NestJS |
|---|---|---|---|---|
| Learning curve | Easiest; tiny API | Easy; similar to Express | Moderate; schemas and plugins | Steep; decorators and dependency injection |
| Where it runs | Node.js | Anywhere: Node, Bun, Deno, edge platforms | Node.js | Node.js |
| Structure | None; you organize it | Minimal | Plugin-based | Strict; modules, controllers, services |
| Performance feel | Fine for most apps | Fast | Fast | Depends on underlying server |
| Best for | Learning; most tutorials | Edge/serverless and small APIs | Fast, schema-validated APIs | Large team backends |

**Verdict:** Learn Express first; it is simple, Express 5 is current, and most tutorials use it. Pick Hono for new small APIs, especially on edge platforms (servers close to users, like Cloudflare Workers), or Fastify when you want built-in request validation. Pick NestJS for large team projects where a strict structure helps.

See all options: [Backend frameworks](#backend-frameworks).

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Learning & references

This is the shelf of places to actually learn web development, from thirty-second syntax lookups to full multi-month courses. Some are references you dip into like a dictionary; others are structured paths you follow start to finish. Reach for these when you need to learn a new concept or double-check how something works — not when you're picking a tool to build with.

**Start here:** [MDN Web Docs](https://developer.mozilla.org/) — the reference you'll come back to for exact syntax on everything else here.

| Name | Best for |
|---|---|
| ⭐ [MDN Web Docs](https://developer.mozilla.org/) | Looking up exact HTML/CSS/JS/API syntax and browser support. |
| [web.dev](https://web.dev/) | Learning performance, PWA, and newest browser features from Google. |
| [javascript.info](https://javascript.info/) | Learning JavaScript step by step, beginner to advanced. |
| [Eloquent JavaScript](https://eloquentjavascript.net/) | A free, thorough intro book if you like reading over videos. |
| [You Don't Know JS](https://github.com/getify/You-Dont-Know-JS) | Understanding JS internals (closures, prototypes) once basics click. |
| [The Odin Project](https://www.theodinproject.com/) | A free structured path from zero to full-stack projects. |
| [Full Stack Open](https://fullstackopen.com/en/) | A free university-grade course covering React, Node, GraphQL. |
| [freeCodeCamp](https://www.freecodecamp.org/) | Interactive lessons plus certificates for structured self-study. |
| [Frontend Mentor](https://www.frontendmentor.io/) | Practicing by building real designs instead of tutorials. |
| [Exercism](https://exercism.org/) | Practicing algorithms with mentor feedback in 70+ languages. |
| [patterns.dev](https://www.patterns.dev/) | Learning proven rendering and architecture patterns for apps. |
| [roadmap.sh](https://roadmap.sh/) | Figuring out what to learn next and in what order. |
| [CSS-Tricks](https://css-tricks.com/) | Deep-dive CSS articles and an almanac of properties. |
| [Josh W. Comeau](https://www.joshwcomeau.com/) | Highly visual, interactive explanations of CSS and React. |
| [Smashing Magazine](https://www.smashingmagazine.com/) | Longer-form articles on design and dev practice. |
| [Web Almanac](https://almanac.httparchive.org/) | Data-backed snapshot of how the web is really built. |
| [W3C standards](https://www.w3.org/standards/) | Checking the actual spec behind a web feature. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## UI frameworks

A UI framework is what you use to build the interactive parts of a website — buttons, forms, live-updating lists — out of reusable pieces called components, instead of hand-writing DOM updates every time data changes. It solves the problem of keeping what's on screen in sync with your app's data as things change. You need one the moment a page has to react to clicks, typing, or new data without a full reload.

**Start here:** React for widest job/ecosystem support; Vue if you want a gentler learning curve.

| Name | Best for |
|---|---|
| ⭐ [React](https://react.dev/) | Biggest ecosystem and job market; default choice for most apps. |
| ⭐ [Vue](https://vuejs.org/) | Approachable syntax and gentle learning curve for newcomers. |
| [Svelte](https://svelte.dev/) | Less boilerplate; compiles away the framework at build time. |
| [Angular](https://angular.dev/) | Large enterprise apps that want structure and conventions built in. |
| [Solid](https://www.solidjs.com/) | React-like syntax with faster, fine-grained reactivity. |
| [Preact](https://preactjs.com/) | A React swap-in when bundle size really matters. |
| [Qwik](https://qwik.dev/) | Very large sites needing near-instant first load. |
| [Lit](https://lit.dev/) | Building reusable Web Components that work anywhere. |
| [Stencil](https://stenciljs.com/) | Compiling a component library to standalone Web Components. |
| [Ember](https://emberjs.com/) | Large, long-lived apps that want strong conventions. |
| [Marko](https://markojs.com/) | Streaming-heavy sites, popularized by eBay's use case. |
| [Mithril](https://mithril.js.org/) | A tiny framework with routing/XHR baked in, no build step needed. |
| [Alpine.js](https://alpinejs.dev/) | Adding small bits of interactivity to mostly-static HTML. |
| [htmx](https://htmx.org/) | Server-rendered apps that want AJAX without writing JS. |
| [Hotwire](https://hotwired.dev/) | Rails-style apps sending HTML over the wire instead of JSON. |
| [Datastar](https://data-star.dev/) | Combining backend-driven HTML with client-side signals. |
| [Leptos](https://leptos.dev/) | Building a full-stack UI in Rust instead of JS. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Meta-frameworks

A meta-framework wraps a UI framework (like React or Vue) with the extra plumbing a real app needs: routing between pages, loading data efficiently, and rendering on the server for speed and SEO. It solves the problem of having to wire all that up yourself from scratch. Reach for one once you're building more than a single-page demo — anything with multiple routes or real data.

> Concepts behind this: [dev-knowledge → CSR vs SSR vs SSG](https://github.com/alwintwk/dev-knowledge#csr-vs-ssr-vs-ssg)

**Start here:** React: Next.js. Vue: Nuxt. Svelte: SvelteKit.

| Name | Works with | Best for |
|---|---|---|
| ⭐ [Next.js](https://nextjs.org/) | React | Default choice for production React apps; huge ecosystem and docs. |
| ⭐ [Nuxt](https://nuxt.com/) | Vue | Default choice for full-stack Vue apps. |
| ⭐ [SvelteKit](https://svelte.dev/docs/kit) | Svelte | Default (and official) choice for full-stack Svelte apps. |
| [React Router (framework mode)](https://reactrouter.com/) | React | Already using React Router; want a lighter full-stack option. |
| [TanStack Start](https://tanstack.com/start) | React, Solid | Type-safe routing fans already using TanStack tools. |
| [Waku](https://waku.gg/) | React | A minimal React server-components setup without extra framework weight. |
| [Vike](https://vike.dev/) | React, Vue, Solid | Wanting full control over your own Vite-based stack. |
| [Gatsby](https://www.gatsbyjs.com/) | React | Content-heavy static React sites with a plugin data layer. |
| [SolidStart](https://start.solidjs.com/) | Solid | Full-stack apps built with Solid's fine-grained reactivity. |
| [Analog](https://analogjs.org/) | Angular | Full-stack Angular apps that want a Vite-based workflow. |
| [Fresh](https://fresh.deno.dev/) | Preact | Deno projects wanting islands architecture and zero JS by default. |
| [Astro](https://astro.build/) | Any | Content sites mixing multiple UI libraries with minimal JS shipped. |
| [Wasp](https://wasp.sh/) | React + Node | Fast full-stack prototypes with auth and DB wired in already. |
| [Inertia.js](https://inertiajs.com/) | React, Vue, Svelte | Server-rendered apps (Laravel/Rails) that want an SPA feel. |
| [Livewire](https://livewire.laravel.com/) | Laravel | Laravel apps that want dynamic UI without writing JS. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Static sites & docs

A static site generator turns your content (Markdown files, templates) into plain HTML pages ahead of time, rather than building each page freshly for every visitor. That makes sites fast and cheap to host, since there's no server doing work per request — like printing a stack of flyers once instead of photocopying one every time someone asks. Reach for these for blogs, marketing pages, and documentation sites.

**Start here:** General sites: Eleventy. Docs sites: Starlight.

| Name | Best for |
|---|---|
| ⭐ [Eleventy](https://www.11ty.dev/) | Simple general-purpose static sites without locking into one UI framework. |
| ⭐ [Starlight](https://starlight.astro.build/) | Default choice for docs sites; built on Astro. |
| [Hugo](https://gohugo.io/) | Very large sites where build speed matters most. |
| [Jekyll](https://jekyllrb.com/) | GitHub Pages-native blogs; simple Ruby-based setup. |
| [Zola](https://www.getzola.org/) | A single binary, no dependencies to install; fast Rust-based builds. |
| [Hexo](https://hexo.io/) | Node-based blogging with a large theme ecosystem. |
| [VitePress](https://vitepress.dev/) | Vue-flavored docs sites with fast Vite-powered builds. |
| [Docusaurus](https://docusaurus.io/) | React-based docs sites, especially versioned OSS project docs. |
| [Nextra](https://nextra.site/) | Docs or blogs already living inside a Next.js app. |
| [Fumadocs](https://fumadocs.dev/) | Highly customizable docs sites built on Next.js. |
| [Rspress](https://rspress.rs/) | Fast docs builds using the Rspack/Rsbuild toolchain. |
| [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) | Python projects wanting a polished Material Design docs theme. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Headless CMS

A headless CMS is a content-editing backend — where non-developers write and update text, images, and pages — that hands that content back as data through an API instead of rendering its own website. It solves the problem of letting content people publish without a developer touching code, while you keep full control of the frontend. Think of it as a stockroom that ships parts to whatever storefront you build, rather than running its own shop.

**Start here:** [Strapi](https://strapi.io/) — the most established open source option, with the biggest plugin and community base.

| Name | Best for |
|---|---|
| ⭐ [Strapi](https://strapi.io/) | The default open source headless CMS; huge plugin ecosystem. |
| [Payload](https://payloadcms.com/) | TypeScript devs already in Next.js wanting the CMS in-app. |
| [Directus](https://directus.io/) | Turning an existing SQL database into an instant API/admin. |
| [Keystatic](https://keystatic.com/) | Storing content as Markdown/JSON files in your own repo. |
| [TinaCMS](https://tina.io/) | Git-backed content with a visual, in-context editor. |
| [Decap CMS](https://decapcms.org/) | Free Git-based CMS for static sites (ex-Netlify CMS). |
| [Ghost](https://ghost.org/) | A dedicated blog/newsletter platform, not a general CMS. |
| [WordPress](https://wordpress.org/) | Reusing WordPress's huge plugin ecosystem headlessly via REST. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## CSS frameworks & styling

This category covers everything that saves you from writing every visual style by hand: ready-made component frameworks, utility classes, CSS-in-JS, preprocessors, and small tools that transform your CSS. It solves the problem of styling consistently and quickly instead of reinventing buttons, spacing, and grids on every project. Think paint-by-numbers versus mixing every color from raw pigment yourself.

**Start here:** Utility-first: Tailwind CSS. Ready-made components: Bootstrap.

| Name | Best for |
|---|---|
| ⭐ [Tailwind CSS](https://tailwindcss.com/) | Fast, consistent styling directly in your markup; today's default pick. |
| ⭐ [Bootstrap](https://getbootstrap.com/) | Ready-made components and grid when you want something onscreen fast. |
| [Bulma](https://bulma.io/) | Flexbox-based classes without needing JavaScript components. |
| [Foundation](https://get.foundation/) | Responsive layouts across sites and HTML emails. |
| [UIkit](https://getuikit.com/) | A lighter, modular alternative to Bootstrap-style frameworks. |
| [UnoCSS](https://unocss.dev/) | Tailwind-like utilities generated on-demand for smaller output. |
| [Pico CSS](https://picocss.com/) | Making plain semantic HTML look decent with zero classes. |
| [Simple.css](https://simplecss.org/) | Classless CSS for quick, presentable prototypes and demos. |
| [Water.css](https://watercss.kognise.dev/) | A drop-in stylesheet for small or hobby projects. |
| [Open Props](https://open-props.style/) | Ready-made CSS custom properties as a design-token starting point. |
| [Panda CSS](https://panda-css.com/) | Type-safe, build-time CSS-in-JS without a runtime cost. |
| [StyleX](https://stylexjs.com/) | Meta-scale apps wanting compile-time atomic CSS. |
| [vanilla-extract](https://vanilla-extract.style/) | Type-safe styles in TypeScript with zero runtime. |
| [styled-components](https://styled-components.com/) | React apps that want components and styles colocated. |
| [Emotion](https://emotion.sh/) | A flexible, well-established CSS-in-JS choice for React. |
| [CSS Modules](https://github.com/css-modules/css-modules) | Locally scoped class names without adopting a new syntax. |
| [Sass](https://sass-lang.com/) | The standard, mature CSS preprocessor most teams already know. |
| [Less](https://lesscss.org/) | A Sass alternative with similar preprocessor features. |
| [PostCSS](https://postcss.org/) | Plugin-based CSS transforms (autoprefixing, future syntax) under the hood. |
| [Lightning CSS](https://lightningcss.dev/) | Very fast parsing/minifying, often used inside other tools. |
| [Modern Normalize](https://github.com/sindresorhus/modern-normalize) | Resetting inconsistent browser default styles before you start. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Component libraries

A component library gives you pre-built, already-styled UI pieces — buttons, modals, dropdowns, data tables — so you don't design and code every widget from zero. It solves the problem of shipping something that looks professional and works accessibly without weeks of UI polish. It's the difference between buying ready-made furniture and building each chair from raw wood.

**Start here:** React: shadcn/ui. Vue: Vuetify. Angular: Angular Material.

| Name | Works with | Best for |
|---|---|---|
| ⭐ [shadcn/ui](https://ui.shadcn.com/) | React | Today's default for React; copy-paste components you fully own. |
| ⭐ [Vuetify](https://vuetifyjs.com/) | Vue | Default choice for Vue; Material Design components ready to go. |
| ⭐ [Angular Material](https://material.angular.dev/) | Angular | Default, official-feeling choice for Angular apps. |
| [HeroUI](https://www.heroui.com/) | React | Tailwind-based components with a polished look, minimal setup. |
| [MUI](https://mui.com/) | React | Apps that want Material Design out of the box. |
| [Mantine](https://mantine.dev/) | React | A large batteries-included set of React components and hooks. |
| [Chakra UI](https://chakra-ui.com/) | React | Accessible-by-default components with a simple styling API. |
| [Ant Design](https://ant.design/) | React | Enterprise/admin dashboards with a dense, ready-made component set. |
| [Fluent UI](https://github.com/microsoft/fluentui) | React, Web Components | Apps that want Microsoft's design language. |
| [Carbon](https://carbondesignsystem.com/) | React, Web Components | Apps that want IBM's open source design system. |
| [Tremor](https://www.tremor.so/) | React | Building dashboards and charts quickly in React. |
| [Magic UI](https://magicui.design/) | React | Animated, eye-catching components for landing pages. |
| [shadcn-vue](https://www.shadcn-vue.com/) | Vue | The shadcn/ui copy-paste approach for Vue projects. |
| [PrimeVue](https://primevue.org/) | Vue | A large, mature all-in-one component suite for Vue. |
| [Element Plus](https://element-plus.org/) | Vue | Desktop-focused admin UIs built in Vue 3. |
| [Naive UI](https://www.naiveui.com/) | Vue | TypeScript-first, themeable Vue 3 components. |
| [Quasar](https://quasar.dev/) | Vue | One codebase targeting web, mobile, and desktop with Vue. |
| [shadcn-svelte](https://www.shadcn-svelte.com/) | Svelte | The shadcn/ui copy-paste approach for Svelte projects. |
| [Skeleton](https://www.skeleton.dev/) | Svelte, React | Tailwind-based components that adapt across Svelte and React. |
| [PrimeNG](https://primeng.org/) | Angular | A large, mature all-in-one component suite for Angular. |
| [NG-ZORRO](https://ng.ant.design/) | Angular | Ant Design's component set ported to Angular. |
| [Spartan](https://www.spartan.ng/) | Angular | Unstyled, shadcn-style accessible primitives for Angular. |
| [daisyUI](https://daisyui.com/) | Any (Tailwind) | Adding ready-made component classes on top of Tailwind. |
| [Flowbite](https://flowbite.com/) | Any (Tailwind) | Tailwind components with ready framework integrations. |
| [Preline UI](https://preline.co/) | Any (Tailwind) | Tailwind components and copy-paste examples. |
| [Web Awesome](https://webawesome.com/) | Any | Framework-agnostic components as plain Web Components. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Headless / unstyled components

Headless (unstyled) components give you the tricky behavior of a UI widget — keyboard navigation, focus handling, screen-reader support for things like dropdowns and dialogs — with zero visual styling, so you paint it however you like. It solves the problem of getting that fiddly accessibility logic right without writing it yourself. Think of it as buying an unfinished wooden chair frame: structurally correct, but you choose the paint.

**Start here:** React: Radix Primitives. Vue: Reka UI.

| Name | Works with | Best for |
|---|---|---|
| ⭐ [Radix Primitives](https://www.radix-ui.com/primitives) | React | The default accessible primitives for React; what shadcn/ui is built on. |
| ⭐ [Reka UI](https://reka-ui.com/) | Vue | Default choice for Vue; Radix-style unstyled accessible components. |
| [Base UI](https://base-ui.com/) | React | A newer unstyled React set from the Radix/MUI/Floating UI teams. |
| [React Aria](https://react-spectrum.adobe.com/react-aria/) | React | Maximum accessibility rigor, backed by Adobe's a11y research. |
| [Headless UI](https://headlessui.com/) | React, Vue | Simple unstyled components made to pair with Tailwind. |
| [Ark UI](https://ark-ui.com/) | React, Vue, Solid, Svelte | One state-machine-driven component API across several frameworks. |
| [Zag](https://zagjs.com/) | Any | Framework-agnostic state machines to build your own component libs. |
| [Bits UI](https://bits-ui.com/) | Svelte | Unstyled, accessible components built for Svelte. |
| [Kobalte](https://kobalte.dev/) | Solid | Unstyled, accessible components built for Solid. |
| [Floating UI](https://floating-ui.com/) | Any | Positioning tooltips, popovers, and dropdowns correctly on screen. |
| [TanStack Table](https://tanstack.com/table) | Any | Building custom tables/datagrids with full control over markup. |
| [TanStack Virtual](https://tanstack.com/virtual) | Any | Rendering huge lists smoothly by only drawing visible rows. |
| [dnd kit](https://dndkit.com/) | React | Adding drag-and-drop to a React app without heavy deps. |
| [cmdk](https://cmdk.paco.me/) | React | Building a fast command-palette (⌘K) menu. |
| [Sonner](https://sonner.emilkowal.ski/) | React | Drop-in, nicely animated toast notifications for React. |
| [Downshift](https://github.com/downshift-js/downshift) | React | Building accessible autocomplete/combobox/select inputs from scratch. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## State & data fetching

State management tools hold onto data your app needs to remember; data-fetching tools handle pulling data from a server and keeping it fresh. Both solve the mess that shows up once several components need to share the same data or the same loading/error/caching logic. Think of it as a shared whiteboard the whole app can read and update, instead of everyone scribbling private notes.

**Start here:** Data fetching: TanStack Query. Client state: Zustand.

| Name | Works with | Best for |
|---|---|---|
| ⭐ [TanStack Query](https://tanstack.com/query) | React, Vue, Solid, Svelte, Angular | Default choice for fetching/caching server data in any framework. |
| ⭐ [Zustand](https://zustand.docs.pmnd.rs/) | React | Default choice for simple React state; minimal boilerplate. |
| [TanStack DB](https://tanstack.com/db) | Any | Sync-first apps that need a local reactive data store. |
| [SWR](https://swr.vercel.app/) | React | A lighter React-only alternative to TanStack Query. |
| [Apollo Client](https://www.apollographql.com/docs/react) | React | GraphQL APIs that want a full-featured client with caching. |
| [urql](https://github.com/urql-graphql/urql) | React, Vue, Svelte | A lighter, more extensible GraphQL client. |
| [Jotai](https://jotai.org/) | React | Small pieces of state you compose bottom-up (atoms). |
| [Valtio](https://valtio.dev/) | React | State that feels like plain mutable objects, via proxies. |
| [Redux Toolkit](https://redux-toolkit.js.org/) | Any | Large apps that want Redux's structure, official and batteries-included. |
| [MobX](https://mobx.js.org/) | Any | Observable state that updates the UI automatically on change. |
| [Legend-State](https://github.com/LegendApp/legend-state) | React | Fast, signal-based React state with built-in sync. |
| [Pinia](https://pinia.vuejs.org/) | Vue | The standard store solution for Vue apps. |
| [NgRx](https://ngrx.io/) | Angular | Reactive, Redux-style state management for Angular. |
| [XState](https://stately.ai/docs/xstate) | Any | Modeling complex flows explicitly as state machines. |
| [Preact Signals](https://github.com/preactjs/signals) | Preact, React | Fine-grained reactive values usable in Preact or React. |
| [Nano Stores](https://github.com/nanostores/nanostores) | Any | A tiny state manager for use across frameworks. |
| [nuqs](https://nuqs.dev/) | React | Storing UI state directly in the URL query string. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Forms & validation

Forms look simple until you handle every edge case yourself: required fields, async checks, nested inputs, error messages that update as you type. Forms and validation libraries handle that state and rule-checking for you instead of you wiring up onChange handlers by hand. It's like having an assistant flag a missing field before you hit submit, rather than you checking it every time.

**Start here:** Form state: React Hook Form. Schema validation: Zod.

| Name | Works with | Best for |
|---|---|---|
| ⭐ [React Hook Form](https://react-hook-form.com/) | React | Default choice for React forms; fast with little re-rendering. |
| ⭐ [Zod](https://zod.dev/) | Any | Default choice for schema validation; pairs with TypeScript everywhere. |
| [TanStack Form](https://tanstack.com/form) | React, Vue, Solid, Svelte, Angular | Type-safe form state shared across React, Vue, Solid, and more. |
| [Conform](https://conform.guide/) | React | Forms built around server actions and progressive enhancement. |
| [Formik](https://formik.org/) | React | An older, still-common React form library many codebases already use. |
| [VeeValidate](https://vee-validate.logaretm.com/) | Vue | Form validation for Vue apps. |
| [FormKit](https://formkit.com/) | Vue | A fuller Vue form framework with inputs and schema built in. |
| [Superforms](https://superforms.rocks/) | SvelteKit | Server- and client-validated forms in SvelteKit. |
| [Valibot](https://valibot.dev/) | Any | A smaller, more tree-shakeable alternative to Zod. |
| [ArkType](https://arktype.io/) | Any | Validation that mirrors TypeScript types almost 1:1. |
| [Yup](https://github.com/jquense/yup) | Any | An older, widely-used schema validator, often paired with Formik. |
| [Standard Schema](https://standardschema.dev/) | Any | A shared interface so Zod/Valibot/ArkType tools interoperate. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Routing

Routing is what decides which screen or page a user sees based on the URL in the address bar — like a receptionist who reads the address you typed and walks you to the right room. Any app with more than one "page" needs it so the back button, bookmarks, and page refreshes all keep working.

**Start here:** React: React Router (most tutorials and libraries assume it). Vue: Vue Router (official, ships with Vue).

| Name | Works with | Best for |
|---|---|---|
| ⭐ [React Router](https://reactrouter.com/) | React | Default React router; most tutorials and libraries assume it. |
| ⭐ [Vue Router](https://router.vuejs.org/) | Vue | Official router for Vue; use it by default. |
| [TanStack Router](https://tanstack.com/router) | React, Solid | Type-safe routing; catches route bugs at compile time. |
| [Wouter](https://github.com/molefrog/wouter) | React, Preact | Tiny router for small apps that want less code. |
| [Solid Router](https://github.com/solidjs/solid-router) | Solid | Official router for Solid apps. |
| [Angular Router](https://angular.dev/guide/routing) | Angular | Built into Angular; no separate install needed. |
| [Expo Router](https://docs.expo.dev/router/introduction/) | React Native | File-based routing for apps that target native and web. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Animation

Animation libraries make elements move smoothly on screen — sliding a menu in, fading a card, bouncing a button — instead of snapping instantly into place. Without one you'd hand-write frame-by-frame math yourself; reach for one whenever an interface should feel alive rather than static.

**Start here:** [Motion](https://motion.dev/) — handles most React/JS/Vue animation needs with sensible defaults.

| Name | Best for |
|---|---|
| ⭐ [Motion](https://motion.dev/) | General UI animation for React, Vue, or plain JS; easiest to start with (formerly Framer Motion). |
| [GSAP](https://gsap.com/) | Complex, precise timeline animations; industry standard, free to use. |
| [React Spring](https://www.react-spring.dev/) | Physics-based motion for React that feels natural, not linear. |
| [AutoAnimate](https://auto-animate.formkit.com/) | Animate list/DOM changes with one line, no config. |
| [Anime.js](https://animejs.com/) | Lightweight animations without a framework dependency. |
| [Theatre.js](https://www.theatrejs.com/) | Animate with a visual timeline editor, not just code. |
| [Lenis](https://lenis.darkroom.engineering/) | Smooth, weighted scrolling for a more polished feel. |
| [Barba.js](https://barba.js.org/) | Smooth transitions between pages on multi-page (non-SPA) sites. |
| [AOS](https://michalsnik.github.io/aos/) | Simple "animate when scrolled into view" effects. |
| [View Transitions API](https://developer.mozilla.org/en-US/docs/Web/API/View_Transition_API) | Native browser page/element transitions; no library to install. |
| [Lottie](https://airbnb.io/lottie/) | Play After Effects animations exported by designers, on web or mobile. |
| [Rive](https://rive.app/) | Interactive vector animations designers build and developers wire up. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## 3D, canvas & graphics

These tools let you draw and animate visuals beyond plain HTML — 3D scenes, games, freehand drawing — using the browser's canvas or WebGL/WebGPU under the hood. Reach for one when HTML and CSS alone can't do the job: a 3D product viewer, a game, a whiteboard, a physics simulation.

**Start here:** 3D: [Three.js](https://threejs.org/) — the standard, huge ecosystem and tutorials. Creative/2D: [p5.js](https://p5js.org/) — built for learning canvas coding.

| Name | Best for |
|---|---|
| ⭐ [Three.js](https://threejs.org/) | The standard for 3D on the web; most tutorials and jobs use it. |
| ⭐ [p5.js](https://p5js.org/) | Easiest way to start with creative/2D canvas coding; built for learning. |
| [React Three Fiber](https://r3f.docs.pmnd.rs/) | Three.js scenes written as React components. |
| [Drei](https://github.com/pmndrs/drei) | Common helpers/shortcuts for React Three Fiber, saves boilerplate. |
| [Threlte](https://threlte.xyz/) | Three.js for Svelte apps. |
| [TresJS](https://tresjs.org/) | Three.js for Vue apps. |
| [Babylon.js](https://www.babylonjs.com/) | Alternative to Three.js with more built-in tooling and an editor. |
| [PlayCanvas](https://playcanvas.com/) | Full game engine with a visual editor, WebGL/WebGPU. |
| [A-Frame](https://aframe.io/) | Build VR/AR scenes by writing HTML tags. |
| [PixiJS](https://pixijs.com/) | Fast 2D rendering for games and interactive graphics. |
| [Phaser](https://phaser.io/) | Full 2D game framework with physics, input, and asset loading built in. |
| [Matter.js](https://brm.io/matter-js/) | Add realistic 2D physics (gravity, collisions) to a page. |
| [Konva](https://konvajs.org/) | Interactive 2D shapes and drag-and-drop canvas apps. |
| [Fabric.js](https://fabricjs.com/) | Canvas as editable objects; good for image/design editors. |
| [Paper.js](http://paperjs.org/) | Vector graphics scripting on canvas. |
| [Excalidraw](https://github.com/excalidraw/excalidraw) | Drop a hand-drawn-style whiteboard into a React app. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Charts, maps & diagrams

These turn numbers and data into pictures — bar charts, line graphs, maps, flowcharts — so people can understand information at a glance instead of reading a spreadsheet. Use one whenever a page needs to show trends, comparisons, locations, or relationships visually.

**Start here:** Charts: [Chart.js](https://www.chartjs.org/) — simplest charting library for common chart types. Maps: [Leaflet](https://leafletjs.com/) — simple, huge community.

| Name | Best for |
|---|---|
| ⭐ [Chart.js](https://www.chartjs.org/) | Simplest charting library for common chart types; best starting point. |
| ⭐ [Leaflet](https://leafletjs.com/) | Simplest way to add an interactive map; huge community. |
| [D3](https://d3js.org/) | Full control over custom, bespoke visualizations; steeper learning curve. |
| [Apache ECharts](https://echarts.apache.org/) | Feature-rich interactive charts out of the box. |
| [Recharts](https://recharts.org/) | Chart components built for React apps. |
| [Nivo](https://nivo.rocks/) | Polished, ready-made React chart components. |
| [visx](https://airbnb.io/visx/) | Low-level chart building blocks for React, more control than Recharts. |
| [Unovis](https://unovis.dev/) | One charting API across React, Vue, Svelte, Angular. |
| [LayerChart](https://layerchart.com/) | Composable charts built for Svelte. |
| [ApexCharts](https://apexcharts.com/) | Interactive charts with good defaults, framework-agnostic. |
| [Plotly.js](https://plotly.com/javascript/) | Scientific, statistical, and 3D charts. |
| [Vega-Lite](https://vega.github.io/vega-lite/) | Describe charts declaratively in JSON instead of code. |
| [Observable Plot](https://observablehq.com/plot/) | Quick, concise charts for data exploration. |
| [uPlot](https://github.com/leeoniya/uPlot) | Very fast charts for large time-series data. |
| [MapLibre GL JS](https://maplibre.org/) | Open source vector maps with smooth WebGL rendering. |
| [deck.gl](https://deck.gl/) | Render huge datasets on a map using the GPU. |
| [React Flow](https://reactflow.dev/) | Build node-based editors/diagrams (flowcharts, pipelines) in React. |
| [Mermaid](https://mermaid.js.org/) | Write diagrams as text, like Markdown for flowcharts. |
| [Cytoscape.js](https://js.cytoscape.org/) | Visualize graphs and networks of connected nodes. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Icons

Icon sets give you ready-made small pictures — arrows, trash cans, hearts — for buttons and menus so you don't have to draw or hunt for your own SVGs. Grab one whenever your UI needs consistent, scalable icons instead of emoji or one-off image files.

**Start here:** [Lucide](https://lucide.dev/) — clean, actively maintained, easy React/Vue components.

| Name | Best for |
|---|---|
| ⭐ [Lucide](https://lucide.dev/) | Clean, consistent icons with easy React/Vue components; good default. |
| [Heroicons](https://heroicons.com/) | Matches Tailwind CSS styling out of the box. |
| [Tabler Icons](https://tabler.io/icons) | Huge free set (5000+) if Lucide doesn't have what you need. |
| [Phosphor Icons](https://phosphoricons.com/) | Multiple weights (thin to bold) for varied styles. |
| [Remix Icon](https://remixicon.com/) | Neutral style that fits most design systems. |
| [Iconoir](https://iconoir.com/) | Another large, free alternative icon set. |
| [Bootstrap Icons](https://icons.getbootstrap.com/) | Matches Bootstrap-based projects. |
| [Material Symbols](https://fonts.google.com/icons) | Google's variable icon font; fits Material Design apps. |
| [Radix Icons](https://www.radix-ui.com/icons) | Small, crisp icons for compact UI (15×15). |
| [Feather](https://feathericons.com/) | Simple, minimal icon style. |
| [Font Awesome](https://fontawesome.com/) | Very popular, huge community; free tier covers most needs. |
| [Simple Icons](https://simpleicons.org/) | Brand/company logos as SVG (GitHub, Twitter, etc.). |
| [SVGL](https://svgl.app/) | Browse and copy SVG logos. |
| [Iconify](https://iconify.design/) | Search and use icons from 200k+ across many sets, one API. |
| [unplugin-icons](https://github.com/unplugin/unplugin-icons) | Import any Iconify icon as a component automatically, no manual copy. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Fonts & typography

Typography tools help you pick, host, and size the text on your site — the letterforms themselves (fonts) and the spacing/scaling rules around them. Reach for them whenever the default system font looks too plain or you need text to scale consistently across screen sizes.

**Start here:** [Google Fonts](https://fonts.google.com/) — free, huge selection, easiest to add to any project.

| Name | Best for |
|---|---|
| ⭐ [Google Fonts](https://fonts.google.com/) | Easiest way to add a free custom font; huge selection. |
| [Fontsource](https://fontsource.org/) | Self-host Google/open fonts via npm instead of a CDN link. |
| [Bunny Fonts](https://fonts.bunny.net/) | Privacy-friendly drop-in replacement for Google Fonts. |
| [Fontshare](https://www.fontshare.com/) | Free, quality fonts; good for a less common look. |
| [Font Squirrel](https://www.fontsquirrel.com/) | Free fonts pre-licensed for commercial projects. |
| [Inter](https://rsms.me/inter/) | Popular, highly readable UI font, used almost everywhere. |
| [Geist](https://vercel.com/font) | Vercel's modern sans/mono pairing, good dev-tool look. |
| [JetBrains Mono](https://www.jetbrains.com/lp/mono/) | Free monospace font, good for code blocks/editors. |
| [Modern Font Stacks](https://modernfontstacks.com/) | Use fonts already on the user's device; nothing to download. |
| [Utopia](https://utopia.fyi/) | Calculate fluid font/spacing sizes that scale with screen width. |
| [Capsize](https://seek-oss.github.io/capsize/) | Fix inconsistent text spacing/line-height across fonts in CSS. |
| [Wakamai Fondue](https://wakamaifondue.com/) | Inspect what a font file actually supports before using it. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Accessibility

> Concepts behind this: [dev-knowledge → Frontend concepts](https://github.com/alwintwk/dev-knowledge#frontend-concepts)

Accessibility (a11y) tools help make sure a site works for people using screen readers, keyboard-only navigation, or who have low vision — not just a mouse and perfect eyesight. Use them to check and fix things like color contrast and missing labels, ideally before shipping rather than after a complaint.

**Start here:** [axe-core](https://github.com/dequelabs/axe-core) — the testing engine most other accessibility tools are built on.

| Name | Best for |
|---|---|
| ⭐ [axe-core](https://github.com/dequelabs/axe-core) | Automated accessibility testing engine; catches most common issues first. |
| [ARIA Authoring Practices Guide](https://www.w3.org/WAI/ARIA/apg/) | Reference for building accessible custom widgets (menus, dialogs) correctly. |
| [WCAG quick reference](https://www.w3.org/WAI/WCAG22/quickref/) | Look up the official accessibility guidelines/requirements. |
| [The A11Y Project](https://www.a11yproject.com/) | Beginner-friendly checklist and community resources. |
| [Inclusive Components](https://inclusive-components.design/) | Worked examples of accessible UI patterns. |
| [WAVE](https://wave.webaim.org/) | Visual, in-browser accessibility check, no setup. |
| [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) | Quickly check if text/background colors pass contrast rules. |
| [Pa11y](https://pa11y.org/) | Run accessibility checks from the command line/CI. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Runtimes & version managers

A runtime is the program that actually executes your JavaScript/TypeScript outside the browser, like on a server; a version manager lets you switch between different versions of that runtime per project. You need a runtime to run any Node-style backend code, and a version manager once you work on more than one project that needs different versions.

**Start here:** Runtime: [Node.js](https://nodejs.org/) — the default everywhere. Version manager: [mise](https://mise.jdx.dev/) — one tool for Node, Python, and more.

| Name | Best for |
|---|---|
| ⭐ [Node.js](https://nodejs.org/) | The default JS runtime; assume this unless you have a reason not to. |
| ⭐ [mise](https://mise.jdx.dev/) | Switch Node/Python/etc. versions per project automatically. |
| [Deno](https://deno.com/) | Runtime with TypeScript and security built in, less config. |
| [Bun](https://bun.sh/) | All-in-one runtime, bundler, and package manager; fast installs. |
| [workerd](https://github.com/cloudflare/workerd) | Run Cloudflare Workers code locally or self-hosted. |
| [LLRT](https://github.com/awslabs/llrt) | Very fast cold starts for small serverless functions. |
| [fnm](https://github.com/Schniz/fnm) | Fast, simple Node-only version switching. |
| [nvm](https://github.com/nvm-sh/nvm) | The original, most widely documented Node version manager. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Package managers & monorepos

A package manager installs and tracks the external code libraries your project depends on; monorepo tools help manage several related projects living in one repository together. Use a package manager on every JS project, and reach for a monorepo tool once you have multiple packages that share code and need to be built or versioned together.

**Start here:** Package manager: [npm](https://www.npmjs.com/) — comes preinstalled with Node.js. Monorepo: [Turborepo](https://turborepo.com/) — simplest way to manage multiple packages.

| Name | Best for |
|---|---|
| ⭐ [npm](https://www.npmjs.com/) | Comes with Node.js; simplest choice when starting out. |
| ⭐ [Turborepo](https://turborepo.com/) | Simple way to manage multiple packages in one repo. |
| [pnpm](https://pnpm.io/) | Faster installs, less disk space; easy upgrade once npm feels slow. |
| [Yarn](https://yarnpkg.com/) | Alternative to npm with workspaces built in. |
| [JSR](https://jsr.io/) | Registry built for publishing TypeScript packages directly. |
| [Verdaccio](https://verdaccio.org/) | Run a private npm registry inside a company/team. |
| [Nx](https://nx.dev/) | More powerful monorepo tooling for large, complex projects. |
| [moon](https://moonrepo.dev/) | Rust-based alternative for monorepo task running. |
| [Rush](https://rushjs.io/) | Enterprise-scale monorepo management from Microsoft. |
| [Lerna](https://lerna.js.org/) | Older tool for versioning/publishing packages in a monorepo. |
| [Changesets](https://github.com/changesets/changesets) | Track version bumps and changelogs across monorepo packages. |
| [Renovate](https://docs.renovatebot.com/) | Automatically opens PRs to update your dependencies. |
| [npm-check-updates](https://github.com/raineorshine/npm-check-updates) | One-off command to bump package.json versions to latest. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Build tools & bundlers

> Concepts behind this: [dev-knowledge → Frontend concepts (bundler, tree shaking)](https://github.com/alwintwk/dev-knowledge#frontend-concepts)

A bundler takes your separate JS/CSS/asset files and combines and optimizes them into what the browser actually loads; a build tool wraps that with a dev server, hot-reload, and other conveniences. You need one for any real frontend project — it's what turns your source code into something a browser can load quickly.

**Start here:** [Vite](https://vite.dev/) — the default modern build tool, fast dev server, minimal config.

| Name | Best for |
|---|---|
| ⭐ [Vite](https://vite.dev/) | The default choice for new frontend projects; fast, minimal config. |
| [Rolldown](https://rolldown.rs/) | Rust bundler now powering Vite under the hood. |
| [esbuild](https://esbuild.github.io/) | Extremely fast bundler, often used inside other tools. |
| [Rspack](https://rspack.rs/) | Drop-in, faster alternative to webpack. |
| [Rsbuild](https://rsbuild.rs/) | Rspack with sensible defaults, less config than raw Rspack. |
| [Turbopack](https://nextjs.org/docs/app/api-reference/turbopack) | Bundler built into Next.js for faster builds. |
| [Farm](https://www.farmfe.org/) | Rust-based alternative to Vite. |
| [Rollup](https://rollupjs.org/) | Best suited for bundling libraries, not apps. |
| [webpack](https://webpack.js.org/) | Older, highly configurable bundler; still common in existing projects. |
| [Parcel](https://parceljs.org/) | Zero-config bundler, good if you don't want to touch settings. |
| [tsdown](https://tsdown.dev/) | Bundle TypeScript libraries, built on Rolldown. |
| [tsup](https://github.com/egoist/tsup) | Bundle a TypeScript library with almost no config. |
| [unbuild](https://github.com/unjs/unbuild) | Library build tool used across the UnJS ecosystem. |
| [unplugin](https://unplugin.unjs.io/) | Write a build plugin once, works across Vite/Rollup/webpack/esbuild. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Languages & compilers

A programming language is the words you type; a compiler (or transpiler) is the translator that turns those words into something a browser or server can actually run. This section covers alternatives and companions to plain JavaScript — some bolt on safety features like types, others compile to fast machine code, and some let you run heavier languages like C, Rust, or Python inside a web page via WebAssembly, a format for running near-native-speed code in the browser.

**Start here:** TypeScript — nearly every modern JS project uses it; learn this before anything else here.

| Name | Best for |
|---|---|
| ⭐ [TypeScript](https://www.typescriptlang.org/) | Default for any serious JS project; catches bugs before runtime. |
| [TC39 proposals](https://github.com/tc39/proposals) | Curious what's coming to JavaScript next, not a tool you install. |
| [tsx](https://github.com/privatenumber/tsx) | Quick-run TypeScript scripts and prototypes without a build step. |
| [SWC](https://swc.rs/) | Faster builds under the hood; powers tools like Next.js. |
| [Babel](https://babeljs.io/) | Support older browsers or use bleeding-edge syntax today. |
| [Effect](https://effect.website/) | Large TypeScript apps needing robust error handling and concurrency control. |
| [Elm](https://elm-lang.org/) | Want a language that makes runtime crashes nearly impossible. |
| [ReScript](https://rescript-lang.org/) | Type safety with fast compiles, a good fit for React teams. |
| [Gleam](https://gleam.run/) | Type-safe language for Erlang-style concurrent, fault-tolerant systems. |
| [WebAssembly](https://webassembly.org/) | Run C, Rust, or Go code at near-native speed in-browser. |
| [AssemblyScript](https://www.assemblyscript.org/) | Already know TypeScript and want an easy path to WebAssembly. |
| [Emscripten](https://emscripten.org/) | Porting an existing C/C++ codebase or library to the web. |
| [Pyodide](https://pyodide.org/) | Run Python and its data science libraries directly in-browser. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Linting & formatting

A linter reads your code and flags mistakes or bad patterns before you run it, like a spellchecker for code. A formatter automatically rearranges spacing and style so every file looks the same, ending arguments about tabs vs spaces. Most teams wire both into git hooks, scripts that run automatically on commit, so bad code never lands in the repo.

**Start here:** Linting: ESLint. Formatting: Prettier — the long-standing defaults with the biggest ecosystems and most tutorials.

| Name | Best for |
|---|---|
| ⭐ [ESLint](https://eslint.org/) | The standard JS/TS linter; huge plugin ecosystem, works with any setup. |
| ⭐ [Prettier](https://prettier.io/) | Auto-formats code so teams stop arguing about style; set and forget. |
| [typescript-eslint](https://typescript-eslint.io/) | Add TypeScript-aware linting rules on top of ESLint. |
| [ESLint Stylistic](https://eslint.style/) | Keep formatting rules inside ESLint instead of a separate formatter. |
| [Biome](https://biomejs.dev/) | Want one fast tool instead of separate linter and formatter. |
| [Oxc (oxlint)](https://oxc.rs/) | Speed up linting on a large codebase; complements ESLint. |
| [dprint](https://dprint.dev/) | Need a fast, pluggable formatter outside the JS ecosystem too. |
| [Stylelint](https://stylelint.io/) | Linting CSS specifically, catching typos and bad practices. |
| [markdownlint](https://github.com/DavidAnson/markdownlint) | Keep documentation and README files consistently formatted. |
| [Knip](https://knip.dev/) | Find and remove dead code, unused files, and dependencies. |
| [publint](https://publint.dev/) | Sanity-check an npm package before publishing it. |
| [Are the Types Wrong?](https://arethetypeswrong.github.io/) | Verify a package's TypeScript types actually resolve for consumers. |
| [Husky](https://typicode.github.io/husky/) | Run checks automatically before every git commit or push. |
| [lint-staged](https://github.com/lint-staged/lint-staged) | Only lint the files you just changed, not the whole repo. |
| [Lefthook](https://github.com/evilmartians/lefthook) | Faster git hook manager for larger, multi-language repos. |
| [commitlint](https://commitlint.js.org/) | Enforce a consistent format for commit messages across the team. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Testing

Testing means running your code against expected outcomes automatically, instead of clicking through the app by hand every time to check nothing broke. Unit test tools check small pieces of logic in isolation; end-to-end (E2E) tools drive a real browser to click through your app the way a user would. Most apps end up needing at least one of each once they grow past a few pages.

> Concepts behind this: [dev-knowledge → Testing](https://github.com/alwintwk/dev-knowledge#testing)

**Start here:** Vitest for unit tests, Playwright for end-to-end — both are fast, modern defaults with great docs.

| Name | Best for |
|---|---|
| ⭐ [Vitest](https://vitest.dev/) | Fast unit tests for Vite-based projects; near drop-in Jest replacement. |
| ⭐ [Playwright](https://playwright.dev/) | Reliable end-to-end tests across Chrome, Firefox, and Safari. |
| [Jest](https://jestjs.io/) | Older, still-common choice for React/Node projects with a big ecosystem. |
| [Node.js test runner](https://nodejs.org/api/test.html) | Zero-dependency testing when you don't want to add a library. |
| [Mocha](https://mochajs.org/) | Flexible test runner for legacy or highly customized setups. |
| [Cypress](https://www.cypress.io/) | Debugging E2E tests visually with an interactive test runner. |
| [WebdriverIO](https://webdriver.io/) | Testing across many browsers plus real mobile devices. |
| [Puppeteer](https://pptr.dev/) | Scripting and automating Chrome specifically, not full cross-browser testing. |
| [Selenium](https://www.selenium.dev/) | Cross-language, cross-browser automation in large enterprise test suites. |
| [Testing Library](https://testing-library.com/) | Write component tests that mimic how real users interact. |
| [Storybook](https://storybook.js.org/) | Build and visually test UI components in isolation from the app. |
| [MSW](https://mswjs.io/) | Mock API responses in tests without touching real servers. |
| [BackstopJS](https://github.com/garris/BackstopJS) | Catch unintended visual/CSS changes with screenshot comparisons. |
| [Stryker](https://stryker-mutator.io/) | Check whether your tests actually catch bugs, not just run green. |
| [k6](https://k6.io/) | Load-test an API to see how it handles heavy traffic. |
| [Artillery](https://www.artillery.io/) | Load testing at larger scale with more scenario complexity. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Backend frameworks

A backend framework is the toolkit your server-side code runs on — it takes incoming requests, routes them to the right logic, and sends back a response. Picking one shapes how you write APIs, handle data, and structure a project for years to come. Most languages have their own popular options, so the right pick often depends on what language you already know or want to learn.

> Concepts behind this: [dev-knowledge → Backend & APIs](https://github.com/alwintwk/dev-knowledge#backend--apis)

> Full-stack meta-frameworks like Next.js, Nuxt, and SvelteKit also run server code. See [Meta-frameworks](#meta-frameworks).

**Start here:** JavaScript/TypeScript: Express — simplest start, and most tutorials use it (try Hono next for small, modern APIs). Python: FastAPI — fast to learn, great docs.

| Name | Language | Best for |
|---|---|---|
| ⭐ [Express](https://expressjs.com/) | JS/TS | Classic choice; simplest starting point with endless tutorials. |
| [Hono](https://hono.dev/) | JS/TS | Small, fast APIs that can deploy to any JS runtime, even edge. |
| ⭐ [FastAPI](https://fastapi.tiangolo.com/) | Python | Modern Python APIs with automatic docs and strong typing. |
| [Fastify](https://fastify.dev/) | JS/TS | Need more raw throughput than Express with similar simplicity. |
| [NestJS](https://nestjs.com/) | JS/TS | Large TypeScript teams wanting Angular-style structure and conventions. |
| [Koa](https://koajs.com/) | JS/TS | Lighter, more flexible middleware model from the Express creators. |
| [AdonisJS](https://adonisjs.com/) | JS/TS | Batteries-included TypeScript framework if you like Laravel's structure. |
| [Nitro](https://nitro.build/) | JS/TS | Deploy server code almost anywhere; also powers Nuxt under the hood. |
| [Elysia](https://elysiajs.com/) | JS/TS | Building on Bun and want end-to-end type safety. |
| [Encore](https://encore.dev/) | TS/Go | Want infrastructure like databases and tracing generated from your code. |
| [Django](https://www.djangoproject.com/) | Python | Content-heavy sites needing an admin panel and ORM out of the box. |
| [Flask](https://flask.palletsprojects.com/) | Python | Small Python APIs or scripts where you want minimal structure. |
| [Litestar](https://litestar.dev/) | Python | High-performance, modern Python APIs with strong typing built in. |
| [Gin](https://gin-gonic.com/) | Go | Simple, fast Go APIs with a huge community. |
| [Echo](https://echo.labstack.com/) | Go | Minimalist Go framework when you want to add pieces yourself. |
| [Fiber](https://gofiber.io/) | Go | Coming from Express and want that feel in Go. |
| [Axum](https://github.com/tokio-rs/axum) | Rust | Type-safe, async Rust APIs built on the Tokio runtime. |
| [Actix Web](https://actix.rs/) | Rust | Maximum raw performance for Rust APIs. |
| [Spring Boot](https://spring.io/projects/spring-boot) | Java/Kotlin | Enterprise Java apps needing a mature, well-supported ecosystem. |
| [Quarkus](https://quarkus.io/) | Java | Java apps that need to start fast, e.g. in containers. |
| [Ktor](https://ktor.io/) | Kotlin | Kotlin teams wanting an async server from JetBrains. |
| [ASP.NET Core](https://dotnet.microsoft.com/apps/aspnet) | C# | Already in the .NET ecosystem and want a fast, typed framework. |
| [Laravel](https://laravel.com/) | PHP | Full-featured PHP apps with the richest PHP ecosystem. |
| [Symfony](https://symfony.com/) | PHP | PHP projects needing reusable, enterprise-grade components. |
| [Ruby on Rails](https://rubyonrails.org/) | Ruby | Fast prototyping with strong conventions, a classic startup choice. |
| [Phoenix](https://www.phoenixframework.org/) | Elixir | Real-time features like chat or live updates on the Elixir VM. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## APIs, RPC & realtime

Once your frontend and backend are separate pieces, they need an agreed-upon way to talk — that's what this section covers: styles for defining APIs (REST, GraphQL, RPC), tools that keep both sides in sync on types, and options for realtime two-way connections like chat or live dashboards. Pick based on how tightly coupled your frontend and backend are, and whether you need data to update live.

> Concepts behind this: [dev-knowledge → Backend & APIs](https://github.com/alwintwk/dev-knowledge#backend--apis)

**Start here:** Type-safe APIs: tRPC (if both ends are TypeScript). Realtime: Socket.IO — the easiest way to add live updates.

| Name | Best for |
|---|---|
| ⭐ [tRPC](https://trpc.io/) | TypeScript frontend and backend in one repo; no schema needed. |
| ⭐ [Socket.IO](https://socket.io/) | Easiest way to add realtime features like chat or live updates. |
| [oRPC](https://orpc.unnoq.com/) | Want tRPC-style type safety plus auto-generated OpenAPI docs. |
| [ts-rest](https://ts-rest.com/) | Share one typed API contract between separate client and server repos. |
| [GraphQL](https://graphql.org/) | Clients need to fetch exactly the fields they want, nothing more. |
| [GraphQL Yoga](https://the-guild.dev/graphql/yoga-server) | Spin up a GraphQL server quickly with sensible defaults. |
| [Apollo Server](https://www.apollographql.com/docs/apollo-server) | Production GraphQL server with the biggest ecosystem and tooling. |
| [Pothos](https://pothos-graphql.dev/) | Build a GraphQL schema in code instead of writing SDL by hand. |
| [gRPC](https://grpc.io/) | High-throughput service-to-service communication, common in microservices. |
| [Connect](https://connectrpc.com/) | Want gRPC-style APIs that also work over plain HTTP/browsers. |
| [OpenAPI](https://www.openapis.org/) | Document a REST API in a standard, tool-friendly format. |
| [Hey API](https://heyapi.dev/) | Generate a typed TypeScript client straight from an OpenAPI spec. |
| [Orval](https://orval.dev/) | Generate typed clients and React Query hooks from OpenAPI. |
| [Scalar](https://github.com/scalar/scalar) | Nicer-looking, interactive docs page for an existing OpenAPI spec. |
| [Swagger UI](https://swagger.io/tools/swagger-ui/) | The long-standing, widely-supported default for interactive API docs. |
| [ws](https://github.com/websockets/ws) | Bare-bones WebSocket server when you want to skip a framework. |
| [PartyKit](https://www.partykit.io/) | Multiplayer or collaborative features deployed on Cloudflare's edge network. |
| [Hoppscotch](https://hoppscotch.io/) | Free, open source alternative to Postman for testing APIs. |
| [Bruno](https://www.usebruno.com/) | Prefer API collections stored as plain files in git. |
| [Insomnia](https://insomnia.rest/) | One client for testing REST, GraphQL, and gRPC APIs. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Databases, ORMs & search

A database stores your app's data permanently — users, posts, orders — so it survives a server restart. An ORM (object-relational mapper) lets you query that database using your programming language's normal objects and functions instead of writing raw SQL by hand. This section also covers search engines for fast text lookup and in-memory stores for caching repeated reads.

> Concepts behind this: [dev-knowledge → Databases](https://github.com/alwintwk/dev-knowledge#databases)

**Start here:** Database: PostgreSQL — the reliable default for almost any project. ORM: Prisma — the gentlest first ORM, with great docs (move to Drizzle once you know some SQL).

| Name | Best for |
|---|---|
| ⭐ [PostgreSQL](https://www.postgresql.org/) | The default relational database; reliable, feature-rich, huge community. |
| ⭐ [Prisma](https://www.prisma.io/) | Beginner-friendly ORM with a visual schema and strong docs. |
| [Drizzle ORM](https://orm.drizzle.team/) | Type-safe queries that read like SQL, minimal magic or overhead. |
| [MySQL](https://www.mysql.com/) | Widely-hosted relational database, common in shared or legacy hosting. |
| [MariaDB](https://mariadb.org/) | Open source MySQL alternative with the same familiar SQL. |
| [SQLite](https://www.sqlite.org/) | A whole database in one file; perfect for small apps and local dev. |
| [libSQL](https://github.com/tursodatabase/libsql) | SQLite with extra features and easy remote or edge replication. |
| [PGlite](https://pglite.dev/) | Run real Postgres in the browser or a test suite, no server. |
| [DuckDB](https://duckdb.org/) | Crunch large local datasets and analytics queries fast, no server. |
| [ClickHouse](https://clickhouse.com/) | Analytics on huge datasets where query speed really matters. |
| [MongoDB](https://www.mongodb.com/) | Flexible, schema-less document storage (source-available). |
| [Redis](https://redis.io/) | In-memory store for caching, sessions, and simple queues. |
| [Valkey](https://valkey.io/) | Open source Redis alternative after Redis's license change. |
| [pgvector](https://github.com/pgvector/pgvector) | Add AI/embedding similarity search directly inside Postgres. |
| [Kysely](https://kysely.dev/) | Want a typed query builder without full ORM abstraction. |
| [TypeORM](https://typeorm.io/) | Decorator-based, Java/NestJS-style ORM for TypeScript classes. |
| [MikroORM](https://mikro-orm.io/) | Need advanced patterns like Unit of Work and Identity Map. |
| [Sequelize](https://sequelize.org/) | Older Node.js codebases already built around it. |
| [Mongoose](https://mongoosejs.com/) | The standard way to model data when using MongoDB. |
| [SQLAlchemy](https://www.sqlalchemy.org/) | The standard, powerful SQL toolkit and ORM for Python. |
| [Meilisearch](https://www.meilisearch.com/) | Add fast, typo-tolerant search to a small-to-medium app. |
| [Typesense](https://typesense.org/) | Open source, self-hostable alternative to Algolia's search. |
| [BullMQ](https://bullmq.io/) | Queue background jobs like emails or processing in Node, via Redis. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Auth

Auth(entication) is how your app knows who's using it — logins, sessions, passwords, social sign-in — and authorization is what they're allowed to do once inside. Rolling this yourself is a common source of security bugs, so most apps lean on a library or hosted service instead of writing it from scratch.

> Concepts behind this: [dev-knowledge → Auth & identity (SSO, OAuth, JWT)](https://github.com/alwintwk/dev-knowledge#auth--identity)

**Start here:** Better Auth — modern, framework-agnostic TypeScript auth library with an active community.

| Name | Best for |
|---|---|
| ⭐ [Better Auth](https://www.better-auth.com/) | Full-featured, batteries-included auth for any TypeScript framework. |
| [Auth.js](https://authjs.dev/) | The standard choice if you're already using Next.js. |
| [OpenAuth](https://openauth.js.org/) | Want a standards-based, self-hosted auth server you control. |
| [Lucia](https://lucia-auth.com/) | Learn how sessions and auth actually work by building it yourself. |
| [Arctic](https://arcticjs.dev/) | Just need OAuth login buttons like Google or GitHub, nothing more. |
| [Passport.js](https://www.passportjs.org/) | Older Node.js apps already wired around its middleware pattern. |
| [SimpleWebAuthn](https://simplewebauthn.dev/) | Add passwordless login with passkeys, fingerprint, or face unlock. |
| [SuperTokens](https://supertokens.com/) | Self-hosted auth with prebuilt login UI, avoid vendor lock-in. |
| [Logto](https://logto.io/) | Open source hosted auth infrastructure built on the OIDC standard. |
| [Zitadel](https://zitadel.com/) | Apps serving multiple organizations or tenants needing isolated auth. |
| [Keycloak](https://www.keycloak.org/) | Enterprise self-hosted identity and access management, on-prem friendly. |
| [Authentik](https://goauthentik.io/) | Self-hosted single sign-on across your own internal tools. |
| [Ory](https://www.ory.sh/) | Open source identity infrastructure for large-scale, custom setups. |
| [CASL](https://casl.js.org/) | Fine-grained "who can do what" permission rules in your app. |
| [OpenFGA](https://openfga.dev/) | Complex permission systems modeled like Google's internal Zanzibar. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Backend as a service

Backend-as-a-service (BaaS) platforms bundle the pieces almost every app needs — a database, login/auth, file storage, realtime updates — behind one dashboard and SDK, so you skip building and hosting your own server. It's a fast way to get a real backend running without managing infrastructure yourself, like renting a fully-furnished apartment instead of building a house.

**Start here:** Supabase — open source, generous free tier, real Postgres underneath so you're not locked in.

| Name | Best for |
|---|---|
| ⭐ [Supabase](https://supabase.com/) | Open source Firebase alternative built on real Postgres; strong free tier. |
| [Appwrite](https://appwrite.io/) | Self-host the whole backend yourself instead of using a cloud vendor. |
| [PocketBase](https://pocketbase.io/) | Tiny single-file backend for small apps and side projects. |
| [Convex](https://www.convex.dev/) | Reactive database where frontend data updates live automatically. |
| [Nhost](https://nhost.io/) | Postgres plus GraphQL and auth in one managed platform. |
| [Hasura](https://hasura.io/) | Turn an existing database into a GraphQL or REST API instantly. |
| [InstantDB](https://www.instantdb.com/) | Realtime data synced straight into your frontend state. |
| [Parse Platform](https://parseplatform.org/) | Long-running open source backend if you want full control. |
| [Trigger.dev](https://trigger.dev/) | Background jobs and scheduled workflows written in TypeScript. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Hosting & deployment

Once your app works on your machine, hosting is how you put it on the internet where others can use it. Deployment is the process of getting your code from your machine onto that server, ideally automatically every time you push. Options range from one-click platforms that hide the servers entirely to self-hosting with tools like Docker, a way to package an app so it runs the same everywhere.

> Concepts behind this: [dev-knowledge → DevOps & cloud](https://github.com/alwintwk/dev-knowledge#devops--cloud)

**Start here:** Static/frontend sites: Vercel. Full app with a backend/database: Railway — both are near-instant to deploy to.

| Name | Best for |
|---|---|
| ⭐ [Vercel](https://vercel.com/) | Best default for Next.js and most frontend frameworks (free tier). |
| ⭐ [Railway](https://railway.com/) | Spin up an app plus a database in a few clicks (trial credit). |
| [Docker](https://www.docker.com/) | Package an app so it runs identically everywhere; base for most hosting. |
| [Coolify](https://coolify.io/) | Self-host your own Heroku/Netlify-style platform on any server. |
| [Dokploy](https://dokploy.com/) | Self-hosted PaaS for deploying apps and databases together. |
| [CapRover](https://caprover.com/) | Simple self-hosted deployment if Docker feels like too much setup. |
| [Kamal](https://kamal-deploy.org/) | Deploy containers straight to your own server with zero downtime. |
| [Caddy](https://caddyserver.com/) | Web server that sets up HTTPS automatically, minimal config. |
| [Nginx](https://nginx.org/) | The long-standing default reverse proxy and web server. |
| [Traefik](https://traefik.io/traefik/) | Reverse proxy built for containerized, cloud-native setups. |
| [GitHub Pages](https://pages.github.com/) | Free static site hosting straight from a GitHub repo. |
| [Cloudflare Pages](https://pages.cloudflare.com/) | Static/full-stack hosting on Cloudflare's global network (free tier). |
| [Netlify](https://www.netlify.com/) | Easiest static/JAMstack hosting with git-based deploys (free tier). |
| [Fly.io](https://fly.io/) | Run your app physically close to users around the world. |
| [Render](https://render.com/) | Simple cloud hosting for apps and databases (free tier). |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## CDNs

A CDN (content delivery network) is a set of servers spread around the world that store copies of your files, so a user loads them from a server near them instead of one far away, making sites load faster. In web dev, they're most often used to load a JavaScript library straight from a URL instead of installing and bundling it yourself.

**Start here:** jsDelivr — reliable, free, and covers both npm and GitHub.

| Name | Best for |
|---|---|
| ⭐ [jsDelivr](https://www.jsdelivr.com/) | Solid default free CDN for pulling in npm or GitHub files. |
| [unpkg](https://unpkg.com/) | Quick, simple CDN for any package published to npm. |
| [cdnjs](https://cdnjs.com/) | Cloudflare-backed free CDN for popular open source libraries. |
| [esm.sh](https://esm.sh/) | Load npm packages as ES modules directly, no build tools needed. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Analytics & monitoring

Analytics tells you who's visiting your site and what they're clicking — footprints on a dashboard instead of guesswork. Monitoring is the smoke detector for your app: it watches for errors, slow pages, or downtime so you find out before users complain. Reach for this once real people are using what you built, not while you're the only visitor.

> Concepts behind this: [dev-knowledge → Observability](https://github.com/alwintwk/dev-knowledge#observability--reliability)

**Start here:** [Plausible](https://plausible.io/) for traffic analytics — simple and privacy-friendly, no cookie banner; [Sentry](https://sentry.io/) for error tracking — free tier catches crashes before users report them; [Uptime Kuma](https://github.com/louislam/uptime-kuma) for uptime checks — self-hosted and free.

| Name | Best for |
|---|---|
| ⭐ [Plausible](https://plausible.io/) | Want lightweight, cookie-free analytics that's simple to set up and read. |
| ⭐ [Sentry](https://sentry.io/) | Need error and performance monitoring with alerts (free tier). |
| ⭐ [Uptime Kuma](https://github.com/louislam/uptime-kuma) | Want self-hosted uptime checks and status pages without paying for SaaS. |
| [Umami](https://umami.is/) | Alternative self-hosted analytics if you want to run your own instance. |
| [PostHog](https://posthog.com/) | Need product analytics, session replay, and feature flags in one tool. |
| [OpenTelemetry](https://opentelemetry.io/) | Want a vendor-neutral standard for traces, metrics, and logs across services. |
| [Grafana](https://grafana.com/oss/grafana/) | Need customizable dashboards to visualize metrics and logs from multiple sources. |
| [GlitchTip](https://glitchtip.com/) | Want self-hosted, Sentry-compatible error tracking without vendor lock-in. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Mobile & desktop

These tools let you take web skills, or a single codebase, and ship something that runs outside the browser — an icon on a phone's home screen or an app you double-click on a desktop. Instead of learning Swift, Kotlin, and C++ separately, most of these let one codebase target several platforms, like writing one letter and photocopying it for different mailboxes. Reach for this once "just a website" isn't enough — you need an app icon, offline use, or phone hardware like the camera.

**Start here:** [Expo](https://expo.dev/) for mobile — fastest path from React knowledge to a real iOS/Android app; [Electron](https://www.electronjs.org/) for desktop — most tutorials, works with plain HTML/CSS/JS; [PWABuilder](https://www.pwabuilder.com/) to turn an existing website into an installable app.

| Name | Best for |
|---|---|
| ⭐ [Expo](https://expo.dev/) | Want the fastest path from React knowledge to a real iOS/Android app. |
| ⭐ [Electron](https://www.electronjs.org/) | Know HTML/CSS/JS and want the fastest, most-documented way to ship a desktop app. |
| ⭐ [PWABuilder](https://www.pwabuilder.com/) | Have a website already and want to package it as an installable app fast. |
| [React Native](https://reactnative.dev/) | Building a mobile app in React and want the most-used framework and ecosystem. |
| [NativeWind](https://www.nativewind.dev/) | Already write Tailwind classes and want the same syntax in React Native. |
| [Tamagui](https://tamagui.dev/) | Need one UI kit that renders natively on mobile and on the web. |
| [Lynx](https://lynxjs.org/) | Curious about ByteDance's newer alternative to React Native for native UI. |
| [NativeScript](https://nativescript.org/) | Want native mobile apps using JavaScript without a React Native rewrite. |
| [Flutter](https://flutter.dev/) | Starting mobile from scratch and want one codebase for mobile, web, and desktop. |
| [Kotlin Multiplatform](https://kotlinlang.org/docs/multiplatform.html) | Already know Kotlin/Android and want to share logic across iOS too. |
| [.NET MAUI](https://dotnet.microsoft.com/apps/maui) | Coming from C#/.NET and want native cross-platform apps in that ecosystem. |
| [Capacitor](https://capacitorjs.com/) | Have an existing web app and want to wrap it as a native app. |
| [Ionic](https://ionicframework.com/) | Want a full mobile UI toolkit built on standard web technologies. |
| [Tauri](https://tauri.app/) | Want a small, fast desktop app and don't mind installing Rust. |
| [Wails](https://wails.io/) | Building a Go backend and want a lightweight desktop shell around it. |
| [Neutralinojs](https://neutralino.js.org/) | Want the smallest possible desktop app wrapper, lighter than Electron. |
| [Workbox](https://developer.chrome.com/docs/workbox) | Need offline support and caching for a PWA without hand-writing service workers. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Images & media

Unoptimized photos and videos are the single biggest reason pages feel slow — these tools compress, resize, convert, or generate lightweight stand-ins so pages load fast and still look good. It's like packing a suitcase efficiently instead of throwing clothes in loose: same content, far less space. Reach for these when a page feels sluggish, when you're handling user uploads, or when you need a placeholder while a big image loads.

**Start here:** [Squoosh](https://squoosh.app/) for quick image compression, no install needed; [SVGOMG](https://jakearchibald.github.io/svgomg/) for SVG cleanup with a simple web UI; [FFmpeg](https://ffmpeg.org/) for anything audio/video.

| Name | Best for |
|---|---|
| ⭐ [Squoosh](https://squoosh.app/) | Want a quick one-off image compression with visual before/after in the browser. |
| ⭐ [SVGOMG](https://jakearchibald.github.io/svgomg/) | Want to optimize an SVG by hand without installing anything. |
| ⭐ [FFmpeg](https://ffmpeg.org/) | Need to record, convert, or stream audio/video — the standard CLI tool for it. |
| [sharp](https://sharp.pixelplumbing.com/) | Resizing/converting images server-side in Node and want the fastest library. |
| [libvips](https://www.libvips.org/) | Processing huge images or high volume and need low memory usage. |
| [ImageMagick](https://imagemagick.org/) | Need a battle-tested CLI for scripted, bulk image editing and conversion. |
| [imgproxy](https://imgproxy.net/) | Want to resize images on the fly via URL params instead of pre-processing. |
| [Unpic](https://unpic.pics/) | Building responsive `<img>` components that work across frameworks and CDNs. |
| [SVGO](https://github.com/svg/svgo) | Automating SVG optimization in a build pipeline or CI. |
| [oxipng](https://github.com/shssoichiro/oxipng) | Need a fast, lossless PNG optimizer for a build step. |
| [ImageOptim](https://imageoptim.com/) | On a Mac and want a drag-and-drop lossless image compressor. |
| [BlurHash](https://blurha.sh/) | Want a tiny blurred placeholder while a photo loads. |
| [ThumbHash](https://evanw.github.io/thumbhash/) | Want a better placeholder than BlurHash, with transparency support. |
| [HandBrake](https://handbrake.fr/) | Want a GUI to transcode video files without learning FFmpeg's CLI. |
| [Vidstack](https://vidstack.io/) | Building a custom video/audio player UI in a modern framework. |
| [Plyr](https://plyr.io/) | Need a simple, accessible HTML5 player without much setup. |
| [hls.js](https://github.com/video-dev/hls.js) | Playing HLS live/adaptive streams in browsers that don't support it natively. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Performance & browser support

This category makes sure your site is fast and actually works on the browsers real visitors use, not just the one on your laptop. Performance tools measure load time and responsiveness — a stopwatch for your page; browser-support tools tell you whether a shiny new feature will silently break on someone's older phone. Check these before shipping, and again whenever a page starts feeling slow or you want to use a newer CSS/JS feature.

> Concepts behind this: [dev-knowledge → Performance](https://github.com/alwintwk/dev-knowledge#performance)

**Start here:** [Lighthouse](https://developer.chrome.com/docs/lighthouse) for a quick performance/SEO audit, built into Chrome; [Can I use](https://caniuse.com/) to check browser support before using a new feature; [bundlephobia](https://bundlephobia.com/) to check an npm package's size cost.

| Name | Best for |
|---|---|
| ⭐ [Lighthouse](https://developer.chrome.com/docs/lighthouse) | Want a free, built-in audit of performance, accessibility, and SEO in Chrome DevTools. |
| ⭐ [Can I use](https://caniuse.com/) | Checking if a CSS/JS feature is safe to use across browsers today. |
| ⭐ [bundlephobia](https://bundlephobia.com/) | Checking how much an npm package will bloat your bundle before installing it. |
| [Lighthouse CI](https://github.com/GoogleChrome/lighthouse-ci) | Want Lighthouse scores tracked automatically on every commit or PR. |
| [Unlighthouse](https://unlighthouse.dev/) | Need to Lighthouse-scan an entire site at once, not one page. |
| [PageSpeed Insights](https://pagespeed.web.dev/) | Want Google's lab and real-world field data for a public URL. |
| [WebPageTest](https://www.webpagetest.org/) | Need a deep, real-browser performance trace with waterfall charts. |
| [sitespeed.io](https://www.sitespeed.io/) | Want open source, self-hosted continuous performance monitoring. |
| [web-vitals](https://github.com/GoogleChrome/web-vitals) | Measuring real Core Web Vitals from actual visitors in production. |
| [Baseline](https://web.dev/baseline) | Quickly checking whether a web feature is safe across all major browsers. |
| [MDN browser-compat-data](https://github.com/mdn/browser-compat-data) | Need the raw compatibility data that powers MDN and Can I use. |
| [Browserslist](https://browsersl.ist/) | Sharing one target-browser list across Babel, Autoprefixer, and other build tools. |
| [Responsively App](https://responsively.app/) | Previewing a layout across many screen sizes side by side. |
| [pkg-size](https://pkg-size.dev/) | Checking an npm package's install size, not just its bundle size. |
| [rollup-plugin-visualizer](https://github.com/btd/rollup-plugin-visualizer) | Seeing what's bloating a Vite or Rollup bundle, visually. |
| [webpack-bundle-analyzer](https://github.com/webpack-contrib/webpack-bundle-analyzer) | Seeing what's bloating a webpack bundle, visually. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Placeholders & mock data

Before real data or a finished backend exists, you still need something to fill the screen while you build — fake photos, fake names, fake API responses that look and behave like the real thing. It's like fitting a dress on a mannequin before the actual model shows up. Reach for these early in a project, or whenever you're building a feature and don't want to wait on a teammate's API.

**Start here:** [Lorem Picsum](https://picsum.photos/) for placeholder photos; [Faker](https://fakerjs.dev/) for generating realistic fake data in code; [JSONPlaceholder](https://jsonplaceholder.typicode.com/) for a ready-made fake REST API.

| Name | Best for |
|---|---|
| ⭐ [Lorem Picsum](https://picsum.photos/) | Need quick random placeholder photos while building a layout, zero setup. |
| ⭐ [Faker](https://fakerjs.dev/) | Generating realistic fake names, emails, or addresses for seed data or tests. |
| ⭐ [JSONPlaceholder](https://jsonplaceholder.typicode.com/) | Want a free hosted fake REST API to test frontend code against instantly. |
| [placehold.co](https://placehold.co/) | Need a placeholder image at an exact custom size and color. |
| [Unsplash](https://unsplash.com/) | Need real free high-resolution photos instead of generic mock images. |
| [Pexels](https://www.pexels.com/) | Need free stock photos or videos for a demo or mockup. |
| [unDraw](https://undraw.co/) | Want free customizable illustrations instead of photos for empty states. |
| [DiceBear](https://www.dicebear.com/) | Need quick generated avatars for user profiles in a demo. |
| [DummyJSON](https://dummyjson.com/) | Want a fake API with realistic products, carts, and users pre-built. |
| [Random User](https://randomuser.me/) | Need randomly generated user profile data via an API call. |
| [json-server](https://github.com/typicode/json-server) | Want a full fake REST API you control from a local JSON file. |
| [Mockoon](https://mockoon.com/) | Prefer a desktop GUI to design and run mock APIs, no code. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## SEO, favicons & meta

This is about the small metadata details that decide whether your site looks polished when shared or found — the little tab icon, the preview card that shows up when you paste a link in Slack, and whether Google understands what your page is about. None of it is required to make the site work, but skipping it makes a project look unfinished. Set it up once you have a real domain and are ready to share the link publicly.

**Start here:** [RealFaviconGenerator](https://realfavicongenerator.net/) for favicons that work everywhere; [metatags.io](https://metatags.io/) to preview and generate your share-link meta tags; [Google Search Console](https://search.google.com/search-console) to monitor how Google sees your site.

| Name | Best for |
|---|---|
| ⭐ [RealFaviconGenerator](https://realfavicongenerator.net/) | Need one favicon that looks right on every browser, OS, and device. |
| ⭐ [metatags.io](https://metatags.io/) | Want to preview how a link card looks on Twitter/Facebook before sharing. |
| ⭐ [Google Search Console](https://search.google.com/search-console) | Want to see how Google actually indexes and ranks your site, for free. |
| [favicon.io](https://favicon.io/) | Making a quick favicon from text, an emoji, or an image. |
| [Maskable.app](https://maskable.app/) | Checking a PWA icon won't get cropped weird on Android. |
| [Open Graph protocol](https://ogp.me/) | Learning the tags behind rich link previews — the spec itself. |
| [Satori](https://github.com/vercel/satori) | Generating share-image (OG image) SVGs/PNGs dynamically from HTML/CSS. |
| [Schema.org](https://schema.org/) | Looking up the structured-data vocabulary search engines actually understand. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

## Lists of lists

Sometimes the fastest way to find a tool isn't a search engine, it's a hand-curated list someone already built and keeps updated. These "awesome lists" and directories collect the best libraries, APIs, and free services for a given topic so you don't have to hunt one by one. Use them when starting a project in an unfamiliar area and you want a trusted shortlist instead of scrolling search results.

**Start here:** [Awesome](https://github.com/sindresorhus/awesome) — the master list that links out to nearly every other curated list, including the framework-specific ones below.

| Name | Best for |
|---|---|
| ⭐ [Awesome](https://github.com/sindresorhus/awesome) | Want one master index linking to curated lists on almost any topic. |
| [Awesome React](https://github.com/enaqx/awesome-react) | Looking for curated React libraries, tools, and learning resources in one place. |
| [Awesome Vue](https://github.com/vuejs/awesome-vue) | Looking for curated Vue ecosystem resources in one place. |
| [Awesome Svelte](https://github.com/TheComputerM/awesome-svelte) | Looking for curated Svelte ecosystem resources in one place. |
| [Awesome Angular](https://github.com/PatrickJS/awesome-angular) | Looking for curated Angular ecosystem resources in one place. |
| [Awesome Node.js](https://github.com/sindresorhus/awesome-nodejs) | Looking for curated Node.js packages and resources in one place. |
| [Awesome TypeScript](https://github.com/dzharii/awesome-typescript) | Looking for curated TypeScript resources and tooling in one place. |
| [Awesome CSS](https://github.com/awesome-css-group/awesome-css) | Looking for curated CSS frameworks, tools, and learning resources. |
| [Awesome Web Components](https://github.com/web-padawan/awesome-web-components) | Looking for curated Web Components libraries and resources. |
| [Awesome Web Performance](https://github.com/davidsonfellipe/awesome-wpo) | Looking for curated web performance optimization resources. |
| [Awesome Self-Hosted](https://github.com/awesome-selfhosted/awesome-selfhosted) | Want free software you can run yourself instead of paying for SaaS. |
| [Public APIs](https://github.com/public-apis/public-apis) | Need a free public API to build a project or demo against. |
| [free-for.dev](https://free-for.dev/) | Looking for SaaS tools and cloud services with usable free tiers. |

<p align="right"><a href="#table-of-contents"><b>↥ Back to top</b></a></p>

---

## Contributing

PRs welcome. Keep entries open source or free. Each row says who it is **best for** (when you would choose it), in 15 words or fewer. Each section keeps its short intro and one **Start here** pick, marked ⭐.

## License

[CC0 1.0](LICENSE): public domain. Copy, share, and reuse freely.
