---
title: |
  Qualité Front-end : à la recherche du AAA
draft: true
category: rd
year: 2022
sections:
    - title: Abstract
      content: |
        Le World Wide Web créé par Tim Berners-Lee en 1989 au CERN<sup><a href="#note-1">1</a></sup> s'appuie sur 3 technologies : URL, HTTP et HTML. Notre proposition se concentre sur cette troisième technologie, l'HTML, qui est toujours omniprésente et qui détermine la qualité de l'expérience Web.

        En tant que développeurs Web, nous produisons de l'HTML tous les jours. Nous avons à cœur de produire le meilleure code HTML possible, ce qui implique de définir ce qu'est un excellent code HTML. Pour cela, nous introduisons dans cet article la notion de *balisage pur et parfait* qui dessine un étalon de qualité en termes d'accessibilité, de sémantique, d'empreinte écologique, de performance et de minimisation du bruit. Nous ne prétendons pas produire un balisage pur et parfait, c'est un chantier qui devra être coopératif et évolutif. En revanche nous affirmons que la notion est nécessaire pour tendre vers un idéal, qui n'est aujourd'hui pas défini, donc pas consensuel.

        Afin d'adresser de façon différenciée les projets Web en fonction de leur nature (information / action / émotion) et de leurs usages (public / privé), nous proposons un classement en trois niveaux, inspiré du jeu vidéo. Le niveau *A* fixe un standard minimum acceptable, pertinent pour les usages privés de type back-office. Le niveau *AA*, ou *double-A*, fixe un standard correct pour la plupart des productions Web. Le niveau *AAA*, ou *triple-A*, fixe le standard d'excellence absolu, le *balisage pur et parfait*.
      notes:
        - title: La naissance du Web
          url: https://home.cern/fr/science/computing/birth-web
    - title: Les enjeux de la qualité HTML
      content: |
        Opquast
        Accessibilité (RGAA)
        Eco-conception
        Sémantique (schema.org)
        SEO
        Maintenabilité
    - title: Inventaire technologique
      content: |
        Les frameworks CSS intrusifs (Bootstrap, Tailwind, Foundation...)

        Les frameworks respectueux (Ariato et PicoCSS)

        Les méthodologies BEM, SMACSS...

        Les outils de dev (Sass, Less, Stylus, Compass...)
    - title: Système de notation
      content: |
        En amont d'un projet, il est important de définir les critères de complexité :
        - La durée de vie : éphémère (événementiel) ou pérenne (structurel)
        - La quantité d'utilisateurs : cible étroite ou large
        - Les usages : e-commerce, informations, application, espace d'administration...

        ### La durée de vie

        Le site est-il déployé pour une période courte, qui n'implique pas de maintenance ni d'évolution sur le long terme ou bien est-il déployé pour une longue période, et fera l'objet d'améliorations successives ?

        Le site doit-il être repris par d'autres développeurs, par exemple dans le cadre d'un projet en source ouverte (open-source) ?

        Ces questions permettent de définir un niveau de maintenabilité minimal à appliquer, et permet de définir si l'utilisation de librairie documentée et largement partagée par la communauté de développeurs web, tel que bootstrap, facilitera la passation et la reprise du code.

        ### La largeur de la cible

        Si le projet a une cible étroite, tel qu'un outil administratif particulier ou un site dédié à un secteur de niche, le choix de la note à viser peut se faire en fonction des autres critères de complexité mais devra toujours respecter les normes WCAG. Dans le cas d'un site très largement visité, il faudra favoriser un haut niveau de qualité front.

        ### Les usages

        Si le site a beaucoup de rédactionnel, cela peut nécessité une forte modularité des composants HTML, et tend à favoriser l'usage d'un design system précis ou une librairie (bootstrap) -- **à discuter**

        L'accès au site est-il public ou privé ? Le site doit-il se positionner sur les moteurs de recherches ?

    - title: Niveau A, le minimum pratique
      content: |
        Ce niveau est facile à développer et à maintenir, tolérant sur la performance et sur le bruit. Il est très adapté pour les back-offices, par exemple.

        [Découvrir le niveau A en détail](/2022/qualite-front-a)
    - title: Niveau AA, la bonne qualité SEO
      content: |
        Ce niveau est optimisé, très performant, mais tolérant sur le bruit HTML.

        [Découvrir le niveau Double-A en détail](/2022/qualite-front-aa)
    - title: Niveau AAA, le balisage pur et parfait
      content: |
        Ce niveau ne tolère aucun compromis de qualité.

        [Découvrir le niveau Triple-A en détail](/2022/qualite-front-aaa)
---
