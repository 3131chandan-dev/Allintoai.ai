# ALLXAI — allintoai.ai

This package contains a ready-to-customize frontend (Vite + React) and backend (Node/Express) for ALLXAI.

## What is included
- `frontend/` — React app (vite) ready to deploy to Vercel
- `backend/` — Express API ready to deploy to Render (or Docker)
- `assets/` — logo.svg and favicon placeholder
- `vercel.json`, `infra/render.yaml`, `.env.example`

## Quick deploy (recommended)
1. Create two GitHub repos: one for `frontend` and one for `backend`.
2. Deploy `frontend` to Vercel (connect GitHub). Set `VITE_API_URL` to `https://api.allintoai.ai`.
3. Deploy `backend` to Render (or use Vercel serverless). Add `DATABASE_URL` and `EMAIL_FROM` in service env.
4. Namecheap DNS (Domain List → Manage → Advanced DNS):
   - A  @    76.76.21.21
   - CNAME  www  cname.vercel-dns.com.
   - CNAME  api  <render-service-hostname>

## Local run
- Frontend:
  cd frontend
  npm install
  npm run dev
- Backend:
  cd backend
  npm install
  npm start

## Notes
- Replace placeholder logo/favicon with final assets in `assets/`.
- Configure SendGrid or SMTP for outbound email; update backend to use Nodemailer transport.
