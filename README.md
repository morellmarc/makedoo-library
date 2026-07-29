# Makedoo Library

Bibliothèque de packs de sessions pour l'application [Makedoo](https://morellmarc.github.io/makedoo-v3).

## Structure

```
makedoo-library/
├── manifest.json          ← catalogue principal (lu par l'app)
├── gratuit/                ← packs accessibles à tous
├── abonnes/                 ← packs réservés aux utilisateurs abonnés
└── professionnel/            ← packs vendus séparément
```

## Ajouter un pack

1. Créer un dossier dans la bonne catégorie : `gratuit/`, `abonnes/`, ou `professionnel/`
2. Y déposer les fichiers `.json` exportés depuis Makedoo (bouton 📤 JSON)
3. Ajouter une entrée dans `manifest.json` avec la liste des fichiers de session
4. Committer et pousser — l'app lira automatiquement le nouveau contenu

## Format d'un pack dans manifest.json

```json
{
  "id": "identifiant-unique",
  "tier": "gratuit | abonnes | professionnel",
  "name": "Nom affiché",
  "description": "Description courte",
  "langPair": "fr-mk",
  "price": "9.90",        // uniquement pour tier=professionnel
  "path": "categorie/dossier-du-pack",
  "sessions": ["01-fichier.json", "02-fichier.json"]
}
```
