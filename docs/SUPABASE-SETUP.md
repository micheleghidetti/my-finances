# Configurazione cloud (Supabase)

Il codice iniziale dell'app è stato caricato su GitHub. L'archiviazione cloud non è ancora attiva: prima occorre creare il progetto Supabase e collegare l'app.

## 1. Crea il progetto
1. Apri https://supabase.com/dashboard e crea un progetto.
2. Scegli una password robusta per il database e conservala in un password manager.
3. Aspetta che il progetto sia pronto.

## 2. Crea la tabella protetta
1. Nel progetto apri **SQL Editor**.
2. Apri il file `supabase/schema.sql` di questo repository.
3. Copia il contenuto nell'editor SQL e premi **Run**.
4. In **Authentication > Providers**, verifica che Email sia abilitato.

Lo schema abilita Row Level Security e limita ogni operazione alle righe con `user_id` uguale all'utente autenticato. Non disattivare RLS.

## 3. Dati da passare per completare il collegamento
Dal pannello Supabase apri **Connect** (oppure **Settings > API Keys**) e recupera:
- Project URL
- Publishable key (inizia con `sb_publishable_`)

La publishable key è destinata al client, ma può essere usata in sicurezza solo con RLS e policy corrette. **Non condividere mai la Secret key o la vecchia service_role key** e non inserirle in GitHub. La configurazione conterrà solo Project URL e Publishable key.

Quando il progetto è pronto, comunica Project URL e Publishable key in un canale che ritieni appropriato. Con questi valori si può completare il login, il salvataggio cloud e la sincronizzazione tra dispositivi.

## Stato dei dati nell'MVP
Finché il collegamento non è attivo, la versione iniziale usa il localStorage del browser. I movimenti restano su quel browser e non vengono sincronizzati su iPhone, Mac o altri dispositivi. Usa **Impostazioni > Scarica backup JSON** per conservarne una copia. Non registrare movimenti reali finché non è attiva la sincronizzazione cloud.
