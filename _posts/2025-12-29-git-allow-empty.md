---
title: "Git : Pourquoi et comment utiliser --allow-empty"
date: 2025-12-29 12:00:00 +0100
categories: [Git]
tags: [git, tips]
---

La commande `git commit --allow-empty` permet de créer un commit dans votre historique Git sans avoir à modifier aucun fichier du dépôt.

```bash
git commit --allow-empty -m "Chore: trigger ci/cd pipeline"
```

Il vous est sûrement déjà arrivé de modifier un fichier avec un simple saut de ligne ou un espace pour pouvoir pousser un commit. Cette manipulation est souvent justifiée par le besoin de déclencher une automatisation telle qu'un workflow de CI/CD, notamment pour les tester lors de leur mise en place.

L'option --allow-empty permet de faire l'équivalent sans nécessiter de modifications de code inutiles.

Son utilisation est plutôt réservée un besoin ponctuel. Elle se fait le plus souvent sur une branche n'ayant pas vocation à être fusionnée avec la branche principale du dépôt, ou bien après avoir `squash` les commits pour éviter de surcharger l'historique.

Certains l'utilisent parfois pour marquer une étape dans l'historique de leurs commits. Il existe toutefois pour cela une autre commande git plus adaptée : le tag.
