---
title: |
  Qualité frontend : à la recherche du AAA
draft: true
category: rd
year: 2022
sections:
    - title: Abstract
      content: |
        Le World Wide Web créé par Tim Berners-Lee en 1989 au CERN<sup><a href="#note-1">1</a></sup> s'appuie sur 3 technologies : URL, HTTP et HTML. Notre proposition se concentre sur cette troisième technologie, l'HTML, qui est toujours omniprésente et qui détermine la qualité de l'expérience Web.

        En tant que développeurs et développeuses Web, nous produisons de l'HTML tous les jours. Nous avons à cœur de produire le meilleur code HTML possible, ce qui implique de définir ce qu'est un excellent code HTML. Pour cela, nous introduisons dans cet article la notion de *balisage pur et parfait* qui dessine un étalon de qualité en termes d'accessibilité, de sémantique, d'empreinte écologique, de performance et de minimisation du bruit. Nous ne prétendons pas produire un balisage pur et parfait, c'est un chantier qui devra être coopératif et évolutif. En revanche nous affirmons que la notion est nécessaire pour tendre vers un idéal, qui n'est aujourd'hui pas défini, donc pas consensuel.

        Afin d'adresser de façon différenciée les projets Web en fonction de leur nature (information / action / émotion) et de leurs usages (public / privé), nous proposons un classement en trois niveaux. Le niveau *A* fixe un standard minimum acceptable, pertinent pour les usages privés de type back-office. Le niveau *AA*, ou *double-A*, fixe un standard correct pour la plupart des productions Web. Le niveau *AAA*, ou *triple-A*, fixe le standard d'excellence absolu, le *balisage pur et parfait*.
      notes:
        - title: La naissance du Web
          url: https://home.cern/fr/science/computing/birth-web
    - title: 7 enjeux de qualité frontend
      content: |
        Le premier enjeu, évident, est le respect du standard HTML, tel que défini par le World Wide Web Consortium<sup><a href="#note-2">2</a></sup>. Depuis 2019, c'est un format unique, qui dispose d'une documentation à l'intention des devs<sup><a href="#note-3">3</a></sup>, ainsi que d'un service de validation permettant de tester son balisage<sup><a href="#note-4">4</a></sup>.

        Le second enjeu est celui de l'accessibilité, c'est à dire de la minimisation de l'exclusion. Un service numérique accessible est perceptible, utilisable, compréhensible et robuste, d'après le Référentiel Général d'Amélioration de l'Accessibilité<sup><a href="#note-5">5</a></sup>. Le référentiel définit des critères mesurables et des niveaux de conformité, qui présentent un caractère contraignant pour les services publics.

        En troisième lieu, la maîtrise de la qualité Web passe par le respect des 240 règles Opquast<sup><a href="#note-6">6</a></sup>. Cet ensemble de bonnes pratiques en Creative Commons est élaboré depuis 2000 par des centaines de professionnelles et professionnels du Web. Chaque règle est *universelle, utile, documentée, sans valeur numérique, fait consensus et n’est pas liée à un pays ou une loi spécifique*.

        Un balisage HTML de grande qualité définit de manière sémantique le contenu des pages. Cette qualification des objets par leur nature permet de nourrir le Web sémantique et de se rapprocher du Graph Global Géant<sup><a href="#note-7">7</a></sup> inventé par Tim Berners Lee en 2007. Si le WWW partage des pages, le GGG partage des connaissances, compréhensibles par des humains comme par des algorithmes. Le projet Schema.org liste les vocabulaires consensuels pour définir un grand nombre d'objets du monde réel, et les relations entre ces objets. Ces vocabulaires thématiques se nomment *ontologies*.

        Un balisage respectueux du standard HTML et sémantique est parfait pour les moteurs de recherche. Cela remplit la part technique de l'optimisation pour les moteurs de recherche (Search Engine Optimization, SEO). En pratique, des balises parasites propriétaires sont souvent ajoutées afin d'améliorer les partages sur les réseaux sociaux, notamment Facebook et Twitter. Dans un monde parfaitement interopérable, ces balises ne devraient pas exister, et les réseaux sociaux devraient utiliser les informations neutres et standardisées à leur disposition. Le compromis entre le balisage idéal et le balisage pragmatique devra faire l'objet d'un consensus, réévalué en fonction des évolutions des acteurs.

        Un frontend de grande qualité doit être aussi sobre que possible. Le Référentiel Général d'Écoconception de Services Numériques<sup><a href="#note-8">8</a></sup> propose un jeu de critères de haut niveau applicables au frontend. À un niveau plus bas, la mise en œuvre de l'écoconception est facilitée par un ensemble d'indicateurs nommés *Web Vitals* par Google<sup><a href="#note-9">9</a></sup>. Ces métriques lient sobriété et performance, et sont assorties d'exemples de bonnes pratiques et d'études de cas.

        Ces 6 critères constituent la qualité *parfaite* du balisage. Nous y ajoutons la nécessité de minimiser le bruit, qui constitue la qualité *pure*. Le rapport signal/bruit<sup><a href="#note-9">9</a></sup> est un indicateur de la qualité de transmission d'une information, mesuré habituellement en décibels. Curieusement, cet indicateur largement consensuel dans de nombreux domaines ne semble pas influencer le développement frontend. Ce balisage pur et parfait présente une analogie avec le son haute-fidélité, c'est une sorte d'HTML Hi-Fi dans lequel il y a toute l'information et rien de plus.

        Ces 7 critères définissent le *quoi*, le résultat que nous souhaitons atteindre. Mais les devs sont (malheureusement) souvent plus intéressés par le *comment*, les outils, les méthodes et les gadgets utilisables pour atteindre ce résultat. Plusieurs enjeux s'entrecroisent. D'abord, la rapidité de production : comment produire vite et faire évoluer rapidement. Ensuite, la maintenabilité : comment éviter de se retrouver avec une assiette de spaghetti impossible à démêler, ce qui a un impact sur la rapidité mais aussi sur la stabilité. Plus le code est compliqué, plus il présente d'effets de bord indésirables. Enfin, la courbe d'apprentissage : les méthodes utilisées sont-elles longues à apprendre ? Et dans tous les cas, si on en change, il faut réapprendre.

        Quels outils avons-nous à notre disposition, en 2022 ? Faisons l'inventaire...
      notes:
        - title: W3C
          url: https://www.w3.org
        - title: "HTML: The Living Standard"
          url: https://html.spec.whatwg.org/dev/
        - title: Markup Validation Service
          url: https://validator.w3.org
        - title: RGAA
          url: https://www.numerique.gouv.fr/publications/rgaa-accessibilite/
        - title: Qualité Web
          url: https://checklists.opquast.com/fr/assurance-qualite-web/
        - title: GGG
          url: https://fr.wikipedia.org/wiki/Graphe_Global_G%C3%A9ant
        - title: schema.org
          url: https://schema.org
        - title: RGESN
          url: https://ecoresponsable.numerique.gouv.fr/publications/referentiel-general-ecoconception/
        - title: Web Vitals
          url: https://web.dev/learn-web-vitals/
        - title: Rapport signal sur bruit
          url: https://fr.wikipedia.org/wiki/Rapport_signal_sur_bruit
    - title: Inventaire technologique
      content: |
        Rappelons quelques concepts de base pour les lecteurs et lectrices qui ne coderaient pas, ou pas du Web. Le cœur du Web est l'HTML, qui permet de structurer les informations. L'apparence de ces informations (les typographies, les couleurs, la mise en page) est définie par les feuilles de style en cascade, le CSS. Une partie de l'interactivité est directement intégrée à l'HTML, par exemple les boutons, les formulaires ou les liens hypertexte. Les comportements plus sophistiqués sont développés en JavaScript. En synthèse, nous avons donc 3 composants : l'HTML (le sens et l'interactivité basique), le CSS (l'apparence, la forme) et le JS (l'interactivité avancée).

        La base low-tech consiste à écrire du code HTML, CSS et JS dans un éditeur de texte. Comme les pages HTML présentent de nombreux éléments répétitifs, plusieurs outils permettent de réutiliser du code d'une page sur l'autre. En termes techniques, si l'on se situe dans le cadre d'une application Web,  on codera souvent les vues du pattern Modèle Vue Controlleur (MVC), en utilisant des mécanismes de template et d'inclusion de fragments de code. Si l'on se situe dans un projet sans base de données ni technologie backend, on utilisera souvent un générateur de site statique qui propose les mêmes mécanismes. Ces infrastructures n'ont pas d'impact sur la qualité frontend (les 6 premiers enjeux), et elles permettent aux devs d'organiser leur code et de ne pas se répéter (le 7e enjeu). Nous ne détaillerons pas plus ces questions, mais nous invitons les devs à rester DRY<sup><a href="#note-10">10</a></sup>, et à utiliser pour cela les outils qui conviennent le mieux au projet et à l'équipe.

        Le CSS a une syntaxe verbeuse, avec des parenthèses, des accolades, des règles de fermeture strictes et un seul niveau de déclaration. Pour pallier ces défauts, plusieurs technologies se sont développées, par exemple Sass, Less ou Stylus. On les appelle des préprocesseurs, c'est à dire des outils qui traitent un langage spécifique pour générer du CSS. Là encore, nous laissons aux devs le choix des armes, avec toutefois un point de vigilance : ces outils peuvent causer une augmentation involontaire du poids du CSS et une diminution de son efficacité. Il convient donc de les employer en surveillant la traduction CSS, et avec une bonne culture du mode d'application du CSS sur le document HTML (le Document Object Model, DOM).

        Une autre école de pensée est partie de l'idée que l'on pouvait standardiser les interfaces et s'appuyer sur des classes HTML pour définir l'apparence. Ces frameworks CSS, dont le plus répandu est Bootstrap, favorisent la rapidité du développement, puisqu'on définit l'apparence  sans écrire de CSS. On gagne également du temps de formation, puisque le framework est réutilisé d'un projet à l'autre. Toutefois, ce gain se fait au prix de deux sacrifices importants. Premièrement, le balisage HTML est pollué, parfois au point que l'on cherche le contenu dans une forêt de balises définissant l'apparence. Deuxièmement, les frameworks sont lourds, puisqu'ils intègrent un grand nombre de possibilités. Afin de résoudre ce problème, certains frameworks, comme Tailwind, proposent des solutions techniques pour limiter le poids aux éléments réellement utilisés. Cela revient à choisir les outils à intégrer en fonction des besoins. L'outil PurgeCSS a été développé pour purger le CSS de toutes les directives non utilisées dans l'HTML. Cela revient à remplir un atelier de tous les outils possibles, puis à le vider en espérant laisser uniquement les outils utiles. Et dans tous les cas, l'HTML n'est pas pur.

        D'autres outils ou frameworks, beaucoup plus confidentiels, sont respectueux de l'HTML et ne le surchargent pas. On peut citer Ariato<sup><a href="#note-11">11</a></sup>, développé par Base Secrète, et PicoCSS<sup><a href="#note-12">12</a></sup>, par Lucas Larroche. Ces librairies sont très pertinentes pour améliorer le rendu de base de l'HTML, par exemple pour un back-office. En revanche, elles sont volontairement minimales, et intègrent des points de vue esthétiques qui peuvent ne pas convenir en fonction du projet. Il existe aussi des librairies de comportement, comme Compass, qui permettent d'écrire plus rapidement du CSS, sans imposer de bruit HTML. Ces librairies peuvent être utile, avec la même réserve que celle exprimée pour les préprocesseurs : il faut veiller à ce que le code généré soit compact et efficient.

        Les méthodologies BEM, SMACSS...

        frameworks JS

        Libs JS
      notes:
        - title: DRY
          url: https://en.wikipedia.org/wiki/Don%27t_repeat_yourself
        - title: Ariato
          url: https://ariato.org
        - title: PicoCSS
          url:
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
