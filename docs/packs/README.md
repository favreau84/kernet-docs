# Packs de paramétrage

## URL stable

`diag-amiante.html` est la page à diffuser et à imprimer :

https://favreau84.github.io/kernet-docs/packs/diag-amiante.html

Son QR code encode l'URL de `diag-amiante.zip`, qui ne change jamais. Un QR
déjà imprimé importe donc toujours la dernière version du pack.

La version affichée sur la page vient de `diag-amiante.json` : la page HTML
n'a pas à être modifiée à chaque livraison.

## Livrer une nouvelle version

Depuis `docs/packs/`, avec le zip exporté depuis Krnet :

1. Archiver le zip sous son nom versionné, tiré du `packVersion` du
   `pack.json` qu'il contient : `krnet-diag-amiante-v<packVersion>.zip`.
2. Le copier sur `diag-amiante.zip`.
3. Mettre à jour `diag-amiante.json` : `packVersion`, `versionLabel`
   (format `J/M/AAAA`), `name`, `updatedAt` et `archive`.
4. Commiter sur `main` — GitHub Pages publie depuis `main` et déploie en
   moins d'une minute.

Les zips versionnés restent en place comme archive. Ne pas les supprimer :
un QR ou un lien plus ancien peut encore les viser.

## Anciennes pages

Les pages `krnet-*-v*.html` sont les pages par version, antérieures à
l'URL stable. Elles restent valides mais ne sont plus créées pour les
nouvelles versions.
