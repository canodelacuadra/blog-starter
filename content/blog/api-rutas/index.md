---
title: Cómo funciona el API de rutas en React
date: "2024-04-05T22:40:32.169Z"
---

## Cómo funciona el API de rutas en React
El API de rutas en React, también conocido como React Router, permite crear aplicaciones de una sola página (SPA) con una navegación fluida entre diferentes secciones o "vistas". Su funcionamiento se basa en tres pilares:

1. Rutas:

Las rutas son las URLs que se mapean a componentes específicos de React. Se definen usando el componente ``<Route>`` dentro del componente App. Cada ruta tiene dos propiedades principales:

- path: La URL que se asociará al componente.
- component: El componente que se renderizará cuando se acceda a la ruta.
Ejemplo
````JavaScript

<Route path="/" component={Home} />
<Route path="/about" component={About} />
````

2. Navegación:

React Router ofrece diferentes maneras de navegar entre las rutas:

   - Enlaces: El componente ``<Link>`` permite crear enlaces a otras rutas dentro de la aplicación.
   - Navegación programática: Puedes usar el hook ``useNavigate`` para navegar a una ruta de forma programática.
   - Redirecciones: Puedes usar el componente ``<Redirect>`` para redirigir a una ruta específica desde otra ruta.
  
3. Historial:

El historial del navegador se actualiza para reflejar los cambios de ruta en la aplicación. Esto permite al usuario usar los botones de "atrás" y "adelante" del navegador para navegar entre las vistas de la aplicación.

### Componentes adicionales:

React Router también ofrece otros componentes útiles para el manejo de rutas:

- Switch: Solo renderiza la primera ruta que coincida con la URL actual.
- Outlet: Se usa para renderizar el componente hijo de un componente Route.
- Params: Permite capturar parámetros de la URL y pasarlos al componente asociado a la ruta.
### Recursos adicionales:

- Documentación oficial de React Router: https://reactrouter.com/
- Tutoriales:
  - https://reactrouter.com/en/main/start/tutorial
  - https://www.youtube.com/watch?v=mHDZBGa8mHg
- En resumen:

> El API de rutas en React es una herramienta poderosa para crear aplicaciones SPA con una navegación fluida e intuitiva. Su funcionamiento se basa en la definición de rutas, la navegación entre ellas y la gestión del historial del navegador.

## Gestión de rutas en Gatsby
Gatsby usa el API de rutas de React (React Router) para gestionar las rutas de tu aplicación. Sin embargo, Gatsby también ofrece algunas características adicionales para facilitar la gestión de rutas:

1. Creación de páginas:

Gatsby crea automáticamente una ruta para cada archivo .js que se encuentra en la carpeta src/pages. El nombre del archivo se usa como la ruta, por ejemplo, src/pages/about.js crea la ruta /about.
Puedes usar el componente ``<Link>`` de React Router para crear enlaces a otras páginas.

2. Rutas dinámicas:

Puedes usar corchetes ``[]`` en el nombre del archivo para crear rutas dinámicas. Por ejemplo, ``src/pages/user/[id].js`` crea la ruta ``/user/:id`` donde ``:id`` es un parámetro dinámico.
Puedes acceder al valor del parámetro en el componente asociado a la ruta usando la API de React Router.

3. Redirecciones:

Puedes usar el archivo gatsby-node.js para configurar redirecciones.
Por ejemplo, puedes redirigir todas las URLs que comienzan con ``/old-page`` a la nueva página ``/new-page``.

4. API de File System Route:

Gatsby ofrece una API específica para crear rutas solo en el cliente.
Esto es útil para crear aplicaciones con contenido dinámico que se carga después de la carga inicial de la página.
### Recursos adicionales:
<div class='alert alert-primary'>
Documentación de Gatsby sobre rutas: https://www.gatsbyjs.com/docs/routing/
</div>


 
> En resumen:

> Gatsby facilita la gestión de rutas en aplicaciones React con características adicionales como la creación automática de páginas, rutas dinámicas, redirecciones y la API de File System Route.