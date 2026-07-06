# My-Mind

Mein digitales Gehirn: Gedanken, Bücher, Videos, Ideen und Projekte als
verlinkte Markdown-Notizen in `content/`, veröffentlicht als interaktive,
durchklickbare Seite mit [Quartz](https://quartz.jzhao.xyz/).

## Struktur

- `content/index.md` – zentrale Kontext-/Startseite
- `content/buecher/` – gelesene Bücher
- `content/videos/` – Videolinks
- `content/ideen/` – Rohideen
- `content/projekte/` – aktive/pausierte Projekte
- `content/erfolge/` – dokumentierte Erfolge
- `content/gedanken/` – unsortierte Notizen, werden regelmäßig durchgesehen
- `content/mindset/` – Mindset-Notizen
- `content/wissen/` – Wissen/Learnings (Sales-Themen bekommen zusätzlich den Tag `sales`)
- `content/wissensvideos/` – gelernter Content aus Videos/Kursen: Link + Dateien/Sprachnachrichten als Anhang, dazu Zusammenfassung und Transkript zum Nachlesen
- `content/templates/` – QuickAdd-Vorlagen für neue Notizen (wird nicht veröffentlicht)

Notizen mit `[[wikilinks]]` verlinken – daraus baut Quartz automatisch die
interaktive Graph-Ansicht.

## Lokal entwickeln

```bash
npm install
npx quartz build --serve
```

Öffnet die Seite unter `http://localhost:8080` mit Live-Reload.

## Veröffentlichen (GitHub Pages)

Der Workflow `.github/workflows/deploy.yml` baut und deployed die Seite bei
jedem Push auf `main`.

1. In `quartz.config.ts` steht `baseUrl: "andreknig44-svg.github.io/My-Mind"` –
   bei anderem Domain-/Repo-Namen anpassen.
2. In den Repo-Einstellungen unter **Settings → Pages** die Quelle auf
   **GitHub Actions** stellen.
3. Bei Push auf `main` läuft der Workflow automatisch und veröffentlicht die
   Seite unter `https://andreknig44-svg.github.io/My-Mind/`.
