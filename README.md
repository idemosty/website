# Idemosty

> Premier projet d'Idemosty 👏

## Technologies

-  🔥 [Vue 3](https://v3.vuejs.org/guide/introduction.html) - framework js
-  🚀 [Vite](https://vitejs.dev/guide/) - bundle tool, very fast development step
-  ✂ [TailwindCSS](https://tailwindcss.com/) - utility-first CSS framework for rapidly building custom designs.
-  😺 [Yarn](https://yarnpkg.com/) - dependencies manager.

## Getting started:

```shell
$ git clone
$ yarn
$ yarn dev
```

Now you can visit [`localhost:3000`](http://localhost:3000) from your browser.

## Contributing

-  Install [Pre-commit](https://pre-commit.com/) whit `pre-commit install` before committing.
-  Install [CZ-cli](https://github.com/commitizen/cz-cli) whit `npm install commitizen -g` before committing with `git cz`.

## Note

### Tree structure

Using Atomic desgin
https://atomicdesign.bradfrost.com/chapter-2/

### Vue 3 devtools

To use chrome extension vue-devtools, need to install the beta version : https://chrome.google.com/webstore/detail/vuejs-devtools/ljjemllljcmogpfapbkkighbhhppjdbg/related

### Vite definition

Vite est un outil qui est un alternative au bundler (webpack/parcel..) pour la phase de dévelopement. Plutôt que de générer un "bundle" à chaque modification d'un fichier, Vite se repose sur le support des import natif des navigateurs en créant un serveur personnalisé (basé sur koa) qui va délivrer des fichiers JS compatibles.

Il intègre le hot-reload, plus besoin de regénérer les fichiers à chaque modification, met à jours la page sans perdre son état.
Fortement conseillé sur des projets relativement grand ou avec beaucoup de process.

### Desgin

Template du site (en js vanilla) : https://github.com/tailwindtoolbox/Landing-Page
