# PHANTOM X ESPORTS — Full-stack foundation

This package turns the V17 frontend into a deployable Node.js + PostgreSQL web app foundation.

## Includes
- PHANTOM X ESPORTS landing page: Register / Enter first
- Tournament, Guild, Giveaway, Registration, Matches, Profile, Leaderboard, Wallet, Live and Admin UI
- Real email/password authentication with bcrypt + JWT
- PostgreSQL schema for users, tournaments, registrations, results and notifications
- Admin-only tournament creation, registration approval and result publishing APIs
- Room ID/password generated only by the admin approval API
- Health endpoint and deployment-ready environment variables

## Run locally
1. Install Node.js 20+ and PostgreSQL.
2. Create a PostgreSQL database named `phantom_x_esports`.
3. Copy `.env.example` to `.env` and fill `DATABASE_URL` and a strong `JWT_SECRET`.
4. Set `ADMIN_EMAIL` and `ADMIN_PASSWORD` before starting.
5. Run `npm install`.
6. Run `npm start`.
7. Open `http://localhost:3000`.

## Production
Use a managed PostgreSQL provider and a Node-compatible host. Set all environment variables in the host dashboard; never commit `.env` or secrets.

## Payments
No real-money payment gateway is enabled in this package. Add a compliant payment provider only after confirming applicable law, age/eligibility rules, game/platform rules and the provider's merchant requirements. Never trust a client-side payment-success flag; verify payments server-side through signed webhooks.
