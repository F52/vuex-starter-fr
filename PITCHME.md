---?image=http://f52.tech/_nuxt/img/f52_welcome.2393ff7.jpg&size=cover

<span class="menu-title" style="display: none;">Débuter avec Vuex (la bibliothèque Redux pour Vue.js)</span>

## <span style="color: white;"> Débuter avec Vuex<br/>(bibliothèque Redux pour Vue.js)</span>

<span style="color: lightgray;">Cédric Foellmi – F52 Technologies<br/>cedric@f52.tech –</span> http://f52.tech

---

## Table des matières

* Redux: pourquoi ?
* Redux: les principes
* Vue.js et Vuex
* Vuex et les "namespaces"

---

<span class="menu-title" style="display: none">Introduction (1)</span>

## Introduction (1)

Redux est un container prévisible d'état (predictable state container). Il a été développé pour résoudre un problème **central** dans les logiciels applicatifs: l'état et ses changements.

_Running Joke_: Le pattern MVC signifie _Massive View Controller_ ...

Quelques problèmes importants quand la _codebase_ d'une app grandit:
- Des morceaux d'état se disperse à travers toute l'app, ses composants etc.
- Des problèmes de plus haut niveau surgissent ("pourquoi l'état (ne) change (pas) à cet endroit, et (pas) à cet autre endroit ?")
- Le déboguage devient bien plus difficile: il devient impossible de _rejouer_ les changements d'état

---

<span class="menu-title" style="display: none">Introduction (2)</span>

## Introduction (2)

**Redux ne résoud pas tout**

En particulier:
- L'état très localisé reste très utile s'il n'a pas besoin d'être partagé en dehors de son contexte
- Si les données ne changent pas, redux n'est pas utile
- Redux est designé pour être prédictif, pas forcément concis...

https://medium.com/@dan_abramov/you-might-not-need-redux-be46360cf367

The tradeoff that Redux offers is to add indirection to decouple “what happened” from “how things change”.

De plus, il oblige à une certaine discipline qui peut être contraignante

---

<span class="menu-title" style="display: none">Introduction (3)</span>

## Introduction (3)

Redux a commencé avec Flux... puis Redux.js puis...

---

<span class="menu-title" style="display: none">Introduction (2)</span>

## Principes

* Single-source of truth
* State is read-only
* Changes are made with pure functions
(A pure function is a function where the return value is only determined by its input values, without observable side effects.)
