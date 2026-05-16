# Crypto Tax Tracker Backend

Initial backend setup for crypto tax tracking using Node.js, TypeScript, Express, Prisma, and PostgreSQL.

## Podman / Docker Setup

1. Copy `.env.example` to `.env` and configure variables (especially DATABASE_URL pointing to the `db` service, e.g. `postgresql://user:pass@db:5432/crypto_tax?schema=public`).
2. Build and run:
   ```bash
   podman compose up --build -d
   ```

## Local Development (without container)

1. `npm install`
2. `npx prisma generate`
3. `npx prisma migrate dev`
4. `npm run dev`

## Scripts
- `npm run dev`: Development server with ts-node
- `npm start`: Production
- `npx prisma studio`: Open DB GUI