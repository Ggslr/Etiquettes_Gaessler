# Etiquettes_Gaessler

Application web de création d'étiquettes produits pour Horticulture GAESSLER.

## Contenu

- `index.html` — application complète (HTML/CSS/JS, sans framework). C'est une copie du
  **code réellement déployé en production** (récupéré depuis https://horticulturegaessler.fr),
  incluant la connexion et la synchronisation Supabase.

## Stockage des données

- Les étiquettes sont stockées dans Supabase (table `public.labels`), synchronisées par compte
  utilisateur (`user_id`), avec repli local sur IndexedDB en cas de coupure réseau.
- Les réglages par défaut (logos, couleurs, disposition des lignes, police…) sont stockés dans
  Supabase (table `public.app_settings`, une ligne par compte), avec repli local sur
  `localStorage` (clé `hgp_set`). Depuis le 2026-09-27, ces réglages suivent donc le compte et
  s'appliquent automatiquement à toute nouvelle étiquette, quel que soit l'appareil ou le
  navigateur utilisé — avant cette date, ils n'étaient mémorisés que dans le navigateur.

## Déploiement

- Le site est déployé manuellement sur Netlify (dépôt "drop" du fichier, pas de build/CI relié
  à ce dépôt Git). Ce dépôt sert de sauvegarde/versionnage du code source.
