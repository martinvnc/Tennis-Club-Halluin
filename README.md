# 🎾 Tennis Club Halluin — Application Web

Application web officielle du **Tennis Club Halluin (TCH)** — Depuis 1927.

> Projet privé — Développé avec Claude Code

---

## Stack technique

| Couche | Technologie |
|--------|-------------|
| Framework | Next.js 14 (App Router) |
| Styling | Tailwind CSS + Shadcn/UI |
| Base de données | Supabase (PostgreSQL + Auth + Realtime) |
| Emails | Resend |
| Déploiement | Vercel |
| Images | next/image |

---

## Structure du projet

```
tch-halluin/
├── public/
│   └── assets/
│       ├── logos/                  # Logos officiels TCH (PNG)
│       └── photos/
│           ├── comite/             # Photo du comité
│           ├── soiree-fluo/        # Photos soirée fluo (18 photos)
│           ├── stage-vacances/     # Photos stage jeunes (4 photos)
│           └── resultats/          # Visuels résultats (6 cards)
├── src/
│   ├── app/                        # App Router Next.js 14
│   │   ├── (public)/               # Pages publiques
│   │   ├── (auth)/                 # Pages connexion/inscription
│   │   ├── mon-compte/             # Espace membre
│   │   ├── entraineur/             # Espace entraîneur
│   │   └── admin/                  # Dashboard admin
│   ├── components/
│   │   ├── ui/                     # Composants Shadcn/UI
│   │   └── tch/                    # Composants spécifiques TCH
│   ├── lib/
│   │   ├── supabase/               # Client Supabase
│   │   └── utils/                  # Utilitaires
│   └── styles/
│       └── globals.css
├── supabase/
│   └── migrations/                 # Fichiers SQL (schéma complet)
├── .env.example                    # Template variables d'environnement
├── PROMPT_CLAUDE_CODE.md           # Document de référence pour Claude Code
└── README.md
```

---

## Démarrage rapide

### 1. Cloner le repo

```bash
git clone https://github.com/martinvnc/Tennis-Club-Halluin.git
cd Tennis-Club-Halluin
```

### 2. Installer les dépendances

```bash
npm install
```

### 3. Configurer les variables d'environnement

```bash
cp .env.example .env.local
# Remplir les valeurs dans .env.local
```

### 4. Lancer en développement

```bash
npm run dev
```

Ouvrir [http://localhost:3000](http://localhost:3000)

---

## Variables d'environnement

Voir `.env.example` pour la liste complète.

Les clés nécessaires :
- **Supabase** : URL + anon key + service role key → [supabase.com](https://supabase.com)
- **Resend** : API key → [resend.com](https://resend.com)

---

## Charte graphique

| Couleur | HEX | Usage |
|---------|-----|-------|
| Vert foncé | `#4c7650` | Couleur principale, boutons, titres |
| Vert clair | `#639268` | Secondaire, hover, badges |
| Jaune balle | `#f6ca73` | Accent, CTA, logo |
| Blanc | `#ffffff` | Fond, cartes |

Police : **Quicksand** (Google Fonts) — 400 / 700 / 800

---

## Logos

| Fichier | Usage |
|---------|-------|
| `logo-vert-header.png` | Header (fond blanc) |
| `logo-blanc-complet.png` | Footer avec tagline (fond vert) |
| `logo-blanc-footer.png` | Footer compact / favicon (fond vert) |

> ⚠️ Toujours utiliser `next/image` avec ces fichiers. Jamais de CSS ou SVG à la place.

---

## Documentation

Le fichier **`PROMPT_CLAUDE_CODE.md`** à la racine contient :
- Toutes les règles de développement
- Le schéma SQL complet
- Les règles métier
- Le seed data de démonstration
- L'ordre de développement recommandé

---

## Déploiement

Le projet est déployé sur **Vercel** avec CI/CD automatique depuis la branche `main`.

---

## Club

**Tennis Club Halluin (TCH)**  
341 rue de la Lys, 59250 Halluin  
contact@tch.fr  
Depuis 1927 🎾
