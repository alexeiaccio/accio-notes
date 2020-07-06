---
title: 'Gatsby Reload'
aliases: ['gatsby-reload', 'Dark Mode']
---

Try to use `gatsby-plugin-node-reload` ([Github](https://github.com/d4rekanguok/gatsby-plugin-node-reload)) for reloading [[Gatsby]] development process when I make some change in my notes.

## Install

```bash
yarn add gatsby-plugin-node-reload
```

```js
// gatsby-config.js

module.exports = {
  plugins: [
    (resolve: 'gatsby-plugin-node-reload'),
    (options: {
      watch: ['./directory-to-watch', './file-to-watch.js'],
    }),
  ],
}
```

It was very strange...

Also: tried add to `gatsby-config.js`.
This one works, but at Brain [[Gatsby Theme]] changes didn't apply. Because of the Theme read files from filesystem directly.
Need to fork it and use `gatsby-source-filesystem`.

```js
// gatsby-config.js

{
  resolve: `gatsby-source-filesystem`,
  options: {
    name: `notes`,
    path: `${__dirname}/content/notes`,
  },
},

```
