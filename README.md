# Lucca Demo — „Mord um das Vermächtnis“

Demo-/Sales-Fall von **Hidden Games** für Lucca Comics & Games 2026.
Diese Fassung ist **deutsch** und dient dem **internen Test**. Sie ist noch nicht öffentlich
angekündigt und trägt überall ein `noindex`.

## Zum Testen

| Was | Adresse |
|---|---|
| Fallakte (Startseite) | `/` |
| Pinnwände (ersetzen im Test die gedruckten Poster) | `/pinnwaende/` |
| Sprachnachricht | `/sprachnachricht.html` |
| Vernehmung | `/vernehmung.html` |

**Empfohlener Testablauf:** Fallakte lesen → Station 1 (Motive) → Station 2 (Alibis) →
zurück zur Fallakte, Verdacht eingeben. Die Hinweisleiter hat drei Stufen und ist bewusst
erst auf Knopfdruck sichtbar.

Bitte beim Testen mitschreiben: **Wie lange habt ihr gebraucht?** Ziel sind 25–30 Minuten.

## Was noch fehlt

- Porträts der sechs Verdächtigen (`assets/verdaechtige/`, Hochformat 3:4, ab 600 × 800 px).
  Von Kommissar Gallo gibt es bewusst **kein** Bild.
- Das Postfach `aurelio.sentieri@dschimail.com` existiert noch nicht. Der QR im Notizbuch auf
  Station 1 ist echt und führt auf `www.dschimail.com` — solange die Seite nicht steht, ins Leere.
- Die QR-Codes für Sprachnachricht und Vernehmung sind noch Attrappen (zufälliges Muster,
  kein scanbarer Code). Sie werden erzeugt, sobald diese Pages-URL steht.
- Die Auktionshaus-Mail (`arte-mc@gmx.de`) ist eine temporäre Testadresse mit Autoresponder.
- Die Audios sind KI-Testaufnahmen.
- Italienische Fassung folgt nach dem deutschen Test.

## Vor dem Livegang entfernen

In `index.html`, `sprachnachricht.html`, `vernehmung.html` und `pinnwaende/index.html`:

1. das gelb-schwarze Develop-Banner (`<div class="devbar">`)
2. `<meta name="robots" content="noindex, nofollow">`

Zusätzlich nur in `index.html`: der Button **„Auflösung anzeigen (intern)“** (`#btn-dev`) samt
Event-Listener.

**Die Pinnwände gehören vor dem Livegang aus dem Repository entfernt** — im fertigen Spiel
liegen sie gedruckt auf dem Tisch. Online sind sie nur für diese Testrunde.

## GitHub Pages

*Settings → Pages → Branch `main`, Ordner `/ (root)`.* Die Datei `.nojekyll` verhindert, dass
Jekyll die Seiten anfasst.

## Was hier bewusst NICHT liegt

Die Konzeptdokumente (`Konzept_v4_INTERN_mit_Loesung.docx` und die Testfassung) sowie die
Design-Backups bleiben in OneDrive. Das INTERN-Dokument enthält die vollständige Auflösung
und darf nicht in ein öffentliches Repository.
