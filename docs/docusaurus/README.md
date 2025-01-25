# docusaurus

- https://docusaurus.io/
- [plugin-pwa](https://docusaurus.io/docs/api/plugins/@docusaurus/plugin-pwa)
- [katex](https://katex.org/)
- [math-equations](https://docusaurus.io/docs/markdown-features/math-equations)
- [Client API](https://docusaurus.io/docs/docusaurus-core)
- By default, any Markdown or JavaScript file starting with _ will be ignored and no routes will be created for that file (see the exclude option).

```md
---
sidebar_position: 1
sidebar_label: Algorithm
sidebar_class_name: green
description: Create a doc page with rich content.
id: doc-with-tags
title: A doc with tags
tags: 
  - Easy
slug: /
---
```

## setup project

```shell
# setup project
npx create-docusaurus@latest my-website classic --typescript

# setup math
# https://docusaurus.io/docs/markdown-features/math-equations
npm install --save remark-math@6 rehype-katex@7
```
