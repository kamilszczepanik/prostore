# Notes from Course

## Useful Libraries
- Shadcn UI(install components one by one, not whole library at once - smaller size)
- lucide-react - icons library, out of the box


## Tips
When some libraries are not updated to new versions of other installed library:

```bash
npm install --legacy-peer-deps
```

safer than installing with force flag


## Next.js

### Not found and loading pages
Create not-found.tsx file in app and export NotFoundPage where you will have your component. The same with the loading page.