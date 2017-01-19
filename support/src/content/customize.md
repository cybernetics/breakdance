---
title: Customize
---

Don't like the defaults used in breakdance? Need to convert custom HTML elements?

With breakdance you can control how any HTML element is converted to markdown, or even how a specific element with certain attributes is converted. It's easy to override any defaults, or add support for custom elements, attributes or options.


## Customizing breakdance

**breakdance** is pretty hackable if you need more than the [provided options](options.html). You can override built-in renderers, create custom renderers for custom HTML tags, or create plugins that "bundle" together your commonly used customizations.

## AST

TODO


## Node

TODO


## Compilers (visitors)

Breakdance "compilers" are visitor functions that are called on specific AST nodes at render time. For example, the `text` compiler is called on nodes with the `text` type.

Override built-in compilers.

- **bos**:
- **html tags**:
  * tag name:
  * `.open`:
  * `.close`:
- **eos**:

### .set

Override an existing compiler, or register a new one.

```js
breakdance.set('html-tag-name', function(node, nodes, i) {

});
```

**Example**

```js
breakdance.set('pre', function(node, nodes, i) {

});
breakdance.set('pre.open', function(node, nodes, i) {

});
breakdance.set('pre.close', function(node, nodes, i) {

});
```

### Plugins

```js
breakdance.use(function() {

});
```

## API

### .isInside
