---
title: "Git : Pourquoi et comment utiliser allow-empty"
date: 2025-12-29 12:00:00 +0100
categories: [Git]
tags: [git, tips]
---

La commande `git commit --allow-empty` permet de créer un commit dans votre historique Git sans avoir à modifier aucun fichier du dépôt.

```bash
git commit --allow-empty -m "Chore: trigger ci/cd pipeline"
```

Il vous est sûrement déjà arrivé de modifier un fichier avec un simple saut de ligne ou un espace pour pouvoir pousser un commit. La raison pour ça est souvent de déclencher une automatisation tel qu'un pipeline de CI/CD.

L'option --allow-empty permet de faire l'équivalent de manière plus élégante et sans avoir à revenir en arrière avec un autre commit.

C'est une pratique plutôt réservée à une utilisation ponctuelle dans une branche n'ayant pas vocation à être fusionnée avec la branche principale du dépôt ou bien après un `squash` des commits pour éviter de rendre l'historique illisible.

Certains l'utilisent parfois pour marquer une étape dans l'historique de leurs commits. Il existe toutefois pour cela une autre commande git : le tag.
