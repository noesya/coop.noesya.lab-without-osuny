---
title: Recherches et réflexions sur la qualité front
draft: true
category: rd
year: 2022
sections:
    - title: Questionnement
      content: |
        Qu’est-ce que la qualité front ? Comment définir des règles et critères qui permettent d'évaluer cette qualité ? Comment faire au mieux en fonction du contexte ?

        Avec une notation en 3 niveaux de qualité *A*, *AA*, ou *AAA*, nous essayons de proposer un ensemble une liste de règles et de bonnes pratiques à appliquer pour répondre au mieux aux besoins d’un projet.

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
    
    - title: A (qualité minimale)
      content: |
        ### Description

        Bootstrap avec plein de balises de style
        Libs JS autorisées
        WCAG minimal

        ### Exemple de contextes

        - Bootstrap avec plein de balises de style
        - Pour les back-offices, thème Bootstrap d’admin

        ### Avantages

        rapide, évolutif, stable

        ### Inconvénients

        HTML laid et pas sémantique, CSS lourd, JS lourd

        ### Exemple d'un header

        ```html
          <nav id="sidebar" class="sidebar">
            <div class="sidebar-content js-simplebar" data-simplebar="init">
              <div class="simplebar-wrapper">
                <div class="simplebar-mask">
                  <div class="simplebar-offset">
                    <div class="simplebar-content-wrapper">
                      <div class="simplebar-content">
                        <a class="sidebar-brand" href="/admin">
                          <img class="img-fluid" src="/assets/osuny-white-5c5a29719b513fa909919512ab06b5fc8f65ce09f1c9b232b49e58f453f49582.svg">
                        </a>
                        <ul class="sidebar-nav">
                          <li class="sidebar-item  ">
                            <a href="/admin" class="sidebar-link collapsed">
                              <i class="fas fa-tachometer-alt"></i>
                              <span class="align-middle">Dashboard</span>
                            </a>
                          </li>
                          ...
                        </ul>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </nav>
        ``` 

    - title: AA (qualité intermédiaire)
      content: |
        ### Description

        Utilisation limitée de Bootstrap :
        - pas d’utilities (”my-3”, “pb-1”...)
        - utiliser les mixins sass de bootstrap (attention aux classes utilisées par le js de bootstrap)
        - limiter les classes, par exemple, favoriser les “row-columns” au lieux des “cols” permet de n’écrire qu’une fois la règle de colonage lorsque que ces dernières sont de même largeurs

        [Schema.org](http://schema.org/) et balises signifiantes

        Purge CSS pour alléger

        Caractéristiques : 

        ### Exemple de contextes

        - Bootstrap avec plein de balises de style
        - Pour les back-offices, thème Bootstrap d’admin

        ### Avantages

        rapide, stable, SEO

        ### Inconvénients

        ...

        ### Exemple d'un menu avec bootstrap

        ```html
          <nav class="navbar navbar-expand-lg" id="navigation" aria-label="Menu principal">
            <div class="container">
              <a class="navbar-brand" href="https://bordeauxmontaigne-iut.netlify.app/">
                <img src="/assets/images/logo.svg" alt="IUT Bordeaux Montaigne" height="42" width="147">
              </a>
              <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="">
                <span class="navbar-toggler-text">Menu</span>
                <span class="navbar-toggler-icon"></span>
              </button>
              <div class="collapse navbar-collapse" id="navbarNavDropdown">
                <ul class="navbar-nav nav-level-1">
                  <li class="nav-item">
                    <a href="/actualites/" class="nav-link">Actualités</a>
                  </li>
                  <li class="nav-item has-children dropdown">
                    <a href="/notre-institut/" class="nav-link dropdown-toggle" id="dropdown-notre-institut" role="button" data-bs-toggle="dropdown" aria-expanded="false">Notre institut</a>
                    <div class="dropdown-menu" aria-labelledby="dropdown-notre-institut">
                      <ul class="nav-level-2">
                        <li class="nav-item">
                          <a href="/notre-institut/presentation-de-liut/" class="nav-link">Présentation de l'IUT</a>
                        </li>
                        <li class="nav-item">
                          <a href="/notre-institut/relations-avec-les-entreprises/" class="nav-link">Relations avec les entreprises</a>
                        </li>

                        [...]

                      </ul>
                    </div>
                  </li>
                  <li class="nav-item has-children dropdown">
                    <a href="/offre-de-formation/" class="nav-link dropdown-toggle" id="dropdown-offre-de-formation" role="button" data-bs-toggle="dropdown" aria-expanded="false">Offre de formation</a>
                    <div class="dropdown-menu" aria-labelledby="dropdown-offre-de-formation">
                      <ul class="nav-level-2">
                        <li class="nav-item">
                          <a href="/offre-de-formation/" class="nav-link">Toute l'offre de formation</a>
                        </li>
                        <li class="nav-item has-children"><a href="/offre-de-formation/bachelor-universitaire-de-technologie/" class="nav-link">Bachelor Universitaire de Technologie</a>
                          <ul class="nav-level-3">
                            <li class="nav-item">
                              <a href="/offre-de-formation/bachelor-universitaire-de-technologie/carrieres-sociales/parcours-animation-sociale-et-socioculturelle/" class="nav-link">Animation sociale et socioculturelle</a>
                            </li>

                            [...]

                          </ul>
                        </li>

                        [...]

                        <li class="nav-item">
                          <a href="/formation-continue/" class="nav-link">Formation continue</a>
                        </li>
                      </ul>
                    </div>
                  </li>
                </ul>
              </div>
            </div>
          </nav>
        ``` 

    - title: AAA (qualité supérieure)
      content: |
        ### Description

        Balisage purement sémantique avec utilisation de [schema.org](http://schema.org/) et aria.

        ### Outils :

        - Pas de Bootstrap.
        - Pas de purge parce qu’il n’y a rien à purger.

        ### HTML :

        - Balisage sémantique
        - Utilisation des schemas (schema.org, itemtype et itemprop)
        - Utilisation des propriétés ARIA ([https://www.w3.org/TR/html-aria/](https://www.w3.org/TR/html-aria/))

        ### Classes CSS :

        - Utiliser en priorité les balises pures, sans classe.
        - S’appuyer sur l’arbre HTML pour les sélecteurs CSS : définir une limite de niveaux pour garder une bonne lisibilité / maintenabilité.
        - Limiter l’usage des classes aux cas où elles apportent du sens, sans pour autant diminuer la compréhension et la maintenabilité.
        - Aucune classe de présentation dans le DOM (row, col, large, mb-5...).
        - Utiliser des body classes indiquant la nature des pages pour du contexte.
        - Quand les balises pures et les body classes ne suffisent pas, ajouter des classes qui indiquent la nature des objets traités (post, person, author, product...)

        ### Exemple d'un menu

        ```html
          <header>
            <a href="/">
              <img  src="https://assets.noesya.coop/images/logos/logo-noesya.svg"
                    alt="noesya" width="100" height="26">
            </a>
            <button aria-label="Ouvrir / Fermer le menu">
              <!-- SVG / IMG / ::after ::before / ... -->
            </button>
            <nav aria-label="Navigation principale">
              <ul>
                <li>
                  <a href="/communs-numeriques">Communs numériques</a>
                </li>
                [...]
              </ul>
            </nav>
          </header>
        ``` 




---
