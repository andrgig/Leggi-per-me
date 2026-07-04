# Leggi per me / Read It to Me

> Un'app web per persone ipovedenti: fotografa un documento e ascoltalo ad alta voce.
> A web app for people with low vision: photograph a document and have it read aloud. 

---

## Italiano

### Cos'è

"Leggi per me" è una piccola app web che usa l'intelligenza artificiale di Anthropic per leggere documenti fotografati. È pensata per persone anziane o ipovedenti che faticano a leggere testi su carta. Non richiede installazione, funziona dal browser del telefono e si aggiunge alla schermata home come un'app normale.

**Come funziona:**
1. L'utente fotografa un documento (ricetta medica, lettera, bolletta, ecc.)
2. L'app invia la foto all'API di Anthropic (Claude)
3. Claude estrae il testo e lo legge ad alta voce
4. L'utente può fare domande a voce sul documento ("puoi ripetere?", "cosa significa...?")

### Requisiti

- Telefono Android con Chrome (o iPhone con Safari)
- Connessione internet
- Una chiave API Anthropic (vedi sotto)

### Come ottenere la chiave API

1. Vai su [console.anthropic.com](https://console.anthropic.com) e crea un account
2. Nel menu a sinistra, clicca **API Keys**
3. Clicca **Create Key**, dai un nome a piacere (es. "Leggi per me")
4. Copia la chiave: inizia con `sk-ant-...`
5. Vai su **Billing** e aggiungi un metodo di pagamento. Puoi impostare un limite mensile (es. 5 euro) per stare tranquillo. Il costo per uso normale è di pochi centesimi al mese.

La chiave viene salvata solo sul telefono dell'utente (localStorage del browser). Non viene trasmessa a nessun server intermedio, va direttamente all'API Anthropic.

### Come pubblicare l'app su GitHub Pages

Se vuoi usare questa app, la strada più semplice è fare un fork di questo repository e abilitare GitHub Pages. In questo modo ottieni un indirizzo web (`https://...`) da cui installare l'app sul telefono.

**Passo 1: fork del repository**
1. In alto a destra su questa pagina, clicca il pulsante **Fork**
2. Scegli il tuo account GitHub come destinazione
3. Clicca **Create fork**

**Passo 2: abilitare GitHub Pages**
1. Nel tuo fork, clicca **Settings** (in alto)
2. Nel menu a sinistra, clicca **Pages**
3. Sotto "Branch", seleziona `main` e la cartella `/ (root)`
4. Clicca **Save**
5. Aspetta 1-2 minuti. Apparirà un link del tipo `https://tuonome.github.io/leggi-per-me/`

**Passo 3: aprire l'app sul telefono**
1. Apri Chrome sul telefono Android
2. Vai all'indirizzo che hai ottenuto nel passo 2
3. L'app si apre nel browser. La prima volta chiede la chiave API: inseriscila una sola volta, viene salvata automaticamente.

**Passo 4: aggiungere alla schermata home**
1. In Chrome, tocca i **tre puntini** in alto a destra
2. Seleziona **"Aggiungi a schermata Home"** oppure **"Installa app"**
3. Conferma. Apparirà un'icona sulla home del telefono.

Da quel momento, aprire l'app è come aprire qualsiasi altra app.

### Aggiornare la chiave API

Se la chiave scade o vuoi cambiarla, in fondo all'app c'è il pulsante **"Cambia chiave API"**.

---

## English

### What is it

"Read It to Me" is a small web app that uses Anthropic's AI to read photographed documents aloud. It is designed for elderly or visually impaired people who have difficulty reading printed text. No installation is required: it runs in the phone's browser and can be added to the home screen like a regular app.

**How it works:**
1. The user photographs a document (prescription, letter, utility bill, etc.)
2. The app sends the photo to the Anthropic API (Claude)
3. Claude extracts the text and reads it aloud
4. The user can ask voice questions about the document ("can you repeat that?", "what does ... mean?")

### Requirements

- Android phone with Chrome (or iPhone with Safari)
- Internet connection
- An Anthropic API key (see below)

### How to get an API key

1. Go to [console.anthropic.com](https://console.anthropic.com) and create an account
2. In the left menu, click **API Keys**
3. Click **Create Key**, give it any name (e.g. "Read It to Me")
4. Copy the key: it starts with `sk-ant-...`
5. Go to **Billing** and add a payment method. You can set a monthly spending limit (e.g. $5) to stay in control. Normal use costs only a few cents per month.

The key is stored only on the user's phone (browser localStorage). It is never sent to any intermediate server; it goes directly to the Anthropic API.

### How to publish the app on GitHub Pages

The easiest way to use this app is to fork this repository and enable GitHub Pages. This gives you a web address (`https://...`) from which you can install the app on your phone.

**Step 1: fork the repository**
1. Click the **Fork** button at the top right of this page
2. Choose your GitHub account as the destination
3. Click **Create fork**

**Step 2: enable GitHub Pages**
1. In your fork, click **Settings** (at the top)
2. In the left menu, click **Pages**
3. Under "Branch", select `main` and the `/ (root)` folder
4. Click **Save**
5. Wait 1-2 minutes. A link will appear like `https://yourname.github.io/leggi-per-me/`

**Step 3: open the app on your phone**
1. Open Chrome on your Android phone
2. Go to the address you got in step 2
3. The app opens in the browser. The first time it asks for the API key: enter it once and it is saved automatically.

**Step 4: add to the home screen**
1. In Chrome, tap the **three dots** in the top right
2. Select **"Add to Home screen"** or **"Install app"**
3. Confirm. An icon will appear on the phone's home screen.

From that point on, opening the app works like any other app.

### Updating the API key

If the key expires or you want to change it, there is a **"Cambia chiave API" (Change API key)** button at the bottom of the app.

---

## Struttura del repository / Repository structure

```
/
├── index.html       # App completa / Full app (single file)
├── manifest.json    # PWA manifest per installazione / for installation
├── LICENSE          # MIT License
└── README.md        # Questo file / This file
```

> Le icone (`icon-192.png`, `icon-512.png`) sono opzionali. Senza di esse l'app funziona ugualmente ma usa un'icona generica sulla schermata home.
>
> The icons (`icon-192.png`, `icon-512.png`) are optional. Without them the app works fine but uses a generic icon on the home screen.

---

## Licenza / License

MIT — libero uso, modifica e distribuzione. Vedi [LICENSE](LICENSE).  

MIT — free to use, modify, and distribute. See [LICENSE](LICENSE).
