# Modern JavaScript

Projet exemple permettant d'introduire l'utilisation et l'outillage de JavaScript en 2017.

# Étapes

## 01 - Node.js

[Node.js](https://nodejs.org) est un environnement d'exécution JavaScript basé sur le moteur de Chrome. Il peut être utilisé pour faire du développement backend ou pour écrire des scripts.

Il est recommandé d'utiliser un gestionnaire de versions comme [nvm](https://github.com/creationix/nvm) ou [n](https://github.com/tj/n) afin de pouvoir utiliser parallèlement plusieurs versions de Node.

Par exemple avec nvm :

    nvm ls-remote               # affiche les versions disponibles
    nvm install v6.11.0         # installe la dernière version LTS
    nvm alias default lts/boron # utilise par défaut la dernière version LTS

## 02 - Yarn

[Yarn](https://yarnpkg.com) est un gestionnaire de dépendances.
Il est plus performant et plus fiable que le gestionnaire de paquets `npm` fourni avec `Node` mais la version 5 de `npm` a 
permis de combler le retard entre les deux gestionnaires. Libre à vous désormais d'utiliser `yarn` et `npm` (version 5).

La première chose à faire est d'initialiser le projet en créant un fichier `package.json` qui contient la description du projet, ses dépendances, ses scripts et bien d'autres choses (plus ou moins équivalent au fichier `pom.xml` pour les développeurs Java).

    yarn init # initialise le descripteur du projet

## 03 - Babel

[Babel](https://babeljs.io/) est un transpileur JavaScript permettant de transformer du JavaScript moderne en JavaScript moins moderne !
Il faut savoir que JavaScript évolue rapidement (par le biais de l'organisme de standardisation ECMA) et que les navigateurs n'évoluent 
pas aussi vite. `Babel` vous permet d'écrire du JavaScript moderne et de cibler tout de même la quasi-totalité des navigateurs.

    # yarn add --dev babel-cli babel-preset-env # installe le client Babel et les réglages par défaut les plus récents

Puis configurer Babel afin d'utiliser les réglages que vous venez d'installer en créant le fichier `.babelrc` avec le contenu suivant :

    {
        "presets": ["env"]
    }
