# NuxtClientFallback errors

I want to use Nuxt's `NuxtClientFallback` component and build a wrapper component around it.
Unfortunately, when building a wrapper component around it, it does not behave as expected.

## Setup & start the app

Make sure to install the dependencies:

```
yarn install
yarn dev
```

Go to:

- http://localhost:3000/works -> expected behaviour
- http://localhost:3000/bugs -> bug behaviour
