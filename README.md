# Regnanalys

Webbapp för löpande summering och maxanalys av nederbördsdata från Excel/CSV.

## Struktur

- `public/index.html` – hela webbappen
- `wrangler.jsonc` – Cloudflare Workers-konfiguration

## GitHub → Cloudflare Workers

1. Ladda upp denna mappstruktur i ett GitHub-repo (t.ex. `regnanalys`).
2. I Cloudflare: Workers & Pages → `divine-dream-fca0` → Settings → Builds → Connect.
3. Anslut GitHub-repot med produktiongren `main`.
4. Lämna **Build command** tomt. Ange **Deploy command** `npx wrangler deploy`. Root directory `/`.
5. En ny push till `main` publicerar appen automatiskt.

OBS: Om befintliga Workern i Cloudflare har bytt namn måste `name` i wrangler.jsonc ändras till exakt det namnet innan publicering.

Användardata laddas upp lokalt till webbläsaren. Ingen exempelfil ingår i källkoden.
