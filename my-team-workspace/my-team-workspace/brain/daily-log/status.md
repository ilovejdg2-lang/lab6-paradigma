# Status

## Current focus

**BLOQUEO Auth0 (evidenciado):** `access_denied` / `Service not found: https://una-chat-api`.
Las Callback URLs de localhost ya permiten el retorno; falta crear la API con ese Identifier.

## Verificado de verdad

- SDK + botón ejecutan `loginWithRedirect` → `/authorize` real (PKCE, audience, redirect_uri).
- Auth0 responde: Service not found para audience `https://una-chat-api`.
- Bug UI corregido: ya no se pisa el error de Auth0 ni se etiqueta todo `access_denied` como «Cancelaste».
- Evidencia: `evidencias/12-auth0-service-not-found.txt`

## Waiting on

Persona: Create API Identifier `https://una-chat-api` + autorizar a la SPA → Ctrl+F5 → login.

Last reinforced 2026-10-28
