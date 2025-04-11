# consistent-list-newline

Enforce consistent line breaks inside braces of object/array/named imports/exports and function parameters.

## Rule Details

<!-- eslint-skip -->
```js
// 👎 bad
const foo = {
  bar: 'baz', qux: 'quux',
  fez: 'fum'
}
```

<!-- eslint-skip -->
```js
// 👍 good
const foo = {
  bar: 'baz',
  qux: 'quux',
  fez: 'fum'
}

// 👍 good
const foo = { bar: 'baz', qux: 'quux', fez: 'fum' }
```

## Options

This rule has either a string option:

- "consistent" (default) requires consistent usage of linebreaks between properties or items. It will check the newline style of the **first** property or item and apply to the rest of the properties or items.
- "always" requires line breaks between properties or items
- "never" disallows line breaks between properties or items

## Rule Conflicts

This rule might conflicts with the [object-curly-newline](https://eslint.org/docs/rules/object-curly-newline). You can turn if off.

```ts
export default {
  rules: {
    'object-curly-newline': 'off',
  }
}
```
