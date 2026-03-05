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

```bash
cd ~/Downloads/vergers14-deploy && python3 -m http.server 3000
```

## Workflow des modifications

1. Faire les modifications sur `develop`
2. Lancer un serveur local sur http://localhost:3000 pour prévisualiser
3. Demander confirmation avant tout push
4. Attendre confirmation explicite avant de merger `develop` → `main`
5. Pour déployer sur `main`, toujours utiliser : `git show develop:docs/index.html > index.html` (ne jamais copier avec `cp` — cela ne fonctionne pas entre branches)
