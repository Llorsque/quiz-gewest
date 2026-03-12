# 🎯 Quiz Scorebord

Een visueel scorebord voor pub quizzen. Eén HTML-bestand, geen installatie nodig. Werkt via GitHub Pages.

---

## 🚀 Live zetten via GitHub Pages

1. Upload `index.html` en `README.md` naar je repository
2. Ga naar **Settings → Pages**
3. Kies bij *Branch*: `main` → map: `/ (root)` → klik **Save**
4. Na een minuutje is je scorebord live op:
   ```
   https://<jouw-gebruikersnaam>.github.io/<repo-naam>/
   ```

---

## 📺 Gebruik tijdens de quiz

Het scorebord heeft twee schermen, bereikbaar via de URL:

| Scherm | URL | Voor wie |
|--------|-----|----------|
| **Admin** | `https://…/#admin` (of gewoon `/`) | Quizmaster op laptop |
| **Scorebord** | `https://…/#display` | Grote schermen / beamer |

### Stap-voor-stap

1. **Open de admin-URL** op je laptop
2. Stel in: quiznaam + aantal rondes → klik **Toepassen**
3. Voeg teams toe (tot 12 teams)
4. **Open de display-URL** in een nieuw tabblad → sleep dat venster naar je grote schermen
5. Na elke ronde: vul de punten in via de scoretabel
6. Druk op de grote paarse knop **"Presenteer stand na ronde X"**
7. Het scorebord op de grote schermen animeert **automatisch** naar de nieuwe stand

> 💡 De twee tabs communiceren live via BroadcastChannel + localStorage — geen server of internet vereist zolang beide tabs open zijn op hetzelfde apparaat.

---

## 🎨 Scorebord-weergave

- **Rangschikking** op totaalpunten, automatisch bijgewerkt
- **Goud / zilver / brons** badge voor de top 3
- **Geanimeerde scorebalk** — hoe meer punten, hoe langer de balk
- **Header** toont altijd: *Stand na X/Y rondes*
- Smooth animatie bij elke nieuwe ronde-onthulling

---

## 🔧 Technische details

- Eén enkel HTML-bestand (`index.html`), geen frameworks of build-stap
- Data opgeslagen in `localStorage` (blijft bewaard bij herladen)
- Cross-tab sync via de [BroadcastChannel API](https://developer.mozilla.org/en-US/docs/Web/API/BroadcastChannel) + Storage Events
- Werkt in alle moderne browsers (Chrome, Firefox, Safari, Edge)
