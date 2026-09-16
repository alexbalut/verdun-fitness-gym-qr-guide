# Verdun Fitness Gym QR Guide (unofficial demo)

**QR machine-instruction app skinned for a Verdun Fitness club demo.** Members scan a QR on a machine → bilingual (EN/FR) how-to guide. Staff manage machines, download QRs, print floor sheets, and review ROI insights.

> **Unofficial demo mockup for pitching only.** Not affiliated with Verdun Fitness or any parent company. Does **not** use official logo image assets — text wordmark only. Brand colors (`#FF9800` / `#14120C`) are approximate pitch tokens.

Seeded demo gym: **Verdun Fitness**. `/` is the **demo-ready member product UI** — not a marketing landing page.

Sibling (generic GymQR Guide): [gym-machine-qr-guide](https://github.com/alexbalut/gym-machine-qr-guide)

## Disclaimer

This repository is an **unofficial product demo**. Verdun Fitness® and related marks belong to their respective owners. Do not represent this app as an official Verdun Fitness product. No official logos are bundled.

## Quick start

```bash
cd verdun-fitness-gym-qr-guide
cp .env.example .env
npm install
npx prisma db push
npm run seed
npm run dev
```

Or one-shot setup:

```bash
npm install && npm run setup && npm run dev
```

Open [http://localhost:3000](http://localhost:3000) — member gym home for **Verdun Fitness** (Machines / Workout / Progress / Scan).

## Demo credentials

| Field    | Value                    |
|----------|--------------------------|
| Email    | `admin@verdun-fitness.demo`        |
| Password | `demo1234`             |
| Gym      | Verdun Fitness                |
| Slug     | `verdun-fitness`           |

Seed creates **10 bilingual machines**, sample view counts, and a few open/resolved issues.

## Branding notes

- Surfaces use secondary `#14120C` with primary accent **`#FF9800`**
- Text wordmark **Verdun Fitness** — no trademarked logo files
- Tagline: “South-west independent”

## Key routes

| Route | Description |
|-------|-------------|
| `/` | Gym member home |
| `/scan` | Camera QR scan |
| `/q/[token]` | Machine guide |
| `/m/verdun-fitness/[machineSlug]` | Friendly slug URL |
| `/admin/login` | Staff login |
| `/admin/insights` | Owner ROI dashboard |

## Caveats

- Auth is simple credential + JWT cookie — fine for demo; harden for production.
- SQLite at `prisma/dev.db` — don’t commit it.
- Member workout/progress is browser localStorage only (`verdun-fitness-workout:v1:<slug>`).
- Unofficial branding — do not ship as an official Verdun Fitness app.

## Photo credits

Demo photos under `public/machines/` are from Unsplash — see [CREDITS.md](./CREDITS.md). Not official Verdun Fitness assets.

## License / affiliation

This repository is an **unofficial product demo mockup** for pitch purposes. Verdun Fitness® and related marks belong to their respective owners. Do not represent this app as an official Verdun Fitness product.

## Repo

https://github.com/alexbalut/verdun-fitness-gym-qr-guide
