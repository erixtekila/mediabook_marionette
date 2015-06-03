# Pourquoi Marionette.js ?

Backbone.js est un framework qui laisse beaucoup (trop ?) de libertés aux développeurs.
L'usage des classes proposées autant que la structure de l'application n'est pas du tout imposée.
De ce fait, il peut être intéressant de s'appuyer sur un outil complémentaire, afin de profiter de principes et méthodologies éprouvées.

## Frameworks complémentaires les plus populaires :

- [Chaplin.js](http://chaplinjs.org/)
- [Thorax](http://thoraxjs.org/)
- [LayoutManager](http://layoutmanager.org/)
- [Marionette.js](http://marionettejs.com/)

Tous ces outils proposent des réponses spécifiques aux problématiques récurrentes, mais laissées ouvertes par Backbone.js.

## Problématiques Backbone

### Gestion de l'affichage des `View`

La méthode `View.render()` n'a pas dimplémentation concrète. Le développeur est laissé libre de la redéfinir ou d'utiliser une combinaison d'autres méthodes.

De plus, le choix du moteur de _template_ n'est pas imposé.
Il est même possible de s'en passer, d'utiliser uniquement jQuery ou du javascript natif.

### Gestion du cycle de vie des `View`

Les `View` encapsulent un élément du DOM.

- Que devient-il lorsqu'il est supprimé ?
- Comment s'assure t-on que les événements auquel elle téiat abonné sont également bien supprimés ?
- Qui orchestre le dérouelement des opérations de création, de mise à jour et de destruction des éléments graphiques ?

### Communication entre `View`

Quelle méthodologie choisir pour établir une communication entre les différentes `View` de l'application ?

- Utilisation directe de jQuery ?
- Créer un système de gestion événementielle entre elles ?
- Modification d'un `Model` partagé ?
- Définir une route dédiée ?

### Structuration applicative

- Quel est le point de départ de votre webapp ?
- Comment partager des types ?
- Comment éviter de "polluer" l'espace global ?
