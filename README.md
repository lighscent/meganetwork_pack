# Guide GitHub — Contribuer au Resource Pack

Ce guide explique comment travailler à plusieurs sur le resource pack sans modifier directement la version principale du projet.

# Pré-requis

- Avoir un compte GitHub.
- Avoir installé Git sur ton ordinateur. [Télécharger Git](https://git-scm.com/install/windows#:~:text=Git%20for%20Windows/x64%20Setup.)
- Avoir un éditeur de texte pour modifier les fichiers (ex: Visual Studio Code, Notepad++, Sublime Text, etc.).

## 1. Le principe

Nous utilisons trois notions :

- **dev** : la version officielle du resource pack. On ne la modifie jamais directement.
- **Branch (branche)** : un espace de travail personnel pour faire ses modifications.
- **Pull Request (PR)** : une demande pour ajouter ses modifications à la version officielle.

## 2. Télécharger le projet

Pour commencer, crée un dossier sur ton ordinateur pour le projet. Ensuite, ouvre un terminal dans ce dossier et exécute la commande suivante :

```bash
git clone https://github.com/lighscent/meganetwork_pack .
```

Ouvre ensuite le dossier du projet.

## 3. Créer une branche

Avant de modifier quoi que ce soit, crée une branche :

```bash
git switch dev
git pull
git switch -c feature/nom-de-ta-modification
```

Exemples :
- `feature/new-swords`
- `feature/new-textures`
- `fix/incorrect-model`

Tu peux maintenant travailler normalement sur tes fichiers.

## 4. Enregistrer ses modifications

Quand tu as terminé tes modifications, ouvre un terminal dans le dossier du projet.

```bash
git add .
git commit -m "Description des modifications"
```

Exemple :

```bash
git commit -m "Add new sword textures"
```

## 5. Envoyer ses modifications

Envoie ta branche sur GitHub :

```bash
git push -u origin feature/nom-de-ta-modification
```

## 6. Créer une Pull Request

Sur GitHub :

1. Ouvre le repository.
2. Va dans **Pull requests**.
3. Clique sur **New pull request**.
4. Choisis `dev` comme branche de destination.
5. Choisis ta branche comme branche à intégrer.
6. Clique sur **Create pull request**.

Ta modification est maintenant proposée au reste de l'équipe.

## 7. Validation

Un responsable du projet va vérifier tes modifications.

- Si tout est bon, il accepte la PR (Merge).
- Si des changements sont nécessaires, il te le signalera.

Si tu dois corriger quelque chose, modifie simplement tes fichiers puis exécute :

```bash
git add .
git commit -m "Fix requested changes"
git push
```

La Pull Request sera automatiquement mise à jour.

## 8. Les règles à respecter

- Ne jamais modifier directement `dev`.
- Toujours créer une branche avant de travailler.
- Une branche = une tâche.
- Toujours créer une Pull Request pour proposer ses modifications.
- Tester ses textures et modèles dans Minecraft avant de proposer une PR.
- Ne jamais fusionner ses modifications sans validation.

---
