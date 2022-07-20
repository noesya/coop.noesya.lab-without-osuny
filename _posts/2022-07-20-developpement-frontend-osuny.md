---
title: |
  Développement front-end Osuny
category: rd
year: 2022
sections:
    - title: Objectifs
      content: |
        Réaliser un thème Osuny léger, maintenable, documenté et intégré de façon élégante (voir qualité front double A).
        
        Actuellement on s'appuie sur la librairie bootstrap.
  
    - title: Constat
      content: |
        Actuellement entre le double et le triple A, on obtient un HTML léger, assez pur, et sémantique. En vidant le html des classes (et dividers supplémentaires) bootstrap, via l'usage d'extends et des mixins sass, le style s'en trouve moins lisible et maintenable.

        Faut-il simplifier l'usage de bootstrap au détriment de la qualité du html pour favoriser la maintenabilité et l'accès aux autres développeurs ?

    - title: Purge CSS
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
    
        

---
