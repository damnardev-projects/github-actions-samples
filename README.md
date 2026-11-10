# GitHub Actions Samples

Ce projet contient plusieurs exemples de GitHub Actions pour différents cas d'utilisation.

## Structure du projet

Des commentaires sont directement présents dans les actions GitHub : voir le répertoire `.github/workflows` pour plus de détails.

## Commandes utiles

Il est possible de tester les actions localement avec [act](https://github.com/nektos/act). Avant de l'installer, assurez-vous que Docker est installé et que son service est en cours d'exécution.

Si GitHub CLI est installé, vous pouvez installer act avec la commande `gh extension install https://github.com/nektos/gh-act`, puis déclencher les workflows localement.

La première fois que vous lancez `gh act`, vous devez choisir l'image Docker à installer en fonction de vos besoins.

- `gh act --help` : affiche l'aide de act
- `gh act <EVENT_TYPE> -W <FICHIER>` : exécute le fichier de workflow `<FICHIER>` en simulant un événement `<EVENT_TYPE>`
- `gh act workflow_dispatch -W .github/workflows/workflow_dispatch.yml` : exécute le workflow `workflow_dispatch.yml` en simulant un événement `workflow_dispatch`

## GitHub

Par défaut, le projet est configuré pour lancer Dependabot à 21 h afin de vérifier les mises à jour des GitHub Actions.
