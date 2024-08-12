# A Simple Experiment to get Tailwind working with SvelteKit

## Creation
```bash
pnpm create svelte@latest sveltekit-tailwind
cd sveltekit-tailwind
pnpm i -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

## Postcss config file:

```bash
# postcss.config.js
export default {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
}

```

## Tailwind config file:

```bash
# tailwind.config.js
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    './src/**/*.{svelte,html,js,ts}',
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}

```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.
