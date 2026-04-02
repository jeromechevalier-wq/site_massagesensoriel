# CLAUDE.md — site_massagesensoriel

## Contexte du projet

Site web pour **Jérôme Chevalier**, praticien en massage sensoriel. Le projet est en phase de **conception/prototypage** : plusieurs pistes de design sont explorées en parallèle sous forme de dossiers indépendants. Il n'y a pas encore de framework ou de build system — tout est en HTML/CSS vanilla + Tailwind CDN.

## Structure du dépôt

```
site_massagesensoriel/
├── DESIGN.md                          # Système de design de référence ("The Grounded Sanctuary")
├── design-test.html                   # Page de test visuel de la palette et des composants
├── index.html                         # Prototype principal (Tailwind CDN)
├── tantric_terra/                     # Piste de design alternative 1
│   └── DESIGN.md
├── idee02/                            # Piste de design alternative 2
│   ├── DESIGN.md
│   ├── code.html
│   └── screen.png
├── la_belle_vibration_accueil/        # Piste de design alternative 3
│   ├── code.html
│   └── screen.png
└── massage_sensoriel_j_r_me_chevalier/ # Piste de design alternative 4
    ├── code.html
    └── screen.png
```

## Système de design de référence

Le fichier `DESIGN.md` à la racine est **la source de vérité** pour toutes les décisions visuelles. S'y référer avant toute modification de style.

### Tokens essentiels

| Token | Valeur | Usage |
|---|---|---|
| `surface` | `#fcf9f4` | Fond de base |
| `surface-container-low` | `#f6f3ee` | Séparation de sections |
| `surface-container` | `#f0ede8` | Fond de cartes |
| `surface-container-lowest` | `#ffffff` | Cartes flottantes |
| `primary` | `#883528` | CTA, accents |
| `primary-container` | `#a64c3e` | Gradient CTA |
| `on-surface` | `#1c1c19` | Texte "noir" |
| `on-surface-variant` | `#6b635d` | Texte secondaire |
| `secondary-fixed-dim` | `#f9ba76` | Soulignement bouton tertiary |

### Typographie

- **Titres** : `Noto Serif` (display, headline)
- **Corps** : `Manrope` (title, body, label)
- Chargées via Google Fonts CDN

### Règles absolues

- **Pas de bordures 1px** pour séparer les sections — utiliser des transitions de fond
- **Pas de `#000000`** — utiliser `on-surface` (`#1c1c19`)
- **Pas de coins à 0px** — `border-radius: 0.25rem` minimum
- **Pas de lignes de séparation dans les listes** — utiliser `gap: 4rem`
- **Espace vertical entre sections** : `8.5rem`
- La nav flottante utilise le glassmorphism : `rgba(#fcf9f4, 0.70)` + `backdrop-filter: blur(24px)`
- Les CTA primaires utilisent un gradient : `#883528` → `#a64c3e`

## Stack technique

- HTML5 + CSS vanilla (variables CSS custom properties)
- **Tailwind CSS** via CDN (`cdn.tailwindcss.com`) — pas de build step
- Google Fonts (Noto Serif + Manrope)
- Pas de JavaScript framework
- Pas de bundler

## Conventions de code

- Les couleurs sont définies en **CSS custom properties** (`:root { --primary: #883528; }`) dans les fichiers vanilla
- Dans les fichiers Tailwind, les couleurs sont étendues dans `tailwind.config` en ligne dans le `<script id="tailwind-config">`
- Les fichiers HTML sont autonomes (tout en un seul fichier)

## Ce qu'il ne faut pas faire

- Ne pas introduire de framework JavaScript (React, Vue, etc.) sans validation explicite
- Ne pas ajouter de build system (Vite, Webpack) sans validation explicite
- Ne pas créer de fichiers CSS séparés sauf si demandé
- Ne pas "optimiser" l'espace blanc — le layout doit sembler lent et aéré intentionnellement
