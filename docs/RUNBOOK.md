# prediction-market — Runbook

> Every command you need to develop, test, and deploy this app.
> If a command isn't here, don't guess — add it.

## Install
```bash
npm install
```

## Dev
```bash
npm run dev
```

## Lint
```bash
npm run lint
```

## Typecheck
```bash
npm run typecheck
```

## Test
```bash
npm test
```

## Database
```bash
npx prisma migrate dev --name init
npx prisma db seed
npx prisma studio
```

## Environment
```bash
cp .env.example .env.local
# Required vars (extract from spec):
# DATABASE_URL=
# NEXT_PUBLIC_API_URL=
# REDIS_URL=
# WEB3_INFURA_PROJECT_ID=
# JWT_SECRET=
```

## Build
```bash
npm run build
```

## Deploy
```bash
# Deployment commands using GitHub Actions and Vercel
# Ensure secrets like VERCEL_TOKEN are set in GitHub Secrets
```
