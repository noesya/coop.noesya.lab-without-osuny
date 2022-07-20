---
title: |
  Développement front-end Osuny
category: rd
year: 2022
sections:
    - title: Objectifs
      content: |
        Les sites produits avec Osuny doivent répondre, autant que possible, aux critères énoncés dans l'article [Qualité frontend : à la recherche du AAA](https://lab.noesya.coop/2022/qualite-front).
        Les sites Osuny s'appuient sur un thème, qui encapsule les fonctionnalités et les bonnes pratiques d'accessibilité et d'éco-conception.

        Le thème doit être simple à maintenir pour l'équipe cœur :
        - aussi peu de dépendances que possible 
        - organisé de façon systématique
        - correctement documenté
        - peu entrelacé, pour éviter les usines à gaz / assiettes de spaghetti

        Les sites doivent être simples à développer et à maintenir pour toute la communauté :
        - facile à apprendre (bonne documentation, principes simples)
        - avec de bonnes conventions par défaut
        - avec un code et un style lisible
        - configurable simplement
        - facile à mettre à jour
    - title: Situation actuelle
      content: |
        Nous avons développé le thème en utilisant Bootstrap, afin de rendre l'adoption facile.
        Bootstrap crée un fichier trop lourd pour être utilisé tel quel. 
        Nous avons donc mis en place PurgeCSS, qui permet d'examiner le code HTML, de lister les classes nécessaires et de supprimer le CSS inutile.

        En développant les sites pour se rapprocher au maximum du triple A, nous avons enlevé le balisage Bootstrap.
        La présence de Bootstrap ne facilite pas vraiment le travail pour les développeurs tiers.

        Par ailleurs, cela a rendu PurgeCSS difficile à stabiliser, ce qui crée une situation instable en production.
        Le code que l'on écrit est souvent supprimé en prod.
        
        On se situe actuellement entre le double et le triple A, avec un code HTML léger, assez pur, et sémantique. 
        Cependant, en vidant le html des classes (et dividers supplémentaires) Bootstrap, via l'usage d'extends et des mixins sass, le style s'en trouve moins lisible donc moins maintenable.
    - title: Questions
      content: |
        Comment faire fonctionner correctement PurgeCSS ?

        Faut-il simplifier l'usage de Bootstrap au détriment de la qualité du HTML pour favoriser la maintenabilité et l'accès aux autres développeurs ?

        Faut-il utiliser Bootstrap ?
    - title: PurgeCSS ?
      content: |
        Pour simplifier la contribution par d'autres développeurs, on s'appuie sur Bootstrap. Mais pour optimiser, on allège le poid de la feuille de style avec Purge.

        Objectifs : 
        - Vider la feuille de style avec Purge (PostCSS)
        - N'avoir qu'un setup de PostCSS pour tous les sites

        Problèmes rencontrés : 
        - Un fichier spécifique par site pour géré les classes générées spécifiques
        - Actuellement purgecss se base sur les layouts hugo avant génération
        - S'appuyer sur hugo_stats.json pour purger ne fonctionne pas en l'état car nous utilisons des sélecteurs CSS s'appuyant sur les attributs html (exemple : header[role="banner"])
        - Dans le workflow de build hugo, le CSS est généré via PostCSS en même temps que le build du HTML, ça ne permet pas de s'appuyer sur le build (/public) html final pour lancer un purge.
        
        Pistes : 
        - Lancer purge via npm après le build hugo, cela fonctionne mais cela peut rallonger le temps de compilation total (en fonction de la quantité de fichiers html générés)
        - Enlever les sélecteurs de classes par attribut et utiliser hugo_stats.json pour purger.
    - title: Bootstrap ?
      content: |
        La situation actuelle n'est satisfaisante pour personne :
        - le code HTML est très beau, mais incompréhensible pour un utilisateur de Bootstrap
        - le code SASS est complexe et entrelacé, pas documenté, difficile à utiliser pour tout le monde

        Pour maintenir la qualité du code HTML, nous tentons un prototype sans Bootstrap, avec du code SASS custom.
---
