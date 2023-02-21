---
title: |
  Un bon thème d'admin  
category: rd
year: 2023
sections:
    - content: |
        ## Contexte
        Dans la plupart des applications Web que nous développons, nous avons besoin d'un espace d'administration.
        Cet espace est traditionnellement moins soigné ergonomiquement et graphiquement que le front-office, puisqu'il est utilisé par beaucoup moins de personnes.
        Un thème pour ces espaces d'administration permet de réutiliser des composants graphiques et techniques, et donc de gagner du temps et de la qualité.
        Mais quel thème utiliser ?

        ## Critères

        ### Libre
        Le thème doit utiliser une licence libre, et si possible ne pas être une version gratuite d'un produit commercial.
        
        ### Pérenne
        Le thème doit s'appuyer sur Bootstrap 5, avec une communauté, et des mises à jour régulières.
        
        ### Léger
        Pages légères, peu de composants et de dépendances, ou alors modulables.

        ### Esthétique
        Espaces et typographies bien traitées, pas trop d'effet de mode.

        ## Possibilités
        Benchmark du 20 février 2023
        
        ### CoreUI
        [Github](https://github.com/coreui/coreui-free-bootstrap-admin-template) / 
        [Demo](https://coreui.io/demos/bootstrap/4.2/free/) /
        [Diagnostic 2,15 Mo](https://diagnostic.noesya.coop/b0910c95-d3ac-4af6-bb47-e66e241204ba)<br>
        11500 stars, dernier commit janvier 2023<br>
        Version gratuite d'un produit payant (CoreUI Pro)<br>
        Proche de Bootstrap, un peu brut de fonderie visuellement
        
        ### Material Dashboard 2
        [Github](https://github.com/creativetimofficial/material-dashboard) /
        [Demo](https://demos.creative-tim.com/material-dashboard/examples/dashboard.html) /
        [Diagnostic 1,02 Mo](https://diagnostic.noesya.coop/26d01120-473d-4c5f-b15b-20d2250966cc)<br>
        10400 stars, dernier commit octobre 2022<br>
        Version gratuite d'un produit payant<br>
        Rendu visuel très marqué, plutôt lourd (les couleurs comptent plus que les textes)
        
        ### Adminator
        [Github](https://github.com/puikinsh/Adminator-admin-dashboard) / 
        [Demo](https://colorlib.com/polygon/adminator/index.html) /
        [Diagnostic 947 ko](https://diagnostic.noesya.coop/dcbf4488-1e7d-4f21-8f73-178f5fc599a1)<br>
        4100 stars, dernier commit septembre 2021<br>
        Plutôt simple et clair, très blanc
        
        ### Volt
        [Github](https://github.com/themesberg/volt-bootstrap-5-dashboard) / 
        [Demo](https://demo.themesberg.com/volt/pages/dashboard/dashboard.html) /
        [Diagnostic 1,05 Mo](https://diagnostic.noesya.coop/cb3134f8-c80a-41c2-aab2-dedba5f1a137)<br>
        2500 stars, dernier commit janvier 2023<br>
        Version gratuite d'un produit payant<br>
        Pas mal, un peu lourd typographiquement et manque d'air
        
        ### Mazer
        [Github](https://github.com/zuramai/mazer) / 
        [Demo](https://zuramai.github.io/mazer/demo/) /
        [Diagnostic 5,76 Mo](https://diagnostic.noesya.coop/904a3921-ac19-481b-a664-b158d04ceba6)<br>
        1800 stars, dernier commit janvier 2023<br>
        Chouette mais un peu enfantin, avec dark mode
        
        ### AdminKit
        [Github](https://github.com/adminkit/adminkit) / 
        [Demo](https://demo.adminkit.io) /
        [Diagnostic 2,22 Mo](https://diagnostic.noesya.coop/5b90fc5b-3307-408c-875f-c3c317613458)<br>
        1100 stars, dernier commit août 2022<br>
        Plutôt calé, beaucoup de micro-animations
        
        ### Sneat
        [Github](https://github.com/themeselection/sneat-html-admin-template-free) / 
        [Demo](https://demos.themeselection.com/sneat-bootstrap-html-admin-template-free/html/) /
        [Diagnostic 1,31 Mo](https://diagnostic.noesya.coop/1eaba547-e6dc-42da-b807-436528cbb7a7)<br>
        505 stars, dernier commit février 2023 mais projet très récent<br>
        Version gratuite d'un thème pro.<br>
        Très joli
        
        ### Voler
        [Github](https://github.com/zuramai/voler)  / 
        [Demo](https://zuramai.github.io/voler/) /
        [Diagnostic 296 ko](https://diagnostic.noesya.coop/1eaba547-e6dc-42da-b807-436528cbb7a7)<br>
        457 stars, dernier commit août 2022<br>
        Animations bizarres, cadres dans les cadres, calages très approximatifs
        
        ### PlainAdmin
        [Github](https://github.com/PlainAdmin/plain-free-bootstrap-admin-template)  / 
        [Demo](https://demo.plainadmin.com/) /
        [Diagnostic 675 ko](https://diagnostic.noesya.coop/8b99e49d-ce16-4422-a5a7-bb685c96aece)<br>
        256 stars, dernier commit février 2023 mais projet très récent<br>
        Version gratuite d'un thème pro.<br>
        Transition très laide du menu, typos lisibles et assez grandes
        
        ### ArchitectUI
        [Github](https://github.com/DashboardPack/architectui-html-theme-free)  / 
        [Demo](https://demo.dashboardpack.com/architectui-html-free/) /
        [Diagnostic 538 ko](https://diagnostic.noesya.coop/7ab34dbf-45aa-4f16-b9fc-42c30ba5d66b)<br>
        250 stars, dernier commit août 2022<br>
        Version gratuite d'un thème pro.<br>
        Trop amateur

        ## Analyse

        ### Libre

        Les thèmes qui sont de purs projets libres sont :
        - Adminator
        - Mazer
        - Voler

        Les thèmes suivants sont des versions gratuites de thèmes payants :
        - AdminKit
        - CoreUI
        - Material Dashboard 2
        - Volt
        - Sneat
        - PlainAdmin
        - ArchitectUI

        ### Robuste

        Rassurant :
        - CoreUI
        - Material Dashboard 2
        - Volt
        - Mazer

        Pas sûr :
        - AdminKit (août 2022)
        - Sneat (petit projet très récent, 14 commits)
        - Voler (petit projet, août 2022)
        - PlainAdmin (petit projet très récent, 36 commits)

        Pas du tout :
        - Adminator (septembre 2021)
        - ArchitectUI (petit projet à l'abandon)

        ### Léger

        Idéal :
        - Voler (296 ko)
        - ArchitectUI (538 ko)
        - PlainAdmin (675 ko)
        - Adminator (947 ko)

        Lourd :
        - Material Dashboard 2 (1,02 Mo)
        - Volt (1,05 Mo)
        - Sneat (1,31 Mo)
        - CoreUI (2,15 Mo)
        - AdminKit (2,22 Mo)

        Exclu parce que beaucoup trop lourd :
        - Mazer (5,76 Mo)

        ### Esthétique

        Chouette :
        - Sneat
        - AdminKit
        - Adminator

        Bof :
        - Mazer
        - Volt
        - CoreUI
        - Material Dashboard 2
        
        Pas dingue :
        - Voler
        - PlainAdmin
        - ArchitectUI

        ## Sélection

        ### Disqualifiés

        - Mazer, beaucoup trop lourd
        - ArchitectUI, abandonné et manque de qualité
        - PlainAdmin, pas très beau
        - Voler, pas très beau
        - Adminator, abandonné

        ### Qualifiés

        - CoreUI
        - Material Dashboard 2
        - Volt
        - AdminKit
        - Sneat


---