# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Branches

- Toujours travailler sur la branche `develop`
- Ne jamais pusher sur `main` sans confirmation explicite de l'utilisateur
- La branche `develop` est uniquement pour les tests locaux — elle n'est jamais déployée
- Le site live est sur : https://vergers14.realt.swiss (déployé depuis `main`)

## GitHub Pages

- Source : branche `main`, dossier `/`
- La branche `develop` ne déclenche aucun déploiement automatique

## Serveur local

Pour prévisualiser le site en local sur la branche `develop` :

```bash
cd ~/Downloads/vergers14-deploy && python3 -m http.server 3000
```

Puis ouvrir : http://localhost:3000

## Workflow

1. Faire les modifications sur `develop`
2. Vérifier le rendu sur http://localhost:3000
3. ✅ OK → l'utilisateur dit "push sur main" → merger develop dans main → site live mis à jour
   ❌ Pas bon → continuer à travailler sur develop
4. Ne jamais merger sur `main` sans confirmation explicite de l'utilisateur
