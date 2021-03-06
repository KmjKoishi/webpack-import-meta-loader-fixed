# Webpack Helpers

Webpack loader for supporting `import.meta` in webpack.

> Part of [Open Web Components](https://github.com/open-wc/open-wc/): guides, tools and libraries for modern web development and web components

[![CircleCI](https://circleci.com/gh/open-wc/open-wc.svg?style=shield)](https://circleci.com/gh/open-wc/open-wc)
[![BrowserStack Status](https://www.browserstack.com/automate/badge.svg?badge_key=M2UrSFVRang2OWNuZXlWSlhVc3FUVlJtTDkxMnp6eGFDb2pNakl4bGxnbz0tLUE5RjhCU0NUT1ZWa0NuQ3MySFFWWnc9PQ==--86f7fac07cdbd01dd2b26ae84dc6c8ca49e45b50)](https://www.browserstack.com/automate/public-build/M2UrSFVRang2OWNuZXlWSlhVc3FUVlJtTDkxMnp6eGFDb2pNakl4bGxnbz0tLUE5RjhCU0NUT1ZWa0NuQ3MySFFWWnc9PQ==--86f7fac07cdbd01dd2b26ae84dc6c8ca49e45b50)
[![Renovate enabled](https://img.shields.io/badge/renovate-enabled-brightgreen.svg)](https://renovatebot.com/)

## Note

This is NOT an optimal solution e.g. it may slow down your build a little.
However as currently `import.meta` results in an webpack parse error using a loader is probably the only thing we can do for now.
For details see

- [https://github.com/webpack/webpack/issues/6719](https://github.com/webpack/webpack/issues/6719)
- [https://github.com/Polymer/tools/issues/518](https://github.com/Polymer/tools/issues/518)

If webpack fixed that parse error import.meta will probably work out of the box.
If not then a babel plugin (that can work with AST) will be a better solution.

## Manual Setup

- `yarn add @open-wc/webpack-import-meta-loader`
- Add this to your webpack config

```js
module: {
  rules: [
    {
      test: /\.js$/,
      loader: require.resolve('@open-wc/webpack-import-meta-loader'),
    },
  ],
},
```
