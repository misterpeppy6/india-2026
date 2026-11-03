# India 2026/27 — Web App mobile-first

Progetto creato a partire da `india.pdf`.

## Cosa contiene
- itinerario 25/12/2026–12/01/2027
- luoghi, gastronomia e principali trasferimenti estratti dalla guida
- ricerca e filtri
- preferiti
- link Google Maps senza API key
- pannello Aggiungi/Modifica/Elimina
- backup/import JSON
- PWA con cache essenziale
- API Cloudflare Pages Functions + D1 opzionale

## Prova locale semplice
Apri `dist/index.html` con un server statico locale. Le modifiche vengono salvate nel browser.

## Pubblicazione Cloudflare Pages + D1
1. Crea un database D1 chiamato `india-guide`.
2. Esegui `schema.sql` sul database.
3. Collega il database al progetto Pages con binding `DB`.
4. Imposta il secret `ADMIN_TOKEN` con una stringa lunga e casuale. Non inserirla nel codice.
5. Configura la directory di output Pages come `dist` e mantieni la cartella `functions` alla radice del progetto.
6. Pubblica. Dopo il deploy, apri ⚙︎ e inserisci il token amministratore solo quando devi sincronizzare.

## Foto
Ogni elemento ha un campo `photo`. Per garantire foto uniche e uso offline, aggiungi file immagine originali/licenziati nella cartella `dist/photos/` e usa URL relativi, oppure inserisci URL remoti consapevole che l'offline non è garantito. Non duplicare la stessa immagine in schede diverse.

## Nota sui treni
I collegamenti futuri importati dal PDF sono marcati `Da verificare` quando la guida stessa richiede riconferma.
