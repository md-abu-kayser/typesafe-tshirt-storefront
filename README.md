# TypeSafe T-Shirt Storefront - React + TypeScript + Tailwind

<!-- MIT License -->

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](./LICENSE)


<!-- HTML & CSS -->

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)

<!-- Styling / PostCSS -->

[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?logo=tailwindcss&logoColor=white)](https://tailwindcss.com/docs/)
[![PostCSS](https://img.shields.io/badge/PostCSS-efefef?logo=postcss&logoColor=black)](https://postcss.org/)

<!-- Languages & Web Standards -->

[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![ECMAScript Spec](https://img.shields.io/badge/ECMAScript-262-7A0BC0?logo=ecmascript&logoColor=white)](https://www.ecma-international.org/publications-and-standards/standards/ecma-262/)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178c6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/docs/)

<!-- Infra & Runtime -->

[![Node.js](https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://react.dev/)

<!-- Linting & Formatting -->

[![ESLint](https://img.shields.io/badge/ESLint-4B32C3?logo=eslint&logoColor=white)](https://eslint.org/docs/latest/)
[![Prettier](https://img.shields.io/badge/Prettier-2B3A42?logo=prettier&logoColor=white)](https://prettier.io/docs/)

<!-- Bundler -->

[![Vite](https://img.shields.io/badge/Vite-646cff?logo=vite&logoColor=white)](https://vite.dev/)

## Plain docs links

- HTML (MDN) docs: [https://developer.mozilla.org/en-US/docs/Web/HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- CSS (MDN) docs: [https://developer.mozilla.org/en-US/docs/Web/CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
- Tailwind CSS docs: [https://tailwindcss.com/docs/](https://tailwindcss.com/docs/)
- PostCSS docs / postcss.config: [https://postcss.org/](https://postcss.org/)
- JavaScript (MDN) docs: [https://developer.mozilla.org/en-US/docs/Web/JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- ECMAScript (spec, ECMA-262) docs: [https://www.ecma-international.org/publications-and-standards/standards/ecma-262/](https://www.ecma-international.org/publications-and-standards/standards/ecma-262/)
- TypeScript docs: [https://www.typescriptlang.org/docs/](https://www.typescriptlang.org/docs/)
- Node.js docs: [https://nodejs.org/](https://nodejs.org/)
- React docs: [https://react.dev/](https://react.dev/)
- ESLint docs: [https://eslint.org/docs/latest/](https://eslint.org/docs/latest/)
- Prettier docs: [https://prettier.io/docs/](https://prettier.io/docs/)
- Vite docs: [https://vite.dev/](https://vite.dev/)

---

A small, production-ready React + Vite storefront demonstrating component architecture, typed state management with TypeScript, Tailwind CSS styling, and client-side routing. This project is ideal as a portfolio piece or a starter template for e-commerce UI experiments.

- Clean component composition (Parent / Child communication)
- Strongly-typed props and models via TypeScript ([src/types/index.ts](src/types/index.ts))
- Vite dev experience with HMR ([vite.config.ts](vite.config.ts))
- Tailwind CSS utility styling ([tailwind.config.js](tailwind.config.js))
- Local JSON data source for product catalog ([public/tshirts.json](public/tshirts.json))

## Quick links to notable items

- App entry: [src/main.tsx](src/main.tsx) - router and data loader
- Root layout: [src/components/Layout/Main.tsx](src/components/Layout/Main.tsx) (`Main`)
- Pages / components:
  - [`Home`](src/components/Home/Home.tsx) - product listing and cart state
  - [`Tshirt`](src/components/Tshirt/Tshirt.tsx) - product card component
  - [`Cart`](src/components/Cart/Cart.tsx) - cart UI and conditional rendering examples
  - [`Header`](src/components/Header/Header.tsx) - navigation
  - [`Grandpa`](src/components/Grandpa/Grandpa.tsx) - demo of prop drilling across family components
- Types: [`TShirt`](src/types/index.ts), [`CartItem`](src/types/index.ts), and props interfaces ([src/types/index.ts](src/types/index.ts))
- Static data: [public/tshirts.json](public/tshirts.json)
- App shell: [src/App.tsx](src/App.tsx) and [index.html](index.html)
- Project manifest: [package.json](package.json)

## Tech stack

- Framework: React 
- Tooling: Vite
- Language: TypeScript (strict)
- Styling: Tailwind CSS + a few CSS modules
- Notifications: react-hot-toast
- Routing: react-router-dom v6

### Getting started (fast)

1. **Install dependencies**

```bash
   npm install
```

2. **Run dev server (hot reload)**

```bash
   npm run dev
```

3. **Build for production**

```bash
   npm run build
```

4. **Preview production build locally**

```bash
   npm run preview
```

Other useful scripts: `npm run type-check`, `npm run lint` - see [package.json](package.json).

## How it works - high level

- The router is configured in [src/main.tsx](src/main.tsx). The `/` route loads product data from the static JSON file ([public/tshirts.json](public/tshirts.json)) and renders the [`Home`](src/components/Home/Home.tsx) page.
- [`Home`](src/components/Home/Home.tsx) uses a local React state for the cart (typed as [`CartItem[]`](src/types/index.ts)). Adding/removing items demonstrates pure-state updates and conditional UI patterns.
- UI components are intentionally small and focused (see [`Tshirt`](src/components/Tshirt/Tshirt.tsx) and [`Cart`](src/components/Cart/Cart.tsx)) to demonstrate reusability and composition.
- Type contracts for components are centralized in [src/types/index.ts](src/types/index.ts).

## Project structure

- index.html
- public/
  - [tshirts.json](public/tshirts.json)
- src/
  - [main.tsx](src/main.tsx)
  - [App.tsx](src/App.tsx)
  - components/
    - Layout/[Main.tsx](src/components/Layout/Main.tsx)
    - Home/[Home.tsx](src/components/Home/Home.tsx)
    - Tshirt/[Tshirt.tsx](src/components/Tshirt/Tshirt.tsx)
    - Cart/[Cart.tsx](src/components/Cart/Cart.tsx)
    - Header/[Header.tsx](src/components/Header/Header.tsx)
    - Grandpa/[Grandpa.tsx](src/components/Grandpa/Grandpa.tsx)
    - (other family-demo components...)
  - types/[index.ts](src/types/index.ts)
- config: [vite.config.ts](vite.config.ts), [tailwind.config.js](tailwind.config.js), [postcss.config.js](postcss.config.js)

## Customizing data

- Edit [public/tshirts.json](public/tshirts.json) to add/remove products. The loader in [src/main.tsx](src/main.tsx) fetches this file.

## Why this project stands out

- Real-world patterns: routing + data loaders, typed props, component composition.
- Clean separation of concerns and easy-to-extend structure for additional features (pagination, product details, cart persistence).
- Production-grade tooling (Vite, TypeScript, ESLint, Tailwind).

### Contributing

- All contributions are welcome. Open an issue or PR.
- Run linters and type checks before submitting:
  - Type check: `npm run type-check`
  - Lint: `npm run lint`

### License

- This project is licensed under the terms of the **[MIT License](./LICENSE)**.
- You may replace or update the license as needed for client or proprietary projects.

---

### Contact & Maintainer

- **Project:** _typesafe-tshirt-storefront_
- **Name:** Md Abu Kayser - Full-Stack Engineer
- **Maintainer:** [md-abu-kayser](https://github.com/md-abu-kayser)
- **Email:** [abu.kayser.official@gmail.com](mailto:abu.kayser.official@gmail.com)
- **GitHub:** [github.com/abu.kayser-official](https://github.com/md-abu-kayser)

If you’d like this README tailored for a specific purpose - such as **hiring managers**, **open-source contributors**, or **client deliverables** - feel free to request a custom tone or format.

---

It’s designed to be **clean, well-structured**, and **pleasant to explore** - perfect for portfolio showcases and practice demos.
**Thank you for reviewing this project!**  

---
