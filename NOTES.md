# Notes from [Next.js Course](https://www.udemy.com/course/nextjs-ecommerce-course/).

[Forked Code](https://github.com/kamilszczepanik/prostore/tree/main)
[Readme of the project](README.md)


## Useful Libraries
- Shadcn UI(install components one by one, not whole library at once - smaller size)
- lucide-react - icons library, out of the box
- neon - database in cloud. As a time of learning, it is mandatory to install @neondatabase/serverless, @prisma/adapter-nean, ws to make neon work properly


## Tips
1. When some libraries are not updated to new versions of other installed library:

```bash
npm install --legacy-peer-deps
```

> safer than installing with force flag

2. Try to use form filler(Fake Filler Chrome Extension)


## Typescript
*Use zod to create a validator that will be used not only in form, but also imported to the actual type used across the app. This is crucial practice to not repeat code and have robust app.*

## Next.js

### Structure
(auth) - just a folder to organize paths

### Not found and loading pages
*Create not-found.tsx file in app and export NotFoundPage where you will have your component. The same with the loading page.*

To send user to notFound page:
```
import { notFound } from 'next/navigation'
if (!product) notFound();
```

## Authentication
*We are using auth.js(next auth) - it was originally created for the next.js, later it was broadened to other frameworks*
It is very opinionated and high-level, I set config and it works.
[current auth options](auth.ts)
/auth - everything on that rout next auth is taking care of that

> - [auth.js getting started](https://authjs.dev/getting-started)
> - [auth.js with prisma](https://authjs.dev/getting-started/adapters/prisma)

In next.js 15 to get searchParams or params you have to define them in the props - in "server" components and useSearchParams hook in "client" components.

## Deployment 
> **_IMPORTANT:_** It is a good idea to go through all the versions and update them before deployment and development of the target application.

- to add another language use [next itl](https://next-intl.dev/)

## Database
Commands to run every time after updating schema.prisma
```
npx prisma generate
npx prisma migrate dev --name add_user_based_tables
```