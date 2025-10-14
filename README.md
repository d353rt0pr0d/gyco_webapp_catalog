# GYCO WebApp Catalog

[![Built with Google Apps Script](https://img.shields.io/badge/Built_with-Google_Apps_Script-blue.svg)](https://www.google.com/script/start/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Un catalogo virtuale, moderno e dinamico, per esporre un portfolio di applicazioni web. Sviluppato interamente su piattaforma Google Apps Script, utilizza un Google Sheet come database semplice e intuitivo.

![GYCO WebApp Catalog in azione](LINK_ALLA_TUA_IMMAGINE_O_GIF.gif)
*(Suggerimento: Sostituisci il link sopra con uno screenshot o, ancora meglio, una GIF animata che mostra i filtri e la ricerca in azione!)*

## 📜 Descrizione

Questo progetto nasce dall'esigenza di creare una vetrina elegante e funzionale per presentare una collezione di Web App realizzate con Google Apps Script. L'applicazione funge da "meta-catalogo", leggendo i dati da un semplice foglio di calcolo Google e presentandoli attraverso un'interfaccia reattiva, accattivante e ricca di animazioni.

È la soluzione ideale per sviluppatori, studenti o aziende che vogliono mostrare il proprio portfolio di progetti in modo professionale e centralizzato, senza la necessità di un database o un hosting complesso.

## ✨ Funzionalità Principali

-   **Database su Google Sheets:** Gestisci l'intero catalogo da un unico foglio di calcolo, facile da aggiornare e manutenere.
-   **Interfaccia Moderna a Card:** Un layout pulito e visivamente piacevole, ispirato agli app store moderni.
-   **Filtro Dinamico per Categorie:** Filtra istantaneamente le app visualizzate in base alla categoria di appartenenza.
-   **Ordinamento Multi-criterio:** Ordina le app per data di creazione (crescente/decrescente) o per ordine alfabetico.
-   **🔍 Ricerca Testuale Istantanea:** Trova rapidamente le app digitando parole chiave nel campo di ricerca globale.
-   **🎨 Tema Light & Dark:** Offre una doppia modalità di visualizzazione (chiara e scura) con salvataggio automatico della preferenza dell'utente.
-   **Scheda di Dettaglio Modale:** Cliccando su una card si apre una finestra modale con l'immagine ingrandita e una descrizione dettagliata (supporta la formattazione HTML).
-   **Layout Reattivo:** L'interfaccia si adatta perfettamente a qualsiasi dispositivo, dal desktop allo smartphone.
-   **Animazioni Fluide:** Grazie alla libreria **Isotope.js**, i filtri e gli ordinamenti sono accompagnati da transizioni animate ed eleganti.

## 🚀 Stack Tecnologico

-   **Backend:** **Google Apps Script** (`Code.gs`)
    -   Serve l'interfaccia utente.
    -   Espone API per recuperare i dati in modo asincrono.
-   **Frontend:** **HTML5, CSS3, JavaScript** (`index.html`, `style.html`, `js.html`)
    -   Struttura semantica e accessibile.
    -   Stile moderno con variabili CSS per la gestione dei temi.
    -   Logica client-side per la manipolazione del DOM e le chiamate API.
-   **Database:** **Google Sheets**
-   **Librerie Esterne:**
    -   **Isotope.js:** Per la gestione della griglia, i filtri e gli ordinamenti animati.
    -   **Google Material Symbols:** Per un set di icone pulito e coerente.

## 🔧 Installazione e Configurazione

Per replicare questo progetto, segui questi passaggi:

1.  **Crea un Google Sheet:**
    -   Crea un nuovo foglio di calcolo e rinomina il primo foglio in `Foglio1`.
    -   Configura le colonne come specificato nella sezione **Struttura Dati**.
    -   Popola il foglio con i dati delle tue Web App.
    -   **Importante:** Per le immagini, usa link diretti da un servizio di hosting/CDN (es. GitHub, Cloudinary) per massima compatibilità.

2.  **Crea un Progetto Apps Script:**
    -   Crea un nuovo progetto Apps Script.
    -   Copia il contenuto dei file `Code.gs`, `index.html`, `style.html` e `js.html` nei rispettivi file all'interno dell'editor.

3.  **Collega lo Script al Foglio:**
    -   Apri il file `Code.gs` e sostituisci il placeholder `'INSERISCI_QUI_ID_DEL_TUO_FOGLIO_GOOGLE'` con l'ID del tuo Google Sheet.

4.  **Esegui il Dispiegamento:**
    -   Clicca su **Esegui dispiegamento** > **Nuovo dispiegamento**.
    -   Seleziona il tipo "Applicazione web".
    -   Configura l'accesso (es. "Chiunque") e autorizza lo script.
    -   Copia l'URL `/exec` generato per accedere al tuo catalogo.

## 📊 Struttura Dati (Google Sheet)

Il foglio `Foglio1` deve avere le seguenti colonne:

| Colonna | Nome | Tipo Dato | Descrizione |
| :--- | :--- | :--- | :--- |
| A | `id` | Numero | Un identificatore numerico unico per ogni app. |
| B | `AppScript Name` | Stringa | Il nome completo dell'applicazione. |
| C | `Created` | Data | La data di creazione (usata per l'ordinamento). |
| D | `Category` | Stringa | La categoria di appartenenza (es. "Lavoro", "Scuola"). |
| E | `Deployment Link`| Stringa | L'URL `/exec` della Web App. |
| F | `Description` | Stringa | Descrizione dettagliata. Può contenere tag HTML. |
| G | `ImgUrl` | Stringa | **Link diretto e pubblico** all'immagine di anteprima. |
| H | `Icon` | Stringa | Il nome di un'icona [Material Symbol](https://fonts.google.com/icons). |

## 📄 Licenza

Questo progetto è rilasciato sotto la Licenza MIT. Vedi il file `LICENSE` per maggiori dettagli.
