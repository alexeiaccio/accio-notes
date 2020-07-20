---
title: 'Gatsby Remark Plugins'
aliases: ['gatsby-remark-plugins', 'Essential Plugins for Gatsby Remark']
---

[[Gatsby]] [[MDX]]

Swyx's [post](https://www.swyx.io/writing/gatsby-remark-essential-plugins)

```js
plugins: [
  {
    resolve: `gatsby-transformer-remark`,
    options: {
      plugins: [
        'gatsby-remark-autolink-headers',
        'gatsby-remark-prismjs',
        'gatsby-remark-copy-linked-file',
        'gatsby-remark-external-links',
        'gatsby-remark-images',
        'gatsby-remark-numbered-footnotes',
        'gatsby-remark-social-cards',
        'gatsby-remark-embedder'
    }
  }
]
```

Also:

- [x] `gatsby-remark-autolink-headers`
- [x] `gatsby-remark-prismjs`
- [x] `gatsby-remark-copy-linked-file`
- [ ] `gatsby-remark-external-links`
- [x] `gatsby-remark-images`
- [x] `gatsby-remark-numbered-footnotes`
- [ ] `gatsby-remark-social-cards`
- [x] `gatsby-mdx-embed` not `gatsby-remark-embedder`
- [x] `gatsby-remark-smartypants` [Github](https://github.com/gatsbyjs/gatsby/tree/master/packages/gatsby-remark-smartypants)
- [ ] `gatsby-remark-embed-figma` [Github](https://github.com/stagfoo/gatsby-remark-embed-figma)
- [ ] replace `gatsby-remark-prismjs` with `prism-react-renderer` [Post](https://prince.dev/blog/prism-react-renderer)
  - [ ] or `gatsby-remark-shiki-twoslash` [Github](https://github.com/microsoft/TypeScript-Website/tree/v2/packages/gatsby-remark-shiki-twoslash)
  - [ ] with some [Theme](https://github.com/octref/shiki/blob/master/packages/themes/README.md)

Also:

https://github.com/remarkjs/remark/blob/master/doc/plugins.md
https://github.com/rehypejs/rehype/blob/master/doc/plugins.md

```js
// gatsby-config.js
module.exports = {
  plugins: [
    {
      resolve: `gatsby-plugin-mdx`,
      options: {
        remarkPlugins: [require('remark-abbr')],
        rehypePlugins: [require("rehype-slug")],
      },
    },
  ],
}
```