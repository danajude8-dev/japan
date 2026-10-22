# Le Japon, à notre rythme

Carnet de voyage de Dana et Mathieu · **29 mars–13 avril 2027** · 16 jours, 15 nuits.

React + Vite, prêt pour Vercel. Photos locales, 15 hôtels, itinéraire interactif, comparatif et budget en CHF. Tokyo 4 nuits, Matsumoto 2, Takayama 2, Kyoto 5, Osaka 2 ; variante Kyoto 6 / Osaka 1.

## Publier sur Vercel

1. Ouvrir https://vercel.com/new et se connecter avec GitHub.
2. Importer le dépôt **danajude8-dev/japan**. Si nécessaire, autoriser Vercel à accéder à ce dépôt.
3. Garder **Vite**, le dossier racine **./**, la commande de compilation **npm run build** et le dossier de sortie **dist**. Aucune variable d’environnement requise.
4. Cliquer sur **Deploy**. Vercel fournit le lien à partager.

La configuration est déjà dans `vercel.json`. Utiliser Node.js 24.x ou une version compatible >=22.12.
Documentation : https://vercel.com/docs/frameworks/frontend/vite

## Développement local

```sh
npm ci
npm run dev
```

Ouvrir l’adresse affichée. Pour vérifier la version de production :

```sh
npm test
npm run build
npm run preview
```

7 tests couvrent l’inventaire des hôtels, les 15 nuits et les 16 journées dans les deux variantes, les dates Booking, les budgets et les images.

## Contenu et limites

Les prix sont des fourchettes de préparation par chambre pour deux, **pas des tarifs vérifiés pour mars–avril 2027**. Aucun stock n’est confirmé. Les recherches Booking comprennent les dates, deux adultes et une chambre.

Les photos sont réelles et créditées, avec licences individuelles dans `CREDITS_PHOTOS.md`, `src/images.json` et le site. Niwa et Kanra ont une photo d’archive de l’hôtel. Les autres cartes montrent des vues de destination portant la légende « pas l’hôtel », et un lien mène à la galerie officielle.

Les choix d’hôtels sont mémorisés dans le navigateur, sans compte ni synchronisation. Les polices passent par Google Fonts avec des polices de repli. La mention « carnet privé » indique un usage personnel : le site n’a pas d’authentification. `noindex` ne protège pas l’accès.

Les réponses HTTP du contrôle initial sont documentées dans `VERIFICATION_LIENS.json`. Les paramètres ont ensuite été adaptés aux nouvelles dates et testés ; ils ne prouvent pas les disponibilités.

## Modifier

- `src/data.js` : destinations, journées, hôtels, dates, calculs et sources.
- `src/main.jsx` : interface et interactions.
- `src/style.css` : apparence et version mobile.
- `public/images/` et `src/images.json` : images et crédits.
