# Notes from Course

## Useful Libraries
- Shadcn UI(install components one by one, not whole library at once - smaller size)
- lucide-react - icons library, out of the box
- neon - database in cloud. As a time of learning, it is mandatory to install @neondatabase/serverless, @prisma/adapter-nean, ws to make neon work properly


## Tips
When some libraries are not updated to new versions of other installed library:

```bash
npm install --legacy-peer-deps
```

safer than installing with force flag

## Typescript
Use zod to create a validator that will be used not only in form, but also imported to the actual type used across the app. This is crucial practice to not repeat code and have robust app.

## Next.js

### Not found and loading pages
Create not-found.tsx file in app and export NotFoundPage where you will have your component. The same with the loading page.

