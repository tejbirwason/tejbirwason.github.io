---
title: 'Prettier and Minified Code'
date: 2023-08-11
---

Today, I learned that [Prettier](https://prettier.io/), the popular code formatter, can handle minified JavaScript code and try to format it into a readable form. However, there are some things to be aware of:

- **Performance Concerns**: Prettifying large minified files (e.g., libraries) can be time-consuming.
- **Accuracy**: Minified code might not always format cleanly due to certain minification tricks.
- **Original Structure**: Prettified minified code won't necessarily match the original code structure. Minification often renames variables and changes the code's structure.
- **Configuration**: If using automated tools that trigger Prettier (like on save or commit), consider configuring them to ignore `.min.js` files to avoid performance hits.

In practice, if the goal is to understand minified code, it's usually better to find the unminified source or use a source map. Prettier is great, but it's designed more for consistent formatting than for reversing minification.
