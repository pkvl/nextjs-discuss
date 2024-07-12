This is a simple discuss-style application built to familiarize myself with [Next.js](https://nextjs.org/).

## Technologies used
- [Next.js](https://nextjs.org/) - app
- [NextAuth.js](https://next-auth.js.org/) - for auth purposes
- [Prisma](https://www.prisma.io/) - ORM
- [SQLite](https://www.sqlite.org/) - SQL file-based Database
- [Tailwind](https://tailwindcss.com/) - for styling
- [Zod](https://zod.dev/) - for input validation

## Getting Started

To complete the setup you need to create a [GitHub OAuth application](https://github.com/settings/applications/new). Copy `.env` file and rename the copy to the `.env.local`. Set up the application variables:
  - `DATABASE_URL="file:./dev.db"` - path to your SQLite db file.
  - `AUTH_SECRET` - should be your secret wording (for the client)
  - `GITHUB_CLIENT_ID` and `GITHUB_CLIENT_SECRET` should be copied from your freshly-created GitHub OAuth application.

Generate database via Prisma (if you want to have a database in the repository: delete `prisma/dev.db` from `.gitignore`):
```bash
npx prisma init --datasource-provider sqlite && npx prisma generate
```

Run the development server:

```bash
npm run dev
```

Or start the production-ready application:
```bash
npm run start
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Features
- Sign In/Sign Up process via GitHub account
- Create Topics
- Create Posts in Topics
- Leave comments in Posts 
- Search Posts

![Demo image]((https://github.com/pkvl/nextjs-discuss/blob/main/assets/demo.png?raw=true)