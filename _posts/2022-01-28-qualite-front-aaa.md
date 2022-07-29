---
title: Qualité front AAA
draft: true
category: rd
year: 2022
sections:
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
          <header role="banner">
            <a href="/">
              <img  src="https://assets.noesya.coop/images/logos/logo-noesya.svg"
                    alt="noesya" width="100" height="26">
            </a>
            <button aria-label="Ouvrir / Fermer le menu">
              <!-- SVG / IMG / ::after ::before / ... -->
            </button>
            <nav role="navigation" aria-label="Navigation principale">
              <ul>
                <li>
                  <a href="/communs-numeriques">Communs numériques</a>
                </li>
                [...]
              </ul>
            </nav>
          </header>
        ```


    - title: Faire des sélecteurs via des classes CSS ou des attributs HTML ?
      content: |
        ### Breadcrumb

        La question se pose pour le cas du breadcrumb : 

        ```
        - .breadcrumb
        + ol[itemtype="https://schema.org/BreadcrumbList"]
        ```

        https://github.com/noesya/osuny-hugo-theme-AAA/pull/21

        L'argument de ne pas utiliser un sélecteur contenant une url (https://schema.org) ne tient pas, car selon le web de Tim Berners-Lee, une page web est un contrat dont l'URI ne doit pas changer.


---
