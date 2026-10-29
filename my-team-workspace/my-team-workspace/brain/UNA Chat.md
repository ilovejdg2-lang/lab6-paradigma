# UNA Chat

Purpose and verified stack for the Laboratorio 5 → 8 product.

## Purpose (confirmed)

Chat en tiempo real académico (UNA) con mensajes de texto, detección de imágenes/URLs de video y validación anti-inyección en `libs/unalib.js`.

## Architecture (verified in repo)

- **Not React.** Frontend: `index.html` + jQuery + Socket.IO client CDN.
- Backend: Node.js, Express, Socket.IO (`server.js`).
- Validation: `libs/unalib.js` → `validateMessage`.
- Event: `Evento-Mensaje-Server` with `{ nombre, mensaje, color }`.
- Tests: Mocha unit, Jest integration, Playwright e2e.
- OpenSpec present under `openspec/`.

## Location

`Repos/lab5-paradigmas/` (independent Git). Remote: `ilovejdg2-lang/lab5-paradigmas`.

## Commands

- `npm start` — server on `PORT` or 3000
- `npm test` — Mocha
- `npm run test:integration` — Jest
- `npm run test:e2e` — Playwright

## Lab 5 features to preserve

Mensajes entre usuarios, color, imágenes, videos/enlaces admitidos, validaciones y pruebas existentes. Evitar XSS vía `.html()` sin sanitizar (unalib ya escapa / construye embeds seguros).

## US-01 (in progress — not done until verified)

Auth0 Universal Login social; access token en API/Socket.IO; identidad desde `sub` validado.

Last reinforced 2026-10-28
