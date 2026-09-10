# TapAvis

Landing page — cartes NFC avis Google, livrées et configurées à Paris en 2h.

En ligne : https://designsprintexperts-art.github.io/tapavis/
Dépôt : https://github.com/designsprintexperts-art/tapavis

## Structure

```
tapavis/
├── index.html          page complète (CSS + JS inline, images en base64)
├── robots.txt          autorise l'indexation, pointe vers le sitemap
├── sitemap.xml         une seule URL
├── assets/
│   └── hero.mp4        vidéo de fond du hero, jouée une fois au chargement
└── design/             explorations de logo, hors site
```

`design/` ne sert pas au site et n'a pas besoin d'être téléversé.

## Mise en ligne (GitHub Pages)

Déposer `index.html`, `robots.txt`, `sitemap.xml` à la racine du dépôt, et
`hero.mp4` dans `assets/`. Pages est déjà activé sur `main` / `(root)`.

Le chemin de la vidéo est relatif : si `assets/hero.mp4` manque, le hero
retombe silencieusement sur la photo statique. Pas de page cassée, mais pas
d'animation non plus.

Après un téléversement, forcer le rechargement (Cmd+Maj+R) : le navigateur
garde l'ancienne version en cache.

## Fait

- Hero vidéo lue une fois puis fondu vers la photo (z-index corrigé, sinon
  la photo, qui porte un transform, se peignait par-dessus)
- Menu mobile, lightbox sur la photo produit, animations au scroll
- Section tarif : les deux produits nommés et numérotés
- Métadonnées SEO : title, description, canonical, robots, Open Graph,
  Twitter Card, balises geo Paris
- Contact : WhatsApp 06 35 31 50 35 · e.loui@uxdesignparis.fr
- Footer : crédit UXDP vers uxdesignparis.fr

## Reste à faire

- **FAQ + JSON-LD** (LocalBusiness, Offer, FAQPage, HowTo) — le volet
  AEO/GEO n'est pas terminé
- `assets/og-cover.jpg` (1200x630) : les balises og:image la référencent
  déjà, mais le fichier n'existe pas encore
- Sortir les images du HTML en .jpg : la page ferait ~60 Ko au lieu de 1,4 Mo
- Valider le domaine tapavis.fr, puis le brancher en domaine personnalisé
  (mettre à jour canonical, og:url, sitemap et robots au passage)
