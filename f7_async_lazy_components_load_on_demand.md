# Async Lazy Components
## With Webpack it is possible to load page components on demand, it is possible with F7's async route, for example:

```js
{
  path: '/about',
  async(routeTo, routeFrom, resolve, reject) {
    // dynamic import component; returns promise
    const vueComponent = () => import('./pages/about.vue');
    // resolve promise
    vueComponent().then((vc) => {
      // resolve with component
      resolve({ component: vc.default })
    });
  } ,
},
```
