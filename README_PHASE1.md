# AeroVista Phase 1 — Live Backend Demo

The existing v2.3 AeroVista UI is connected to a real Phase-1 backend path:
React → FastAPI → PostgreSQL + Redis → Python observation simulator.

## Run on Windows / Docker Desktop
1. Start Docker Desktop.
2. In this folder run `docker compose up --build`.
3. In a second terminal run `npm install` then `npm run dev`.
4. Open the Vite URL, normally `http://localhost:5173`.

The Command Centre polls FastAPI every 3 seconds. A new observation is persisted every 5 seconds. The UI shows LIVE BACKEND and the exact last-update time in IST. Stop the containers with `docker compose down`.

## Verify
- Backend health: http://localhost:8000/health
- Current summary: http://localhost:8000/api/v1/dashboard/summary
- Interactive docs: http://localhost:8000/docs

The Phase-1 collector is intentionally a Python simulation of incoming fare observations. It is not live airline/OTA scraping yet. The database/API/cache pipeline is designed so a compliant collector can replace the simulator later without changing the dashboard contract.

## Fare Time Machine
A new **Fare Time Machine** navigation tab is included. It calls `GET /api/v1/routes/price-history` and displays a selected route's T+1/T+7/T+15/T+30/T+45 fares at 30-day, 15-day, 7-day and current checkpoints. The history is retained in PostgreSQL and current observations update today's checkpoint through the Phase 1 simulator.
