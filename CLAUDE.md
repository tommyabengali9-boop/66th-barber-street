# 66th Barber Street — site vitrine (démo commerciale)

## Contexte business
- Salon de coiffure réel : **66th Barber Street**, 66 Av. René Coty, 76600 Le Havre, tél. 07 69 57 12 97.
- Ce site est une **démo non encore vendue** au salon. L'éditeur légal actuel (provisoire) est Tommy (tommyabengali9@gmail.com) — voir `legal.html`. Au moment de la vente, remplacer les mentions légales par les vraies infos du salon (raison sociale, SIRET).
- Le salon utilise déjà **Planity** pour la prise de rendez-vous — ce site ne gère PAS de réservation en ligne, juste vitrine + contact + lien Planity.

## Stack
- Site statique pur : HTML/CSS/JS vanilla, pas de framework, pas de build (sauf `npm install` déclaré dans `netlify.toml` pour rester cohérent avec les autres projets, mais aucune dépendance réelle actuellement).
- Déployé sur **Netlify** (site `66th-barber-street` ou équivalent — vérifier le nom exact dans le dashboard Netlify), connecté en continuous deployment depuis GitHub `tommyabengali9-boop/66th-barber-street`, branche `main`.
- Formulaire de contact via **Netlify Forms** (attribut `data-netlify="true"`, honeypot anti-spam, soumission AJAX en `fetch` + `x-www-form-urlencoded`).
- Analytics : chargeur GA conditionnel désactivé par défaut (`const GA_MEASUREMENT_ID = ""`) — à activer avec un vrai ID GA4 si le salon le souhaite, seulement après consentement (bannière cookies déjà en place).
- SEO : JSON-LD `schema.org` de type salon de coiffure dans `index.html`. **Ne pas inventer de note/avis Google** — aucune note fiable n'a été trouvée pour ce salon au moment de la création ; ne pas ajouter `aggregateRating` sans donnée vérifiée.

## Fichiers clés
- `index.html` — page principale (hero, prestations, contact, schema.org, bannière cookies).
- `legal.html` — mentions légales & confidentialité (à mettre à jour lors de la vente).
- `images/` — photos du salon.

## Ce qui reste ouvert / decisions à prendre
- Vente du site pas encore conclue — proposition commerciale et script d'appel disponibles dans le dossier parent (`proposition-66th-barber-street.docx`, `script-appel-pitch.md`).
- Nom de domaine définitif pas encore choisi.
- Pas de vraie note Google vérifiée à ce jour — revérifier si le salon en obtient une avant de l'afficher.
