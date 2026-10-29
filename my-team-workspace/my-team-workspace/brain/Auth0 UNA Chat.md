# Auth0 UNA Chat

Conceptual configuration. **No secrets.**

## Application (confirmed by student)

- Type: Single Page Application
- Name: Proyecto
- Domain: `dev-no1ya3dw3r0fgsjz.us.auth0.com`
- Client ID: `liMsSpRB0TwB1dcXgNqsXIMY2eMdU6KT`
- Local origin (approved): `http://localhost:3000` (not 5173)

## SDK choice (decision)

`@auth0/auth0-spa-js` — Authorization Code + PKCE. No React.

## Three separate URL concepts

1. **Auth0 Application URLs** (Allowed Callback / Logout / Web Origins) → UNA Chat origins.
2. **Social provider → Auth0 callback** (configured inside the Google/GitHub connection; Auth0 shows the exact URL).
3. **UNA Chat backend CORS** (`FRONTEND_ORIGIN`) — Express `Access-Control-Allow-Origin`, not an Auth0 Application field.

## API / audience (proposed, pending Dashboard)

- Identifier proposed: `https://una-chat-api` (not a hosted page; Auth0 API identifier only).

## US-01 status

**Code implemented** in `Repos/lab5-paradigmas` (auth0-spa-js CDN 2.1.3, jose JWT, socket auth). Automated JWT tests pass. **Social login not verified** until a real IdP login succeeds. Audience `https://una-chat-api` still **proposed** until Dashboard confirmation.

Last reinforced 2026-10-28

