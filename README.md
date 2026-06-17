# ON TEAM Evolution — Site officiel

Site vitrine premium (HTML/CSS, sans build) pour ON TEAM Evolution —
agence de team building, séminaires & événements d'entreprise à Casablanca.

## Structure

```
.
├── index.html              ← Page d'accueil (servie sur « / »)
├── qui-sommes-nous.html    ← Page « Qui sommes-nous ? »
├── favicon.png             ← Favicon (logo ON TEAM)
├── apple-touch-icon.png    ← Icône iOS
├── netlify.toml            ← Config Netlify (aucun build requis)
└── assets/
    └── images/             ← Photos réelles + logo source (prêtes à intégrer)
        ├── team-building-outdoor.jpg
        ├── paintball.jpg
        ├── coaching-equipe.jpg
        ├── seminaire-salle.jpg
        └── logo.png
```

Chaque page est **autonome** : CSS et images (base64) sont embarqués,
seules les Google Fonts sont externes. Rien à compiler.

## Déployer sur Netlify (via GitHub)

1. **Créer le dépôt GitHub** et y pousser ces fichiers :
   ```bash
   git init
   git add .
   git commit -m "ON TEAM — site initial"
   git branch -M main
   git remote add origin https://github.com/VOTRE-COMPTE/onteam-site.git
   git push -u origin main
   ```
2. Sur **app.netlify.com** → **Add new site → Import an existing project**.
3. Choisir **GitHub** puis le dépôt `onteam-site`.
4. Réglages de build :
   - **Build command** : *(laisser vide)*
   - **Publish directory** : `.` (la racine)
5. **Deploy site**. Netlify fournit une URL `xxxx.netlify.app`.
6. (Optionnel) **Domain settings** → brancher un domaine personnalisé.

Toute modification poussée sur `main` redéploie automatiquement.

## Pages & navigation

| URL | Statut |
|-----|--------|
| `/` (accueil) | ✅ en ligne |
| `/qui-sommes-nous.html` | ✅ en ligne |
| `/nos-prestations.html` | ⏳ à créer |
| `/galerie.html` | ⏳ à créer |

> Les liens « Nos prestations » et « Galerie » renverront un 404 tant que
> ces pages ne sont pas ajoutées (mêmes navbar/footer/design system).

## Notes

- Les **photos réelles** sont rangées dans `assets/images/` (optimisées web),
  prêtes à remplacer les visuels temporaires de « Qui sommes-nous ? ».
- Design system de référence : `DESIGN_SYSTEM_ON_TEAM.docx`.
