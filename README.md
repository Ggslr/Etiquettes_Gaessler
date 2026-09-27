# Etiquettes_Gaessler

Application web de création d'étiquettes produits pour Horticulture GAESSLER.

## Contenu

- `index.html` — application complète (HTML/CSS/JS, sans framework), version locale de référence.

## Notes

- Cette version locale utilise IndexedDB pour le stockage des étiquettes et `localStorage`
  (clé `hgp_set`) pour mémoriser les réglages par défaut (logos, couleurs, disposition des lignes).
- La version en ligne (https://horticulturegaessler.fr) reprend la même logique de réglages
  par défaut, avec en plus une synchronisation des données via Supabase (connexion utilisateur,
  stockage des étiquettes en base au lieu d'IndexedDB).
- Ce dépôt sert de sauvegarde/versionnage du code source ; il n'est pas branché en déploiement
  automatique sur Netlify (le site en ligne est actuellement déployé manuellement).
