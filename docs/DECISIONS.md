# prediction-market — Technology Decisions

> Locked choices from the council. Do not change without running `council refine`.
> **OSS-first policy:** If a package is listed in "OSS Accelerators" below, use it. Do not build a custom version.

## Section 1: Technology Stack

| Decision          | Choice            | Why                                                                 |
|-------------------|-------------------|---------------------------------------------------------------------|
| Blockchain        | Base blockchain   | Offers high transaction speeds and low costs, crucial for short-duration events. |
| Smart Contracts   | Solidity          | Primary language for Ethereum-compatible chains like Base, ensuring reliability. |
| Backend           | Node.js with Express | Excellent for handling asynchronous operations, fitting the MVP needs. |
| Database          | PostgreSQL        | Handles off-chain data such as user profiles and event metadata efficiently. |
| ORM               | Prisma            | Provides type-safe database access and easy integration with Node.js. |
| Real-time Updates | WebSockets        | Essential for pushing real-time updates to users about market status and outcomes. |
| Frontend Framework| Next.js           | Provides server-side rendering and static site generation, ideal for responsive web apps. |
| CSS               | Tailwind CSS      | Allows rapid UI development with utility-first classes. |
| State Management  | Zustand           | Lightweight and provides a simple API for managing client-side state. |
| Auth              | Auth.js (formerly NextAuth.js) | Simplifies authentication logic integration. |
| Testing           | Playwright        | Enables end-to-end testing with a focus on modern web apps. |
| CI/CD             | GitHub Actions    | Automates deployment and testing processes. |
| Monitoring        | Sentry            | Tracks errors and performance issues. |

## Section 2: OSS Accelerators (Don't Build What Exists)

| Category              | Package                   | What It Gives Us                                         | Install Command                   |
|-----------------------|---------------------------|----------------------------------------------------------|-----------------------------------|
| Backend Framework     | Blitz.js                  | Replaces custom boilerplate for authentication and API structure. | `npm install blitz`               |
| Database Tooling      | Prisma                    | Replaces raw SQL queries and complex database migrations. | `npm install @prisma/client`      |
| Auth Solution         | Auth.js                   | Replaces custom authentication logic.                    | `npm install auth.js`             |
| Real-time Library     | Socket.io                 | Replaces custom WebSocket implementation.                | `npm install socket.io`           |
| UI Component Libraries| shadcn/ui                 | Provides modern, accessible components with Tailwind CSS. | `npm install @shadcn/ui`          |
| Web3 Integration      | @web3-react/core          | Wallet connection and management for blockchain interactions. | `npm install @web3-react/core`    |
| Chart Libraries       | Recharts                  | Easy-to-use charting library for displaying market trends. | `npm install recharts`            |
| Design Systems        | Radix UI                  | Primitives for building accessible, high-quality UI components. | `npm install @radix-ui/react`     |
| Deployment Templates  | Vercel's Next.js Template | Provides a starter for deploying Next.js apps on Vercel. | Not applicable (Vercel template)  |
| Monitoring/Observability | Sentry                | Free tier for error tracking, widely used and trusted.   | Not applicable (SaaS)             |
| Infrastructure-as-code| Pulumi                    | Manages cloud resources with code, supports multiple providers. | Not applicable (SaaS)             |
| Developer Tooling     | Husky                     | Manages Git hooks, ensuring code quality before commits. | `npm install husky`               |
| Developer Tooling     | Changesets                | Manages versioning and changelogs in a monorepo setup.   | `npm install changesets`          |
