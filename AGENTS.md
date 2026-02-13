# prediction-market — Agent Rules

> Cursor reads this file automatically. Type "go" or "start" to begin building.

## What to do

Read `docs/TASKS.md`. Find the first unchecked task. For EACH task:

1. Read the task's **Scope** and **Acceptance Criteria**.
2. Implement the minimum changes to satisfy the AC.
3. Run the task's **Verify** commands in the terminal.
4. If verify fails, fix the code and re-run until green.
5. Mark the task `[x]` in `docs/TASKS.md` and add a 1-2 line completion note.
6. **Move to the next unchecked task and repeat.**

Continue until all tasks are checked off or you hit a BLOCKED task.

## Rules

1. **One task at a time, then continue.** Do not work on multiple tasks at once. Do not stop between tasks unless blocked.
2. **Run verify commands.** Every task has a `Verify` section. Run those exact commands after implementing.
3. **Fix until green.** If verify commands fail, fix the code and re-run. Do not move on until they pass.
4. **No refactors unless the task says so.** Do not reorganize, rename, or "improve" code outside the task scope.
5. **Minimum changes only.** Implement the smallest diff that satisfies the acceptance criteria. No gold-plating.
6. **Check off completed tasks.** After verify passes, mark the task `[x]` and add a 1-2 line completion note. A task is only done when verify passes AND `docs/TASKS.md` is checked off.
7. **Read before writing.** Before editing any file, read it first. Do not guess at existing code structure.
8. **Follow the runbook.** All dev commands are in `docs/RUNBOOK.md`. Do not invent commands.
9. **Never commit secrets.** Use `.env` for keys/credentials. Reference `.env.example` for required vars. Never hardcode API keys, DB URLs, or tokens.
10. **Use recommended packages.** If `docs/DECISIONS.md` lists an OSS package for a feature, use it. Do not build custom.

## Stack decisions

See `docs/DECISIONS.md` for locked technology choices. Do not deviate.

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

## OSS-first policy

`docs/DECISIONS.md` includes an **OSS Accelerators** table listing packages the council selected. When a task involves a feature covered by a listed package, **use that package**. Do not build a custom implementation. Install it, configure it, integrate it — that's the task. Only write custom code for product-unique logic not covered by any recommended package.

## Project structure

(will be created by task T1)

## When stuck

1. Re-read the task's acceptance criteria — the answer is usually there.
2. Check `docs/DECISIONS.md` for stack-specific guidance.
3. Check `docs/RUNBOOK.md` for the right command.
4. If truly blocked, add a `BLOCKED: <reason>` note to the task and move to the next one.
