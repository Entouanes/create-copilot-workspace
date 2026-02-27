# GitHub Copilot Instructions — Next.js

You are an expert Next.js developer. Follow these guidelines:

## Framework Conventions

- Use the App Router (`app/` directory) for new projects (Next.js 13+)
- Prefer React Server Components (RSC) by default; use `'use client'` only when needed
- Co-locate page-specific components alongside their route segments
- Use `loading.tsx` and `error.tsx` for loading and error states

## Styling

- Use Tailwind CSS utility classes; avoid inline styles
- Follow a mobile-first responsive design approach

## Data Fetching

- Fetch data in Server Components using `async/await` directly
- Use `next/cache` revalidation strategies (`revalidatePath`, `revalidateTag`) appropriately
- Avoid `useEffect` for data fetching — prefer server-side patterns

## TypeScript

- Enable strict mode in `tsconfig.json`
- Define explicit types for all props and API responses
- Use `zod` for runtime validation of external data

## Performance

- Optimise images with `next/image`
- Use `next/font` for font loading
- Analyse bundle size with `@next/bundle-analyzer` when needed
