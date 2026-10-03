# finxorra-legal

Öffentliche Rechtstexte und Rücksprung-Seite für die Anwendung „FinXorra“ (selbst gehostet, private Nutzung), ausgeliefert über GitHub Pages.
Stand: FinXorra v0.7.0 (03.10.2026).

| Seite | Zweck |
|---|---|
| `index.html` | Startseite mit Links und Kontakt |
| `datenschutz/` | Datenschutzerklärung (DE/EN): Datenquellen (Enable Banking, FinTS, Trade Republic, Postfächer), Empfänger (LLM, logo.dev, OSM/OSRM, SMTP/Twilio), Speicherung, Widerruf |
| `nutzungsbedingungen/` | Nutzungsbedingungen (DE/EN) |
| `callback/` | Rücksprung-Seite für Enable Banking: reicht die Antwort der Bank (`state`/`code`/`error`) an die eigene FinXorra-Installation weiter, speichert nichts |

Nach dem Aktivieren von Pages (Branch `main`, Ordner `/`):

- Privacy URL: `https://<benutzer>.github.io/finxorra-legal/datenschutz/`
- Terms URL: `https://<benutzer>.github.io/finxorra-legal/nutzungsbedingungen/`
- Redirect-URL (in Enable Banking registrieren und als `ENABLE_BANKING_REDIRECT_URL` in der FinXorra-`.env` setzen): `https://<benutzer>.github.io/finxorra-legal/callback/`

## Pflege

- Die Texte beschreiben die Datenverarbeitung von FinXorra. Bei neuen Datenquellen, Empfängern oder Diensten (z. B. weiterer Cloud-Anbieter) **Datenschutzerklärung und Datum anpassen**. Quelle für den Abgleich ist `docs/FEATURES.md` im Repository `FinXorra`.
- Die erlaubten Weiterleitungsziele der Rücksprung-Seite stehen fest in `callback/index.html` (`TARGETS`, kein offener Redirect). Die Adressen/Ports müssen zur jeweiligen Installation passen (Dev-Frontend `:5173`, Produktiv-Frontend `FRONTEND_PORT`, Standard `:8080`).
- Die Texte sind keine Rechtsberatung und sollten bei wesentlichen Änderungen am Betrieb (z. B. weitere Nutzer, gewerbliche Nutzung) rechtlich geprüft werden.
