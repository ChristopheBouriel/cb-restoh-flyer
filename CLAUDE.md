# CLAUDE.md - Flyer (RestOh Landing Page)

Ce fichier fournit le contexte complet pour travailler sur la landing page RestOh avec Claude Code.

## Vue d'ensemble du projet

**Flyer** est une landing page professionnelle pour présenter :
1. **RestOh** - Un SaaS complet de gestion de restaurant développé en solo
2. **Christophe Bouriel** - Développeur Full-Stack spécialisé Node.js

**Objectifs principaux :**
- Présenter RestOh de manière professionnelle et technique
- Démontrer les compétences de Christophe (missions critiques : Darva, Thales, Crédit Agricole)
- Générer des opportunités (freelance, missions remote)
- Diriger vers la démo (quand disponible) et les repos GitHub

---

## Stack Technique

```yaml
Framework: Astro 5.x (SSG, zero JS by default)
Styling: Tailwind CSS 4.x (@theme API)
TypeScript: Strict mode
Fonts:
  - Instrument Serif (headings)
  - Plus Jakarta Sans (body)
  - JetBrains Mono (code/metrics)
Deployment: Vercel ou Netlify (à configurer)
```

## Commandes

```bash
npm run dev      # Serveur dev (port 4321)
npm run build    # Build production
npm run preview  # Preview du build
```

---

## Architecture du Projet

```
Flyer/
├── public/
│   ├── favicon.svg          # Logo "CB" stylisé
│   └── og-image.png         # À créer (1200x630)
├── src/
│   ├── components/
│   │   ├── Navigation.astro  # Nav sticky avec mobile menu
│   │   ├── Hero.astro        # Section principale avec CTAs
│   │   ├── MetricsBar.astro  # Métriques clés (2000+ tests, etc.)
│   │   ├── Features.astro    # 3 cards (Customer, Admin, Security)
│   │   ├── TechStack.astro   # Technologies par catégorie
│   │   ├── About.astro       # Bio + expérience + disponibilité
│   │   ├── CTA.astro         # Call to action final
│   │   └── Footer.astro      # Copyright + liens
│   ├── layouts/
│   │   └── Layout.astro      # Layout principal (meta, fonts)
│   ├── pages/
│   │   └── index.astro       # Page unique (single page)
│   └── styles/
│       └── global.css        # Tailwind + custom theme
├── astro.config.mjs
├── tsconfig.json
└── package.json
```

---

## Direction Artistique

### Philosophie
**"Technical Excellence with Human Touch"** - Montrer l'expertise technique sans être froid ou inaccessible.

### Palette de couleurs (Dark Mode Teal)

```css
/* Définies dans src/styles/global.css via @theme */

/* Backgrounds */
--color-bg-primary: #0a0a0b;     /* Near black */
--color-bg-secondary: #111113;   /* Légèrement plus clair */
--color-bg-tertiary: #18181b;    /* Cards/elevated */

/* Text */
--color-fg-primary: #fafafa;     /* Blanc */
--color-fg-secondary: #a1a1aa;   /* Muted */
--color-fg-tertiary: #71717a;    /* Very muted */

/* Accent - Teal */
--color-accent: #14b8a6;         /* Teal 500 */
--color-accent-hover: #0d9488;   /* Teal 600 */

/* Borders */
--color-border: #27272a;
--color-border-hover: #3f3f46;
```

### Utilisation Tailwind (v4 @theme)

Les couleurs custom sont accessibles via les classes Tailwind :
```html
<div class="bg-bg-primary text-fg-primary">
<span class="text-accent hover:text-accent-hover">
<div class="border-border hover:border-border-hover">
```

### Typographie

```css
--font-sans: 'Plus Jakarta Sans'   /* Body, UI */
--font-serif: 'Instrument Serif'   /* Headings (H1, H2) */
--font-mono: 'JetBrains Mono'      /* Code, métriques */
```

Classes Tailwind : `font-sans`, `font-serif`, `font-mono`

### À ÉVITER
- ❌ Gradients violets génériques (AI slop)
- ❌ Fonts génériques (Inter, Roboto)
- ❌ Stock photos de personnes
- ❌ Animations excessives
- ❌ Design "template" sans personnalité

### À PRIVILÉGIER
- ✅ Palette sobre avec accent teal
- ✅ Typography distinctive (serif pour headings)
- ✅ Micro-interactions subtiles
- ✅ Code/terminal aesthetic
- ✅ Espaces blancs généreux

---

## Contenu par Section

### 1. Navigation
- Logo "CB" (font-serif, lien vers #)
- Liens : Project, Features, Stack, About
- CTA : "View on GitHub" (external)
- Mobile : hamburger menu

### 2. Hero (#project)
```
Headline: RestOh
Subheadline: A complete restaurant management SaaS — built solo, production-ready.
Description: Full-stack application featuring customer ordering, table reservations,
admin dashboard, and enterprise-grade security. Built with React, Node.js,
and MongoDB — backed by 2,000+ automated tests.
CTAs:
  - "Try the Demo" (disabled, "Coming Soon")
  - "View on GitHub" → https://github.com/ChristopheBouriel/restoh-frontend
```

### 3. Metrics Bar
| Métrique | Valeur |
|----------|--------|
| Automated Tests | 2,000+ |
| Backend Coverage | 84% |
| Status | Production Ready |
| Experience | 3+ Years |

### 4. Features (#features)
3 cards :

**Customer Experience**
- Menu browsing with filters & search
- Persistent shopping cart
- Online ordering (delivery/pickup)
- Interactive table reservations
- Reviews & ratings system
- GDPR-compliant account management

**Admin Dashboard**
- Real-time statistics
- Menu management with image upload
- Order status workflows
- Reservation calendar view
- User management
- Messaging inbox

**Security First**
- Dual-token authentication
- Server-side token revocation
- OWASP compliance
- Rate limiting & validation
- 84% test coverage
- Comprehensive E2E tests

### 5. Tech Stack (#stack)

| Catégorie | Technologies |
|-----------|--------------|
| Frontend | React 18, Vite, Zustand, React Hook Form, Tailwind CSS, Axios |
| Backend | Node.js, Express, MongoDB, Mongoose, JWT/bcrypt, Joi |
| Services | Stripe, Cloudinary, Brevo |
| Testing | Vitest, Jest, Playwright, React Testing Library |
| DevOps | Docker, GitHub Actions, MongoDB Atlas |

Liens GitHub :
- Frontend: https://github.com/ChristopheBouriel/restoh-frontend
- Backend: https://github.com/ChristopheBouriel/RestOh-back
- Docker: https://github.com/ChristopheBouriel/restoh-docker

### 6. About (#about)

**Bio :**
> Full-Stack Developer specializing in secure, scalable Node.js architectures.
> With 3+ years of professional experience on critical systems — banking at
> Crédit Agricole, aviation supply chain at Thales, and France's central
> insurance messaging at Darva — I bring enterprise-grade thinking to every project.
>
> Currently based in Laos, I'm open to remote opportunities and freelance
> collaborations.

**Expériences :**
- Darva (2 ans) - France's insurance messaging backbone
- Thales Avionics (8 mois) - Global aviation supply chain
- Crédit Agricole (5 mois) - Banking applications

**Badge :** "Open to remote opportunities" (avec animation pulse)

### 7. CTA
```
Headline: Let's work together
Subtext: Looking for a developer who delivers production-ready code with
comprehensive testing? Let's connect.
CTAs:
  - "Contact on LinkedIn" → https://www.linkedin.com/in/christophe-bouriel/
  - "View Full Project" → GitHub
```

### 8. Footer
- © 2025 Christophe Bouriel
- Liens : GitHub, LinkedIn
- Made with ♥ in Laos

---

## Liens Importants

```yaml
LinkedIn: https://www.linkedin.com/in/christophe-bouriel/
GitHub Profile: https://github.com/ChristopheBouriel
RestOh Frontend: https://github.com/ChristopheBouriel/restoh-frontend
RestOh Backend: https://github.com/ChristopheBouriel/RestOh-back
RestOh Docker: https://github.com/ChristopheBouriel/restoh-docker
```

---

## Le Projet RestOh (Contexte Technique)

RestOh est un SaaS complet de gestion de restaurant que Christophe a développé entièrement en solo. Voici les points clés à mettre en avant :

### Métriques Impressionnantes
```yaml
Tests Frontend: 1,620+ tests (unitaires, intégration, E2E)
Tests Backend: 422 tests
Total: 2,000+ tests automatisés
Coverage Backend: 84%
Image Docker: ~77MB (Alpine-based)
Suites E2E: 17 fichiers Playwright
```

### Architecture Sécurité (Dual-Token)
- Access Token : 15 min, stocké en mémoire uniquement
- Refresh Token : 24h (ou 7 jours avec "Remember Me"), cookie HTTP-only
- Auto-refresh transparent
- True logout (révocation serveur)
- Conformité OWASP (rate limiting, validation Joi, protection injection)

### Fonctionnalités Clés
**Client :** Menu, panier persistant, commandes (delivery/pickup), réservations avec carte interactive, avis, profil RGPD
**Admin :** Dashboard stats temps réel, gestion menu avec upload Cloudinary, workflows commandes/réservations, gestion utilisateurs, messagerie

---

## Responsive Design

### Breakpoints (Tailwind defaults)
```css
sm: 640px   /* Mobile landscape */
md: 768px   /* Tablet */
lg: 1024px  /* Desktop */
xl: 1280px  /* Large desktop */
```

### Adaptations principales
- Navigation : inline sur desktop, hamburger sur mobile
- Hero : text-6xl → text-4xl, CTAs empilés sur mobile
- Features : 3 cols → 2 cols → 1 col
- Tech Stack : grid responsive avec badges wrapping

---

## Animations

### Principes
- Purposeful (pas décoratives)
- Durées courtes (150-300ms)
- Easing naturel (ease-out)

### Animations définies
```css
--animate-slide-up: slide-up 0.5s ease-out;
--animate-fade-in: fade-in 0.5s ease-out;
```

### Usage avec délais (staggered)
```html
<div style="animation: slide-up 0.5s ease-out 100ms backwards;">
```

---

## SEO & Performance

### Meta Tags (déjà configurés dans Layout.astro)
- Title, description, keywords, author
- Open Graph (og:title, og:description, og:image)
- Twitter Card
- Canonical URL

### Targets Lighthouse
```yaml
Performance: 95+
Accessibility: 100
Best Practices: 100
SEO: 100
```

---

## Assets à Créer

### og-image.png (1200x630)
Image pour partage social - doit inclure :
- "RestOh" en grand
- Tagline
- Visuellement cohérent avec le design dark mode teal

### Screenshots (optionnel)
Si la démo RestOh est disponible, capturer des screenshots du dashboard pour la section Features.

---

## Prochaines Étapes

1. **Tester le responsive** sur tous les breakpoints
2. **Créer og-image.png** pour le partage social
3. **Optimiser pour Lighthouse** (vérifier les scores)
4. **Déployer sur Vercel/Netlify**
5. **Configurer le domaine** (suggestion : restoh.christophebouriel.dev)
6. **Activer le CTA "Try the Demo"** quand la démo sera live

---

## Notes de Développement

### Tailwind v4 (@theme API)
Ce projet utilise Tailwind CSS v4 avec la nouvelle syntaxe `@theme` dans `global.css`. Les variables custom sont automatiquement disponibles comme classes utilitaires (ex: `bg-bg-primary`, `text-accent`).

### Astro Components
Tous les composants sont en `.astro` (pas de React nécessaire pour une landing page statique). Le JS minimal est dans des balises `<script>` pour le menu mobile.

### Fonts via Google Fonts
Les fonts sont chargées via CDN dans `Layout.astro` avec `preconnect` pour la performance.

---

## Conventions

- **Composants** : PascalCase (`Hero.astro`)
- **Styles** : Classes Tailwind inline
- **Couleurs** : Utiliser les variables custom (`bg-bg-primary`, `text-accent`)
- **Liens externes** : Toujours `target="_blank" rel="noopener noreferrer"`
- **Accessibilité** : `aria-label` sur les boutons icon-only

---

**Dernière mise à jour :** Décembre 2024 - Setup initial avec tous les composants
