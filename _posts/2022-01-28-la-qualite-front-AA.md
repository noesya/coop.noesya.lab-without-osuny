---
title: Qualité front AA
draft: true
category: rd
year: 2022
sections:
    
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
---
