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



![image](https://github.com/user-attachments/assets/65230f5d-5302-4434-b8d9-7ee767582e2c)

`/works` page
When opening this page
- SSR:
   - component A : renders an error message ✔️
   - components B & C : render their defaut template ✔️
- Client (after hydration)
   - component A : renders an error message ✔️
   - components B & C : render their defaut template ✔️
[Screencast from 29-07-2024 17:37:41.webm](https://github.com/user-attachments/assets/24777265-feed-4929-a6e2-818906963ce5)

`/works` page
You will see that, on SSR, component A has rendered its error message and components B+C render their default template ☑️
But, **after hydration**, components B+C render an error message even though only A has failed ❎
[Screencast from 29-07-2024 17:37:17.webm](https://github.com/user-attachments/assets/b5f4192c-0597-4176-b3d3-17c923803ba3)
