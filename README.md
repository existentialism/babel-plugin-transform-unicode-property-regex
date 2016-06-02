# babel-plugin-transform-unicode-property-regex [![Build status](https://travis-ci.org/mathiasbynens/babel-plugin-transform-unicode-property-regex.svg?branch=master)](https://travis-ci.org/mathiasbynens/babel-plugin-transform-unicode-property-regex)

Compile [Unicode property escapes](https://github.com/mathiasbynens/regexpu-core/blob/master/property-escapes.md) (`\p{}` and `\P{…}`) in Unicode regular expressions to ES5 or ES6 that works in today’s environments.

**Note:** the Unicode property escape syntax is non-standard and may or may not reflect what eventually gets specified.

## Installation

```sh
$ npm install babel-plugin-transform-unicode-property-regex
```

## Usage

### Via `.babelrc` (recommended)

`.babelrc`

```json
{
  "plugins": ["transform-unicode-property-regex"]
}
```

### Via CLI

```sh
$ babel --plugins transform-unicode-property-regex script.js
```

### Via Node.js API

```js
require('babel-core').transform(code, {
  'plugins': ['transform-unicode-property-regex']
});
```

To transpile to ES6/ES2015:

```js
require('babel-core').transform(code, {
  'plugins': [
    ['transform-unicode-property-regex', { 'useUnicodeFlag': true }]
  ]
});
```

## Author

| [![twitter/mathias](https://gravatar.com/avatar/24e08a9ea84deb17ae121074d0f17125?s=70)](https://twitter.com/mathias "Follow @mathias on Twitter") |
|---|
| [Mathias Bynens](https://mathiasbynens.be/) |

## License

This code is available under the [MIT](https://mths.be/mit) license.
