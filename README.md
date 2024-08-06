This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

## PASSO A PASSO

1. npx create-next-app@latest fsw-barber
2. npm install prisma --save-dev
3. npx prisma init --datasource-provider postgresql
   - Define o postgresql como bd para o prisma e cria a pasta "prisma"
4. Criar as tabelas no "schema.prisma"
5. npx prisma migrate dev --name init_db
   - Cria a migration
6. Criou o arquivo "/prisma/seed.ts", para inicializar alguns dados no BD
7. Adicionou comando no "package.json" para rodar o seed
   "prisma": {
   "seed": "ts-node prisma/seed.ts"
   }
8. npm i -D ts-node (rodar o comando que inicializa o seed no BD)
9. npx prisma db seed

Obs: usar "npx prisma format" para identar arquivo ".prisma"

## CONFIG

- node: 20.16.0
- npm: 10.8.1
