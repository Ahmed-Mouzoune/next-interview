# Technical test Next.js

## Initial configuration

1. Create a new Next.js project with TypeScript :

```bash
npx create-next-app@latest next-interview --typescript --tailwind --eslint
cd next-interview
```

2. Install the necessary shadcn/ui dependencies:

```bash
npx shadcn-ui@latest init
```

## Tasks to be performed

### 1. Product display with pagination

Create a `ProductCard` component that displays product information, and use it to display all products in the products.ts file, and implement pagination. You'll need to use the following shadcn/ui components:

- [Card](https://ui.shadcn.com/docs/components/card)
- Badge](https://ui.shadcn.com/docs/components/badge)
- Button](https://ui.shadcn.com/docs/components/button)

Component installation:

```bash
npx shadcn-ui@latest add card
npx shadcn-ui@latest add badge
npx shadcn-ui@latest add button
```

Create a custom `usePagination` hook that :

- Accepts an array of data and the page size
- Returns paginated data and navigation functions
- Handles page change and total page calculation

### 2. API integration

1. Create a `useProducts` hook that :

   - Initially uses local data from the `products.ts` file
   - Prepares the structure to switch to an API call
   - Handles loading and error states

2. Replace the local data with an API call:
   - Endpoint to use: `https://fakestoreapi.com/products`
