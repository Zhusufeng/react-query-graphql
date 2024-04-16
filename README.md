# React Query GraphQL

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app) that has examples of how to use React Query with a REST API and a GraphQL API (frontend-only).

## Prerequisites

- Node.js 18+

## Tech Stack

- Vercel's [Next](https://nextjs.org/) 14
- [GraphQL](https://graphql.org/) 16
- [React](https://react.dev/) 18
- [Tanstack's React Query](https://tanstack.com/query/latest/docs/framework/react/overview)
- Prisma's [graphql-request](https://www.npmjs.com/package/graphql-request)
- The Guild's [GraphQL Codegen](https://the-guild.dev/graphql/codegen)

## NPM Scripts

- `npm run dev` - Runs the development server
- `npm run build` - Builds the code
- `npm start` - Runs the built code
- `npm lint` - Lints
- `npm run codegen` - Using the link to the GraphQL schema in codegen.ts, it will generate code for TypeScript typing.

## Getting Started

```bash
git clone <repo>

cd react-query-graphql

npm i
```

Run the development server:

```bash
npm run dev
```

## Development Notes

If your GraphQL schema changes, you will need to have setup your codegen.ts.

You can do so by doing the following:

```bash
npx graphql-code-generator init
```

It will ask you questions and create a codegen.ts at the root.

To use the Star Wars GraphQL API, you would use the following:

```bash
? What type of application are you building?
  Application built with React
? Where is your schema?: (path or url)
  https://swapi-graphql.netlify.app
? Where are your operations and fragments?:
  src/**/*.tsx
? Where to write the output:
  src/gql/
? Do you want to generate an introspection file?
  No
? How to name the config file?
  codegen.ts
? What script in package.json should run the codegen?
  codegen
```

It also adds the npm script `"codegen": "graphql-codegen --config codegen.ts"`.

You can run `npm run codegen` to create the src/gql file. You can use the generated code to have full-typed GraphQL operations.

## Example REST API call with React Query

- Code: [/src/pages/index.tsx](./src/pages/index.tsx)
- View it at http://localhost:3000

## Example GraphQL API call with React Query

- Code: [/src/pages/graphql.tsx](./src/pages/graphql.tsx)
- View it at http://localhost:3000/graphql

## API Routes

There are none.

<!-- [API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.ts`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages. -->

## References

- [TanStack React GraphQL](https://tanstack.com/query/latest/docs/framework/react/graphql#type-safety-and-code-generation)
- [GraphQL-Codegen: Quick Start](https://the-guild.dev/graphql/codegen/docs/getting-started/installation)
- [GraphQL-Codegen: Guide: React and Vue](https://the-guild.dev/graphql/codegen/docs/guides/react-vue)
