# disallow overwriting reserved keys (no-reservered-keys)

- :warning: This rule was **deprecated** and replaced by [no-reserved-keys](no-reserved-keys.md) rule.

This rule prevents to use reserved names from to avoid conflicts and unexpected behavior.

## Rule Details

:-1: Examples of **incorrect** code for this rule:

```js
export default {
  props: {
    $el: String
  },
  computed: {
    $on: {
      get () {
      }
    }
  },
  data: {
    _foo: null
  },
  methods: {
    $nextTick () {
    }
  }
}
```

## :wrench: Options

This rule has an object option:

`"reserved"`: [] (default) array of dissalowed names inside `groups`.

`"groups"`: [] (default) array of additional groups to search for duplicates.

### Example:

```json
{
  "vue/no-dupe-keys": [2, {
    "reserved": ["foo"]
  }]
}
```

:-1: Examples of **incorrect** code for this configuration

```js
export default {
  computed: {
    foo () {}
  }
}
```
