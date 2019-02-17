# nuxt-external-resource-loading-issue

> Nuxt.js project

This project was created using [create-nuxt-app](https://github.com/nuxt/create-nuxt-app).

This project was created in order to demo the following bug:
- https://github.com/nuxt/nuxt.js/issues/3396
- https://github.com/nuxt/nuxt.js/issues/3872

I created an issue in the Nuxt community forum, which references this repo: https://cmty.app/nuxt/nuxt.js/issues/c8677

## Steps to reproduce

### Case 1

1. Launch the app via `npm run dev` and open it up in your browser.
2. Click the "Test 1" link.
3. The following error will appear in your console:
```
TypeError: window.jQuery is not a function
  at VueComponent.mounted (test-1.js:34)
```
4. Refresh the page.
5. Everything will load correctly.
6. Click the "Home" link.
7. Click the "Test 1" link.
8. Everything will load correctly.
9. Click the "Home" link.
10. Refresh the page.
11. Click the "Test 1" link.
12. The following error will appear in your console:
```
TypeError: window.jQuery is not a function
  at VueComponent.mounted (test-1.js:34)
```
13. Refresh the page.
14. Everything will load correctly.

### Case 2

1. Launch the app via `npm run dev` and open it up in your browser.
2. Click the "Test 2" link.
3. The "(CDN script has loaded)" message will not be appended to the `<h1>` element.
4. Refresh the page.
5. The "(CDN script has loaded)" message will appear inside the `<h1>`.
6. Click the "Home" link.
7. Click the "Test 2" link.
8. The "(CDN script has loaded)" message will appear inside the `<h1>`.
9. Click the "Home" link.
10. Refresh the page.
11. Click the "Test 2" link.
12. The "(CDN script has loaded)" message will not be appended to the `<h1>` element.
13. Refresh the page.
14. The "(CDN script has loaded)" message will appear inside the `<h1>`.

## Build Setup

``` bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, checkout [Nuxt.js docs](https://nuxtjs.org).
