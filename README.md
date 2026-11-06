# My Finances

Applicazione web personale, mobile-first, per registrare manualmente entrate e uscite e consultare il riepilogo mese per mese.

## Funzioni MVP presenti
- Dashboard con saldo, entrate e uscite del mese.
- Inserimento manuale di entrate e uscite (descrizione, categoria, data, importo e note).
- Navigazione tra i mesi e grafico mensile.
- Esportazione CSV e backup JSON.
- Layout ottimizzato per iPhone e manifest per aggiunta alla Home.

## Stato importante: cloud non ancora attivo
La versione iniziale salva i movimenti nel localStorage del browser: non c'è ancora sincronizzazione tra dispositivi. Prima di inserire dati reali, completa la configurazione Supabase descritta in [docs/SUPABASE-SETUP.md](docs/SUPABASE-SETUP.md). Lo schema protetto è in [supabase/schema.sql](supabase/schema.sql).

## Sviluppo e pubblicazione
I file sono statici: `index.html`, `styles.css` e `app.js`. Possono essere serviti da un hosting statico.

Il repository è privato. GitHub Pages per repository privati richiede un piano GitHub Pro, Team o Enterprise; con GitHub Free il repository deve essere pubblico. Non rendere pubblico il repository senza averlo deciso consapevolmente.

## Sicurezza
- Non inserire password, token, Supabase Secret key o service_role key nel repository.
- La publishable key può stare nel client solo con RLS abilitato e policy ristrette.
- Lo schema SQL autorizza ogni utente autenticato ad accedere esclusivamente alle proprie righe.
