# nuxt-clipboard

> A "copy to clipboard" module for Nuxt.js using [vue-clipboard2](https://github.com/Inndy/vue-clipboard2)

## Setup
- Add `nuxt-clipboard` dependency using yarn or npm to your project
- Add `nuxt-clipboard` to `modules` section of `nuxt.config.js`

```js
export default {
     modules: [
      'nuxt-clipboard',
     ],
     clipboard: {
       autoSetContainer: true  
     }
}
```

## Usage
You can use **$copyText** in almost any context using `app.$copyText` or `this.$copyText` (Including store actions).

See [vue-clipboard2 official docs](https://github.com/Inndy/vue-clipboard2) for more usage information.

```js
export default {
  methods: {
    async copySomething(text) {
      try {
        await this.$copyText(text);
      } catch (e) {
        console.error(e);
      }
    },
  },
};
```

## License

[The MIT License (MIT)](./LICENSE.md)

Copyright (c) Chantouch Sek
