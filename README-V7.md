# INDIA 2026/27 V7 MODIFICABILE

## Attivazione D1
1. In Cloudflare: Storage & Databases > D1 SQL Database > Create database. Nome: `india-2026-db`.
2. Copiare il Database ID in `wrangler.jsonc` al posto di `INCOLLA_QUI_DATABASE_ID`.
3. Da terminale nella cartella del progetto: `npx wrangler d1 execute india-2026-db --remote --file=schema.sql`.
4. Impostare il PIN segreto: `npx wrangler secret put ADMIN_PIN`.
5. Fare commit e push. Cloudflare eseguirà il deployment.

Dalla Web App: premere `PIN`, inserire il PIN scelto, poi `+ Aggiungi`.
