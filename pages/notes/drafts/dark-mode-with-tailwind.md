---
title: "Dark Mode with Tailwind"
aliases: ["dark-mode-with-tailwind", "Dark Mode"]
---

[[Dark Mode]] with [[Tailwind]] [[CSS]]

First you'll need to add a custom media query to your `tailwind.config.js` file.

```js
// tailwind.config.js

module.exports = {
  theme: {
    extend: {
      screens: {
        dark: { raw: '(prefers-color-scheme: dark)' }
      }
    }
  }
};
```

Then you may use the breakpoint in your HTML.

```js
<main class="bg-white dark:bg-black"></main>
```

For more detail see: [Vinkla's post](https://vinkla.dev/blog/dark-mode-with-tailwind)

Plugin `https://github.com/ChanceArthur/tailwindcss-dark-mode` didn't work for me 😫
