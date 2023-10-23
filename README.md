# nuxt-i18n-reproduction
Reproduction for https://github.com/nuxt-modules/i18n/issues/2491

```
> cd ./i18n-app
> npm install
```

This should throw an error

```
npm ERR!  ERROR  No lockfile found from ...\i18n-reproduction\i18n-app\node_modules\@skoenfeld\i18n-layer
npm ERR!
npm ERR!   at resolveLockfile (.../i18n-reproduction/i18n-app/node_modules/pkg-types/dist/index.mjs:122:9)
npm ERR!   at async getPackageManagerType (.../i18n-reproduction/i18n-app/node_modules/@nuxtjs/i18n/dist/module.mjs:108:26)
```


- i18n-app is the app and has the dependency `"@skoenfeld/i18n-layer": "0.0.2"`
- i18n-layer is the package [@skoenfeld/i18n-layer](https://www.npmjs.com/package/@skoenfeld/i18n-layer) and has the `"@nuxtjs/i18n": "^8.0.0-rc.5"` dependency
- @skoenfeld/i18n-layer is the published package
