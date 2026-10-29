# Environments

URLs, paths, and ports. No secrets. Paths are relative to the repo layout.

## Workspace layout (confirmed)

- **Repositorio principal (Lab 8 + memoria):** `lab6-paradigma/`
- **Workspace oficial (versionado en el principal):** `my-team-workspace/my-team-workspace/`
- **Memoria (brain):** `my-team-workspace/my-team-workspace/brain/`
- **Desde el clon UNA Chat** (`Repos/lab5-paradigmas/`): memoria en `../../brain/`
- **Instrucciones brain (fuente):** `obsidian-brain-instructions 1.md` en la raíz de `lab6-paradigma/`

## Versionado

- Documentos del workspace (brain, Knowledge, Skills, AGENTS, reglas) se versionan desde el **repositorio principal** `lab6-paradigma`.
- UNA Chat en `Repos/lab5-paradigmas/` mantiene su **propio** repositorio Git (contenido ignorado por el principal salvo `Repos/AGENTS.md`).
- Historial Git previo del workspace: carpeta local `.git.backup-lab8-workspace/` (ignorada; no se publica).

## UNA Chat repository

- Path: `Repos/lab5-paradigmas/`
- Remote del proyecto: `https://github.com/ilovejdg2-lang/lab5-paradigmas.git`
- Origen local: `http://localhost:3000`
- Puerto: `3000` (`PORT`)

## Auth0 (identificadores públicos)

- Domain: `dev-no1ya3dw3r0fgsjz.us.auth0.com`
- Client ID (SPA, público): `liMsSpRB0TwB1dcXgNqsXIMY2eMdU6KT`
- Audience propuesto (confirmar en Dashboard): `https://una-chat-api`
- Callback / logout / web origin local: `http://localhost:3000` (raíz; no `/callback`)
- Dominio Vercel: pendiente `<VERCEL_DOMAIN>`

Last reinforced 2026-10-28
