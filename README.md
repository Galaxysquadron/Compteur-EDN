# Compteur EDN

Petite app pour compter les items EDN travaillés chaque jour, avec objectif
8/jour (56/semaine) et mémoire de la semaine. Tout est stocké en local dans
le navigateur (`localStorage`) — aucune donnée n'est envoyée où que ce soit.

## Fichiers

```
index.html      → l'app entière (HTML + CSS + JS)
manifest.json   → permet l'installation en icône sur l'écran d'accueil
icons/          → icônes de l'app (192, 512, apple-touch, favicon)
```

## Mettre en ligne sur GitHub Pages

1. Crée un repo (ex. `edn-counter`) et mets ces fichiers à la racine
   (ou dans un dossier `docs/`, au choix).
2. Sur GitHub : **Settings → Pages → Source**, sélectionne la branche
   (`main`) et le dossier (`/root` ou `/docs`), puis Save.
3. Ton app sera disponible à `https://<ton-pseudo>.github.io/edn-counter/`
   après une à deux minutes.

## Ajouter l'icône sur l'écran d'accueil du téléphone

**iPhone (Safari) :** ouvre le lien → bouton Partager (le carré avec la
flèche) → *Sur l'écran d'accueil*.

**Android (Chrome) :** ouvre le lien → menu ⋮ → *Ajouter à l'écran
d'accueil* (ou *Installer l'application*, selon la version).

L'icône (fond bleu nuit, anneau rouge→vert, coche blanche) et le nom
« EDN » apparaîtront automatiquement grâce à `manifest.json`.

## Fonctionnement

- **Le gros bouton rond = le compteur.** Un tap = +1 item aujourd'hui.
  Il passe du rouge (0) au vert (8), en dégradé, comme un moniteur.
- **−1** corrige un tap accidentel.
- **Réinitialiser** repasse le compteur du jour à 0 (avec confirmation).
- La ligne du bas montre les 7 jours de la semaine (L→D), le total, et
  une barre de progression vers l'objectif de 56.
- Les données sont conservées par date : tu peux fermer l'app, changer de
  jour, la mémoire de la semaine reste correcte.

## Remarque technique

Pour que l'installation sur l'écran d'accueil fonctionne bien (surtout
sur iPhone), sers le site en HTTPS via GitHub Pages plutôt que d'ouvrir
`index.html` directement en local (`file://`).
