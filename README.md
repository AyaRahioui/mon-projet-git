# Mon Projet Git

**Git & GitHub** : workflow complet, du premier commit à la Pull Request.

## Compétences démontrées

| Domaine | Ce que je sais faire |
|---|---|
| **Git en local** | Initialiser un dépôt, suivre l'état (`status`), utiliser la zone de staging, écrire des commits clairs, lire l'historique (`log --oneline`, `diff`) |
| **Branches** | Créer et changer de branche (`switch -c`), fusionner (`merge`), comprendre et résoudre un conflit de merge |
| **Bonnes pratiques** | Configurer son identité Git, exclure les fichiers sensibles ou inutiles avec `.gitignore` (`.env`, `node_modules/`) |
| **GitHub** | Lier un dépôt distant (`remote add origin`), publier (`push -u`), récupérer sans fusionner (`fetch`) puis fusionner (`merge`) |
| **Collaboration** | Travailler sur une branche dédiée et ouvrir une Pull Request avec un titre et une description clairs |

## Workflow suivi

```bash
git init && git add README.md && git commit -m "Initial commit"   # dépôt local
git switch -c feature-login                                      # branche de travail
git diff && git commit -am "..." && git switch main              # modifier, relire, committer
git merge feature-login                                          # intégrer
git remote add origin <url> && git push -u origin main           # publier
git fetch origin && git merge origin/main                        # synchroniser
git switch -c amelioration && git push -u origin amelioration    # puis Pull Request
```

## Points clés compris

- **Conflit de merge** : deux branches modifient la même ligne ; Git ne peut pas choisir. Je corrige le fichier entre les marqueurs `<<<<<<<` / `>>>>>>>`, puis `git add` et `git commit`.
- **Pull Request plutôt que push direct** : elle impose une relecture par l'équipe avant l'intégration dans `main`, ce qui protège la branche principale et garde la trace des décisions.
- **`fetch` avant `merge`** : je regarde les changements distants avant de les intégrer, au lieu de les subir avec un `pull` automatique.

## Liens

- Dépôt : `https://github.com/AyaRahioui/mon-projet-git`
- Pull Request : `https://github.com/AyaRahioui/mon-projet-git/pull/<numéro>`


