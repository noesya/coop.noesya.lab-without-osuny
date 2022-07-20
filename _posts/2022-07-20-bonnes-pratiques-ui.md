---
title: "Interface Utilisateur (UI) : bonnes pratiques"
category: rd
year: 2022
sections:
    - content: |
        Cet article synthétise les bonnes pratiques d'interface appliquées dans les différents thèmes <a href="https://www.osuny.org" target="_blank">Osuny</a>, 
        notamment le site de l'<a href="https://www.iut.u-bordeaux-montaigne.fr" target="_blank">IUT Bordeaux Montaigne</a>,
        le site <a href="https://www.osuny.org" target="_blank">Osuny</a>
        et le site <a href="https://www.communication-democratie.org" target="_blank">Communication & démocratie</a>.

        ## Menu 

        En mobile comme en desktop, le menu se masque au scroll, et réapparaît quand on scroll vers le haut.
        De cette façon, on ne gaspille pas l'espace vertical comme avec un menu fixe, 
        et on évite de devoir scroller en haut de page pour retrouver le menu comme avec le menu en haut.

        ### Desktop
        Le menu classique présente le logo à gauche et la navigation à droite, ou le logo en haut et le menu dessous.

        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/iut-menu-desktop.png" class="thumb" loading="lazy">
        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/code-menu-desktop.png" class="thumb" loading="lazy">
        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/osuny-menu-desktop.png" class="thumb" loading="lazy">

        Le menu desktop fermé permet d'afficher des sous-niveaux, avec une ouverture pleine largeur.
        Le niveau 2 est colonné, sur 3 ou 4 colonnes.
        Le niveau 3 s'affiche dans chaque colonne.
        En l'absence de niveau 3, le menu peut afficher la description de la page de niveau 2.

        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/iut-menu-desktop-open.png" class="thumb" loading="lazy">
        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/code-menu-desktop-open.png" class="thumb" loading="lazy">
        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/osuny-menu-desktop-open.png" class="thumb" loading="lazy">
        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/osuny-menu-desktop-open-2.png" class="thumb" loading="lazy">

        ### Mobile
        Le menu mentionne, à l'idéal, le terme menu en texte. 
        Une icône peut être utilisée en complément, ou seule, même si ce dernier cas n'est pas idéal (toutes les personnes ne connaissent pas forcément la signification de 3 traits superposés).

        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/iut-menu-mobile.png" class="thumb thumb--mobile" loading="lazy">
        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/code-menu-mobile.png" class="thumb thumb--mobile" loading="lazy">
        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/osuny-menu-mobile.png" class="thumb thumb--mobile" loading="lazy">

        Le menu ouvert affiche le niveau 2, avec des icônes indiquant l'ouverture possible.
        Presser le nom ou l'icône permet d'ouvrir le niveau 2, qui affiche les niveaux 2 et 3.

        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/iut-menu-mobile-open.png" class="thumb thumb--mobile" loading="lazy">
        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/code-menu-mobile-open.png" class="thumb thumb--mobile" loading="lazy">
        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/osuny-menu-mobile-open.png" class="thumb thumb--mobile" loading="lazy">

        ## Breadcrumb
        Les rubriques cliquables et la rubrique non cliquable sont très peu distinctes de façon à maintenir un bon rapport de contraste.
        Elles se distinguent par la présence ou l'absence de soulignement.

        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/iut-breadcrumb-desktop.png" class="thumb" loading="lazy">
        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/code-breadcrumb-desktop.png" class="thumb" loading="lazy">
        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/osuny-breadcrumb-desktop.png" class="thumb" loading="lazy">

        En mobile, le breadcrumb dépasse de la page, scrollable horizontalement.

        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/iut-breadcrumb-mobile.png" class="thumb thumb--mobile" loading="lazy">
        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/code-breadcrumb-mobile.png" class="thumb thumb--mobile" loading="lazy">
        <img class="img-fluid" src="/assets/images/posts/2022-07-20-bonnes-pratiques-ui/osuny-breadcrumb-mobile.png" class="thumb thumb--mobile" loading="lazy">

---
