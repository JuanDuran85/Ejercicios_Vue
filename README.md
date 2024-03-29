# Vue

```bash
    -p, --preset <presetName>       omitir indicaciones
    -d, --default                   usar el default en la creación
    -m, --packageManager <command>  Usar npm o yarn
    -n, --no-git                    Sin utilizar git
    -b, --bare                      Sin isntrucciones para principiantes
```

```bash
vue create ejemplo1 -dnm yarn
```

```bash
vue init simple nombre_proyecto
vue init webpack-simple nombre_proyecto
npm install -g npm-check-updates
ncu
ncu -u
```

```js
"production":"vue-cli-service build --modern"
```

```bash
npx http-server ./dist/
```

## Usando servidor local para json
- Instalacion de json-server
  ```bash
   npm install -g json-server
  ```
- Levanando el servidor local. Crear archivo json con el nombre db
  ```bash
  json-server db.json
  ```

## Libreria para monedas: Accounting.js

* [Repositorio](http://openexchangerates.github.io/accounting.js/).

* [CDN](https://raw.githubusercontent.com/openexchangerates/accounting.js/master/accounting.js).

```bash
npm i accounting
o
yarn add accounting
```
* Uso:
  ```javascript
    import accounting from 'accounting';
    accounting.formatMoney(valor)
  ```

## Libreria para Fechas: [moment.js](https://momentjs.com/)

* [Repositorio](https://github.com/moment/moment/).
* [CDN](https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.14.1/moment-with-locales.js).
* [Web](https://momentjs.com/).

```bash
npm i moment
o
yarn add moment
```

## Libreria de CSS Bootstrap

* [Repositorio](https://github.com/moment/moment/).
* [CDN-CSS](https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css).
* [CDN-jQuery](https://code.jquery.com/jquery-3.4.1.slim.min.js).
* [CDN-popper](https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js).
* [CDN-bootstrap](https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js).
* [Web](https://getbootstrap.com/).

```bash
npm i bootstrap jquery popper.js
o
yarn add bootstrap jquery popper.js @popperjs/core
```
* utilizacion en el main.js o index.js
  ```js
    import 'bootstrap'; 
    import 'bootstrap/dist/css/bootstrap.min.css';
    window.$ = window.jQuery = require('jquery');
  ```

## Uso de Babel - plugin-syntax-dynamic-import

Esta dependencia permitirá trabajar e implementar desde VueJS las Lazy Loading Routes en conjunto con Vue-Router.

[Documentación Oficial para Vue-Router](https://router.vuejs.org/guide/advanced/lazy-loading.html#grouping-components-in-the-same-chunk)
[Documentación oficial para babel:](https://babeljs.io/docs/en/babel-plugin-syntax-dynamic-import/).

Instalacion de la dependencia: 

```bash
npm install --save-dev @babel/plugin-syntax-dynamic-import
o
yarn add --dev @babel/plugin-syntax-dynamic-import
```

## Instalando Vue-Router

* Sitio oficial:
    [Vue-Router](https://router.vuejs.org/)

* Usando el CDN o descarga del archivo:
    [CDN/descarga](https://unpkg.com/vue-router/dist/vue-router.js)

    ```javascript
      <script src="https://unpkg.com/vue-router@3.1.6/dist/vue-router.js"></script>
    ```

* Instalacion con NPM:
```bash
npm i --save vue-router
```

* Instalacion con Yarn:
```bash
yarn add vue-router
```

## Instalando Vuex

* Sitio oficial:
    [Vuex](https://vuex.vuejs.org/),

* Usando el CDN o descarga del archivo:
    [CDN/descarga](https://unpkg.com/vuex)

    ```javascript
      <script src="https://unpkg.com/vuex@3.1.3/dist/vuex.js"></script>
    ```

* Instalacion con NPM:
```bash
npm -i vuex --save
```

* Instalacion con Yarn:
```bash
yarn add vuex
```

* Utilizar mapState, mapGetters

```javascript
import {mapState, mapGetters} from 'vuex'
```

## Instalando Bootstrap-Vue

Para trabajar con bootstrap-vue es necesario primero instalar bootstrap.

* Sitio oficial:
    [Bootstrap-Vue](https://bootstrap-vue.js.org/),

* Usando el CDN o descarga del archivo:

    ```html
      <head>
        <!-- Load required Bootstrap and BootstrapVue CSS -->
        <link type="text/css" rel="stylesheet" href="//unpkg.com/bootstrap/dist/css/bootstrap.min.css" />
        <link type="text/css" rel="stylesheet" href="//unpkg.com/bootstrap-vue@latest/dist/bootstrap-vue.min.css" />
        <!-- Load polyfills to support older browsers -->
        <script src="//polyfill.io/v3/polyfill.min.js?features=es2015%2CIntersectionObserver" crossorigin="anonymous"></script>
        <!-- Load Vue followed by BootstrapVue, and BootstrapVueIcons -->
        <script src="//unpkg.com/vue@latest/dist/vue.min.js"></script>
        <script src="//unpkg.com/bootstrap-vue@latest/dist/bootstrap-vue.min.js"></script>
        <script src="//unpkg.com/bootstrap-vue@latest/dist/bootstrap-vue-icons.min.js"></script>
      </head>
    ```

* Instalacion con NPM:
```bash
npm i bootstrap-vue
```

* Instalacion con Yarn:
```bash
yarn add bootstrap-vue
```

* utilizacion en el main.js o index.js
  ```js
    import 'bootstrap/dist/css/bootstrap.css';
    import 'bootstrap-vue/dist/bootstrap-vue.css';

    import { BootstrapVue, IconsPlugin } from 'bootstrap-vue'

    // Install BootstrapVue
    Vue.use(BootstrapVue)
    // Optionally install the BootstrapVue icon components plugin
    Vue.use(IconsPlugin)
  ```

## Utilizando Webpack, NodeJS y ExpressJS

```bash
node ./node_modules/webpack/bin/webpack --config ./build/webpack.config.js 
```

## Configurando e instalando FireBase

Para trabajar con firebase debes tener una cuenta de Google, ir al sitio web oficial y crear un nuevo proyecto, haciendo clic en comenzar, luego en añadir proyecto, escribir el nombre del proyecto y seguir los pasos.

* Sitio oficial:
    [Firebase](https://firebase.google.com/)

* Documentación para JavaScript con Firestore.
    [Firestore](https://firebase.google.com/docs/reference/js/firebase.firestore.Firestore)

* Instalacion con NPM:
```bash
npm i firebase --save
```

* Instalacion con Yarn:
```bash
yarn add firebase -D
```

* Para llevar una aplicacion al Hosting de firebase, se debe:
1. Crear el proyecto en firebase
2. Entrar en la seccion del hosting
3. Hacer un clic en iniciar o get started
4. Instalar mediante la terminal firebase tool con:
    Con NPM
    ```bash
      npm i firebase-tools -g
      ```
    Con Yarn
      ```bash
      yarn global add firebase-tools
    ```
5. Luego clic en continuar dentro de firebase hosting
6. Ahora en el editor, dentro del proyecto, se debe iniciar sesion de firebase con el comando: ```firebase login```, seleccionando o iniciando la sesion con la cuenta de gmail donde se encuentra ejecutando firebase hosting en la web
7. Ahora en la terminal, se debe iniciar el proyecto con ```firebase init```
8. Luego si en proceder
9. Despues seleccionar el hosting
10. Posteriormente selecciona el proyecto en el cual tienes activo el hosting.
11. Ahora se debe escribir el nombre del directorio donde se encontraran los archivos de produccion. En este caso se debe ingresar "dist" porque este sera el nombre de la carpeta que crea vue-cli para al produccion.
12. Indicar que si para compilar en una SFC
13. Finalizado el proceso de configuracion de firebase, se debe iniciar el proceso de produccion con vue-cli mediante el comando "build", ya sea:
    Con NPM
    ```bash
      npm run build
      ```
    Con Yarn
      ```bash
      yarn build
    ```
14. Terminado el procesod e produccion de vue-cli, se debe enviar los archivos de la carpeta dist al hosting de firebase, mediante la instruccion: ```firebase deploy --only hosting```
    
## Aplicando FontAwesome

Para utilizar la libreria de FontAwesome de manera local sin el CDN, se deben instalar las dependencias:

* Instalacion con NPM:
```bash
$ npm i --save @fortawesome/fontawesome-svg-core
$ npm i --save @fortawesome/free-solid-svg-icons
$ npm i --save @fortawesome/vue-fontawesome
```

* Instalacion con Yarn:
```bash
yarn add @fortawesome/vue-fontawesome -D
yarn add @fortawesome/free-solid-svg-icons -D
yarn add @fortawesome/fontawesome-svg-core -D
yarn add @fortawesome/fontawesome-free -D
```

* Sitio Oficial:
    [Vue-Fontawesome](https://github.com/FortAwesome/vue-fontawesome)

```javascript
import { library } from '@fortawesome/fontawesome-svg-core';
import { faCheck, faTimes } from '@fortawesome/free-solid-svg-icons';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

library.add(faCheck);
library.add(faTimes);

Vue.component('font-awesome-icon', FontAwesomeIcon);
```

## Instalando Axios

* Sitio oficial:
    [Axios](https://github.com/axios/axios),

* Usando el CDN:

    ```javascript
      <script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>
      ```
      o
      ```javascript
      <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
      ```

* Instalacion con NPM:
```bash
npm install axios --save-dev
```

* Instalacion con Yarn:
```bash
yarn add axios -D
```

Para usar a Axios, se debe importar en cada componente donde se desea implementar dentro del script:

```javascript
import axios from 'axios';
```

## Instalando VueFire

* Sitio Oficial:
  [VueFire](https://vuefire.vuejs.org/)

* Instalacion con NPM:
```bash
npm install vuefire firebase
```

* Instalacion con Yarn:
```bash
yarn add vuefire firebase
```

## ¿Qué es el testeo de aplicaciones?

Es el proceso de someter una aplicación a diferentes pruebas para comprobar que ésta funcionacorrectamente. 

 ### Tipos de tests y técnicas de desarrollo con tests

Para mayor información: [Vue Test Utils](https://vue-test-utils.vuejs.org/) 

#### Unitario

Un test unitario o “prueba unitaria” es un tipo de test automatizado, es decir, se debe poder ejecutarsin necesidad de intervención manual. Este test, se utiliza para comprobar que un método concretodel código de producción funciona correctamente.

#### Tests end-to-end

Es una metodología que se utiliza para probar si el flujo de una aplicación se está ejecutando segúnlo  diseñado de  principio a  fin.

La diferencia que tiene con los tests unitarios, es que end-to-end se enfoca en el sistema de maneraintegral, es decir probarlo como un todo.

#### Técnicas TDD y BDD

Ambas técnicas, están orientadas a crear aplicaciones más robustas y centradas en los requisitosmás que en el contenido propio del código

Desarrollo guiado por pruebas de software, o **Test-driven development (TDD)**, es una técnica quese  basa en  un  desarrollo de  pruebas a  través de  las  cuales debe pasar el  código, si  está bienimplementado, se continúa creando código enfocado hacia la siguiente prueba, sinó, se configurahasta que pase la prueba y podamos ir a la siguiente fase.

Desarrollo dirigido por comportamiento o **Behavior Driven Development (BDD)**, como bien lo indicasu nombre, no se trata de una técnica de testing, sino que es una estrategia de desarrollo (así comoTDD).

Mientras TDD se enfoca en la prueba unitaria, BDD en cambio, se enfoca en la prueba de más altonivel, la prueba funcional, la de aceptación, el foco está en cumplir con el negocio y no solo con elcódigo.

#### Assertions

Una aseveración es  una  expresión booleana  en  un  punto específico de  un  programa  que  seráverdadera a menos que haya un error en el programa.

#### Mocks

O  "Mock  object" son  sustitutos de  objetos o  componentes del  sistema, utilizados en  reemplazodurante las pruebas. Su principal función es validar que ciertos métodos sean llamados en los objetos que están imitando

#### Stubs

Una función, Método o  fragmento de  código sustituto, que  simula un  comportamiento específicodentro de un objeto para facilitar las pruebas
