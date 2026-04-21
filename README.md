# DevFlow — Backend API

Node.js/Express backend for DevFlow, an AI-powered project management SaaS.

## 🔗 Links
- **Frontend:** https://github.com/zaki9254/devflow-frontend
- **Live App:** https://devflow-frontend-five.vercel.app

## ⚙️ Tech Stack
- **Runtime:** Node.js + Express.js
- **Database:** MongoDB Atlas + Mongoose
- **Cache:** Redis (ioredis) — session caching + rate limiting
- **Real-time:** Socket.io — live board updates
- **Auth:** JWT (jsonwebtoken) + bcryptjs
- **Payments:** Stripe — subscription billing + webhooks
- **AI:** OpenAI API — AI task suggestions
- **Email:** Nodemailer
- **Other:** Passport.js (Google OAuth), Cloudinary, express-rate-limit

## 📁 Project Structure
src/
config/      → MongoDB, Redis connections
controllers/ → Request handlers (auth, workspace, project, board, task, ai, billing)
middleware/  → JWT auth, rate limiting, role-based access
models/      → Mongoose schemas (User, Workspace, Project, Board, Task)
routes/      → Express route definitions
services/    → AI, email, Stripe, Socket.io services
utils/       → Token generation, slug generation, API response helpers

## 🏗️ Key Features
- JWT authentication with 7-day token expiry
- bcrypt password hashing with pre-save hook
- Role-based access control (owner / admin / member)
- Real-time task updates via Socket.io rooms
- Redis session caching with graceful degradation
- Rate limiting on auth routes (10 req / 15 min)
- Stripe subscription billing with webhook verification
- AI task suggestion (OpenAI integration)

## 🚀 Run Locally
```bash
git clone https://github.com/zaki9254/devflow-backend
cd devflow-backend
npm install
# create .env with MONGO_URI, REDIS_URL, JWT_SECRET, STRIPE_KEY, OPENAI_KEY
npm run dev
```
