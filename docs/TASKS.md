# prediction-market — Task Queue

> Each task is a unit of work for one Cursor agent session.
> Work top-to-bottom. Do not skip. Do not reorder.
> Mark `[x]` when verify passes. Add a completion note.
>
> **Done definition:** A task is only complete when its Verify commands pass AND this file is updated with `[x]` and a 1-2 line note. No exceptions.

## - [ ] T1 Project Init

**Scope:** Create a new repository using the Blitz.js starter template. Install necessary dependencies including Prisma, Socket.io, and Auth.js. Set up the initial folder structure aligning with the product's backend architecture.

**AC:**
- Repository initialized with Blitz.js template.
- Dependencies installed: Prisma, Socket.io, Auth.js.
- Folder structure created to support backend and frontend separation.

**Verify:**
```bash
npx blitz new prediction-market
cd prediction-market
npm install @prisma/client socket.io auth.js
npm run build
```

---

## - [ ] T2 Configure Database

**Scope:** Set up PostgreSQL database using Supabase. Configure Prisma schema with the provided data model and generate the Prisma client.

**AC:**
- PostgreSQL database set up on Supabase.
- Prisma schema matches the provided data model.
- Prisma client generated successfully.

**Verify:**
```bash
npx prisma migrate dev --name init
npx prisma generate
```

---

## - [ ] T3 Blockchain Integration

**Scope:** Integrate Base blockchain using ethers.js. Set up basic smart contract interaction for event creation and bet placement.

**AC:**
- Base blockchain integrated using ethers.js.
- Basic smart contract interaction for event creation and bet placement implemented.

**Verify:**
```bash
node scripts/testBlockchainIntegration.js
```

---

## - [ ] T4 User Authentication

**Scope:** Implement authentication using Auth.js. Configure wallet-based authentication flow with MetaMask and Coinbase Wallet support.

**AC:**
- Auth.js configured for wallet-based authentication.
- MetaMask and Coinbase Wallet integration tested.

**Verify:**
```bash
npm run test:auth
```

---

## - [ ] T5 Real-Time Updates

**Scope:** Set up real-time updates using Socket.io for event outcomes and market changes. Ensure latency is under 2 seconds.

**AC:**
- Socket.io configured for real-time updates.
- Latency for updates verified to be under 2 seconds.

**Verify:**
```bash
npm run test:realtime
```

---

## - [ ] T6 Event Management API

**Scope:** Implement API endpoints for creating events, placing bets, and resolving events. Ensure endpoints align with the provided API design.

**AC:**
- API endpoints for event creation, bet placement, and event resolution implemented.
- Endpoints tested and verified against the API design.

**Verify:**
```bash
npm run test:api
```

---

## - [ ] T7 Frontend Setup

**Scope:** Set up the frontend using Next.js with Tailwind CSS and shadcn/ui for styling. Implement basic navigation and layout components.

**AC:**
- Next.js frontend set up with Tailwind CSS and shadcn/ui.
- Basic navigation and layout components implemented.

**Verify:**
```bash
npm run dev
```

---

## - [ ] T8 Event List & Details UI

**Scope:** Implement UI for listing events and displaying event details. Ensure responsiveness and accessibility.

**AC:**
- Event list and details UI implemented.
- UI tested for responsiveness and accessibility.

**Verify:**
```bash
npm run test:ui
```

---

## - [ ] T9 Bet Placement UI

**Scope:** Implement UI for placing bets on events. Ensure integration with wallet authentication and real-time updates.

**AC:**
- Bet placement UI implemented.
- Integration with wallet authentication and real-time updates verified.

**Verify:**
```bash
npm run test:betUI
```

---

## - [ ] T10 Payout Logic & Testing

**Scope:** Implement payout logic for resolving events and distributing winnings. Test logic with various scenarios.

**AC:**
- Payout logic implemented and tested.
- Various scenarios (e.g., no bets, all bets wrong) tested.

**Verify:**
```bash
npm run test:payout
```

---

## - [ ] T11 Social Sharing Features

**Scope:** Implement social sharing features allowing users to share bets and outcomes on social media.

**AC:**
- Social sharing features implemented.
- Sharing functionality tested on major social platforms.

**Verify:**
```bash
npm run test:social
```

---

## - [ ] T12 Security & Audit

**Scope:** Conduct a security review and audit of the smart contracts and authentication flows. Implement necessary security measures.

**AC:**
- Security review and audit conducted.
- Identified vulnerabilities addressed.

**Verify:**
```bash
npm run test:security
```

---

## - [ ] T13 Deployment Setup

**Scope:** Set up deployment pipeline using Vercel and Supabase. Configure environment variables and CI/CD pipeline.

**AC:**
- Deployment pipeline set up with Vercel and Supabase.
- CI/CD pipeline configured and tested.

**Verify:**
```bash
npm run deploy
```

---

## - [ ] T14 Smoke Test Full App

**Scope:** Conduct a smoke test of the full application, verifying end-to-end functionality from event creation to payout.

**AC:**
- Full application tested end-to-end.
- All core features verified to work as expected.

**Verify:**
```bash
npm run test:smoke
```
