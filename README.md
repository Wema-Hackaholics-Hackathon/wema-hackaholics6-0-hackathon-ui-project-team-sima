# [Project Title]

## Team Members
- Olaniran Pamilerin Simon
- Oluremi Alao
- Victor Akinmoladun
- Ayooluwa Paul
- Kolawole Jegede

---

## 🚀 Live Demo

*   **Live Application:** https://wematrust.vercel.app/
*   **Backend API:** [Link to your live backend API endpoint URL, if separate]
*   **Recorded Demo:** [Link to your recorded demo explaining how your solution works using Loom].


---

## 🎯 The Problem

**Challenge Track:** E-Channels & Transaction Reliability  
**Challenge Question:**  
> How might we shield customers from internal system complexities and make every digital transaction feel instant and completely reliable, even when failures occur behind the scenes?

## ✨ Our Solution

Our project, **Instant-Feel Transactions**, is a prototype system designed to make transfers feel as seamless as fintechs like OPay and Moniepoint — even when issues occur behind the scenes.  

We combined **proactive communication**, **smart crediting**, and **fintech-inspired liquidity pools** to solve both the *trust gap* and the *instant transfer problem* in commercial banks.  

### Core Features
1. **Instant Crediting (Ledger First):**  
   - For Wema-to-Wema transfers, recipients are credited instantly and funds are usable, even if reconciliation is pending in the backend.  
   - Internal ledger ensures consistency and automatic reconciliation without customer friction.  

2. **Pre-Funded Pool Accounts:**  
   - Wema holds funded accounts in major partner banks (e.g., GTB, Access).  
   - Outbound transfers are instantly credited from these pools while final settlement with NIBSS happens later.  
   - This mirrors how OPay and Moniepoint achieve speed.  

3. **Tiered Risk Controls:**  
   - **Low-value transfers (< ₦50k):** Auto-credit with minimal checks.  
   - **High-value transfers (> ₦500k):** Stricter checks and may require additional validation.  

4. **Proactive Communication:**  
   - Real-time push + SMS notifications at each stage.  
   - Transparency: customer is told if the receiving bank is experiencing issues, instead of being left in the dark.  

5. **Monitoring & Admin Dashboard:**  
   - Shows transactions under reconciliation, liquidity pool usage, and partner bank status.  
   - Helps bank staff resolve issues quickly while customers continue experiencing instant credit.  

6. **Fallback Mode (If NIBSS Down):**  
   - Switches automatically to pre-funded pool accounts to continue instant payouts.  
   - Reconciles once NIBSS is restored.  

---

## 🛠️ Tech Stack

### 🏗️ Frontend
**Core Framework**
- Next.js 15.3.3 — React framework with App Router  
- React 18 — UI library with hooks and modern patterns  
- TypeScript — Type-safe JavaScript  

**Styling & UI**
- Tailwind CSS — Utility-first CSS framework  
- shadcn/ui — Pre-built accessible UI components  
- Lucide React — Icon library  
- CSS Modules — Component-scoped styling  

**State Management**
- React Hooks — `useState`, `useEffect`, `useCallback`, `useRef`  
- Server Actions — Next.js server-side form handling  
- Local Storage — Browser-side data persistence  

---

### 🚀 Backend
**API Layer**
- Next.js API Routes — Serverless API endpoints  
- RESTful APIs — Standard HTTP methods (GET, POST)  
- Server-Sent Events (SSE) — Real-time updates  

**Data Persistence**
- File-based Storage — JSON files for persistence  
- In-memory Database — Map-based structures  
- localStorage — Browser-side caching  

**Data Validation**
- Zod — Schema validation library  
- TypeScript Interfaces — Type definitions  

---

### 🔧 Development Tools
**Build & Development**
- Turbopack — Fast bundler (Next.js default)  
- Node.js — JavaScript runtime  
- npm — Package manager  

**Code Quality**
- ESLint — Code linting  
- TypeScript Compiler — Type checking  
- Prettier — Code formatting  

---

## ⚙️ Local Setup & Installation

### Prerequisites

Before you begin, ensure you have the following installed:
- **Node.js** (v18 or higher) - [Download here](https://nodejs.org/)
- **npm** (comes with Node.js)
- **Git** - [Download here](https://git-scm.com/)

### Step 1: Clone the Repository
```bash
git clone https://github.com/Wema-Hackaholics-Hackathon/wema-hackaholics6-0-hackathon-ui-project-team-sima
cd wematrust
```
### Step 2: Install Dependencies

```bash
npm install
```

This will install all required dependencies including:
- Next.js and React
- Tailwind CSS and UI components
- TypeScript and type definitions
- Zod for validation
- Lucide React for icons

### Step 3: Environment Setup

Create a `.env.local` file in the root directory (optional for local development):

```bash
# Optional: Set custom port (default is 9002)
NEXT_PUBLIC_BASE_URL=http://localhost:9002
```

### Step 4: Start the Development Server

```bash
npm run dev
```

The application will start on `http://localhost:9002`

### Step 5: Access the Application

1. **Open your browser** and navigate to `http://localhost:9002`
2. **Login Page** - Select a demo user:
   - **Admin** - Access admin dashboard and system monitoring
   - **Demo User 1** - Account: 0123456789 (Balance: ₦100,000)
   - **Demo User 2** - Account: 9876543210 (Balance: ₦50,000)

---

## 🔧 Available Scripts

```bash
# Start development server
npm run dev

# Build for production
npm run build

# Start production server
npm start

# Run linting
npm run lint

# Type checking
npm run typecheck
```

---

## 📁 Project Structure

```
wematrust/
├── src/
│   ├── app/                 # Next.js App Router
│   │   ├── api/            # API routes
│   │   ├── admin/          # Admin dashboard
│   │   ├── login/          # Login page
│   │   └── page.tsx        # Main dashboard
│   ├── components/         # React components
│   │   ├── ui/             # shadcn/ui components
│   │   ├── dashboard-layout.tsx
│   │   ├── transfer-form.tsx
│   │   └── admin-logs-dashboard.tsx
│   └── lib/                # Utilities and types
│       ├── database.ts     # Data access layer
│       ├── types.ts        # TypeScript definitions
│       └── utils.ts        # Helper functions
├── public/                 # Static assets
│   └── wemaba-logo.png     # Wema Bank logo
├── data/                   # Data persistence
│   └── wematrust_db.json   # Database file
└── package.json
```

---

## 🚀 Key Features Demonstrated

### 1. Instant Credit System
- Recipients are credited immediately upon transfer
- Backend settlement happens asynchronously
- Transfer logs track both instant and backend status

### 2. Prefunded Accounts
- Liquidity pools in partner banks
- Real-time balance monitoring
- Automatic status updates (ACTIVE/LOW/DEPLETED)

### 3. Admin Dashboard
- Real-time transfer monitoring
- System health indicators
- Comprehensive audit trails

### 4. Real-time Updates
- Server-Sent Events for live updates
- Instant UI refresh after transfers
- Real-time balance and transaction updates

---

## 🐛 Troubleshooting

### Common Issues:

1. **Port Already in Use**
   ```bash
   # Kill existing processes
   taskkill /F /IM node.exe  # Windows
   killall node              # macOS/Linux
   ```

2. **Database Reset**
   ```bash
   # Delete database file to reset
   rm data/wematrust_db.json
   ```

3. **Dependencies Issues**
   ```bash
   # Clear cache and reinstall
   rm -rf node_modules package-lock.json
   npm install
   ```

4. **TypeScript Errors**
   ```bash
   # Run type checking
   npm run typecheck
   ```

---

## 📖 API Endpoints

- `GET /api/accounts?userId={id}` - Get user account
- `GET /api/transactions?userId={id}` - Get user transactions
- `POST /api/transfer` - Process transfer
- `GET /api/admin/logs` - Admin dashboard data
- `GET /api/events` - Server-Sent Events stream
- `POST /api/ussd` - USSD simulation

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request 

## 🎮 How to Use the Application

### For Regular Users:

1. **Login** - Select "Demo User 1" or "Demo User 2"
2. **Dashboard** - View your account balance and recent transactions
3. **Make Transfer** - Send money to another account:
   - Enter amount (e.g., ₦5,000)
   - Enter destination account number
   - Select destination bank
   - Add optional note
   - Click "Send Money"
4. **Real-time Updates** - Watch your balance and transaction history update instantly

### For Admin Users:

1. **Login** - Select "Admin"
2. **Admin Dashboard** - Access at `http://localhost:9002/admin`
3. **Monitor System** - View:
   - Total transfers and success rates
   - Prefunded account status
   - Recent transfer logs
   - System health metrics
4. **Network Simulation** - Change partner bank statuses to test resilience

### Testing the Instant Transfer System:

1. **Make a Transfer** - Send money from User 1 to User 2
2. **Observe Instant Credit** - Recipient is credited immediately
3. **Check Admin Logs** - See the transfer in the admin dashboard
4. **Watch Backend Settlement** - Backend settles in ~3 seconds
5. **Verify Data Persistence** - Refresh the page to see persisted data

---

## 📖 Documentation

- **Ledger-first crediting:** Receivers see funds instantly, with reconciliation handled in the backend.  
- **Pre-funded pool architecture:** Inspired by fintechs, allows instant cross-bank transfers even during NIBSS downtime.  
- **Tiered transfer rules:** Low vs. high-value transaction flow.  
- **Notifications:** All state changes generate push + SMS.  
- **Monitoring Panel:** Simulates outages by toggling partner bank status.  

---

## ✅ Why This Matters

This solution allows Wema to:  
- Compete with fintechs like OPay/Moniepoint on speed.  
- Preserve **trust** with instant user feedback and communication.  
- Stay **compliant** with CBN/NIBSS while introducing modern reliability mechanisms.  