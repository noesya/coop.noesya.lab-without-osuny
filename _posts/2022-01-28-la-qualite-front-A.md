---
title: Qualité front A
draft: true
category: rd
year: 2022
sections:
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
---
