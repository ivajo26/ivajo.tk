---
layout: post
title:  "Integrar Stylus con React"
date:   2017-05-05 19:46:00 -0500
categories: React, Frontend, HTML, CSS, JS
abstract: "Si deseas integrar stylus con react usando Webpack, aqui te dejo algunas las configuraciones necesarias para hacerlo. "
---
Para muchos **Frontend** es importante el uso de ***Pre-procesadores de CSS***, dado las múltiples ventajas que nos permiten mejorar nuestro trabajo.

React se ha convertido en una excelente alternativa a usar para muchos proyectos dado en sus grandes ventajas, las cuales no mencionaremos en este post; pero una de esas es la implementación de los archivos **.jsx** con la cual se busca unir ***HTML, CSS*** y ***JS***, y trabajar todo a partir de módulos, algo que es excelente si pensamos en componentes.

Para trabajar con react y aprovechar al máximo su potencial **Webpack** es una herramienta excelente para configurar nuestros proyectos, ahora te mostraré cómo integrar Stylus a nuestras configuraciones.

Teniendo nuestro proyecto de react con webpack debemos hacer lo siguiente:

Primero instalaremos algunos paquetes necesarios:

```
npm install stylus-loader css-loader style-loader stylus
```
o
```
yarn add stylus-loader css-loader style-loader stylus
```

Luego en nuestro archivo `webpack.config.js`:

```
module: {
  rules: [
    .
    .
    .
    {
      test: /\.styl$/,
      loader: 'style-loader!css-loader?modules&importLoaders=1&localIdentName=[name]__[local]___[hash:base64:5]!stylus-loader',
    },
    .
    .
    .
  ],
},
```

Y listo de esta manera hemos integrado Stylus a nuestro proyecto de react.
