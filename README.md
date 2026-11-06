# My Finances

Applicazione web personale, mobile-first, per registrare manualmente entrate e uscite e consultare il riepilogo mese per mese.

## Stato attuale

Prima versione dell'interfaccia (MVP):
- dashboard con saldo, entrate e uscite del mese;
- inserimento manuale di entrate e uscite con descrizione, categoria, data e note;
- navigazione tra i mesi;
- grafico giornaliero essenziale;
- esportazione CSV e backup JSON;
- layout ottimizzato per iPhone e metadati per l'aggiunta alla Home.

## Avvio

Aprire `index.html` con un server statico oppure pubblicare il repository con GitHub Pages.

## Importante: persistenza dei dati

Questa prima versione salva temporaneamente i movimenti in `localStorage` del browser. **Non è ancora sincronizzata con il cloud** e i dati non sono condivisi tra dispositivi. Prima di inserire dati finanziari reali, va completata l'integrazione Supabase con autenticazione, policy Row Level Security e backup.

## Prossimi passaggi

1. Creare un progetto Supabase.
2. Configurare autenticazione e tabella dei movimenti con policy RLS.
3. Aggiungere il client Supabase e migrare i movimenti locali.
4. Abilitare GitHub Pages e testare l'installazione su iOS.

Non inserire mai nel repository password, service-role key o altre chiavi segrete.
