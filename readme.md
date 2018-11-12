# Co-op CSS Foundations [WIP]
Co-op CSS Foundations contains all the core CSS styles needed to build Co-op branded digital content.

The foundations set the basic Co-op look and feel - they should be included in all Co-op services.

## Installation
Install via `npm` or Yarn:
```bash
$ npm install @coopdigital/css-foundations --save
# OR
$ yarn add @coopdigital/css-foundations
```

## Usage
You can include CSS Foundations in your project by referencing it from your existing CSS via `@import` statement, i.e.:
```css
@import "node_modules/@coopdigital/css-foundations/dist/foundations.css";
```

If you use PostCSS in your build pipeline, you can reference the sources directly like so:
```css
@import "node_modules/@coopdigital/css-foundations/src/foundations.pcss";
```

If you use a `postcss-import` plugin, it gets even easier:
```css
@import "@coopdigital/css-foundations";
```

## Examples
Here's a bunch of examples, showing how you can integrate this CSS module in your project, based on most popular stacks of project. You can either use a post-processed and pre-built CSS form the `dist` directory, ot use PostCSS sources from the `src` dir.

The latter have certain dependencies, which should be consumed by your frontend toolkit to postprocess the CSS correctly.

### Vue.js
In Vue, you can just reference it from a global component like so:
```css
<style>
/* Import PostCSS source */
@import "~@coopdigital/css-foundations/src/foundations.pcss";
/* Import postprocessed distributable CSS */
@import "~@coopdigital/css-foundations/dist/foundations.css";
</style>
```

### React.js
TBD

### Webpack
TBD

## Development
CSS Foundations follows a modular architecture and as such is composed out of several CSS Modules. You are free to use either individual modules or load the entire framework into your project.

### Modules
- [x] Variables [`@coopdigital/foundations-vars`](https://github.com/coopdigital/foundations-vars)
- [x] Global [`@coopdigital/foundations-global`](https://github.com/coopdigital/foundations-global)
- [x] Typography [`@coopdigital/foundations-typography`](https://github.com/coopdigital/foundations-typography)
- [x] Colours [`@coopdigital/foundations-colors`](https://github.com/coopdigital/foundations-colors)
- [x] Buttons [`@coopdigital/foundations-buttons`](https://github.com/coopdigital/foundations-buttons)
- [x] Forms [`@coopdigital/foundations-forms`](https://github.com/coopdigital/foundations-forms)
- [ ] Tables
- [ ] Grid
- [ ] Layout
- [ ] Utilities & Helpers

### How to develop?
This package only serves as a master package for all individual CSS modules. Development should be done within individual package repositories, following general guidelines.
