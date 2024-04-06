---
title: Funcionamiento de las variables en CSS
date: "2024-04-06T10:26:32.169Z"
description: Explicamos lo que son las variables en CSS y mostramos las ventajas de su  utilización.
---

Las variables CSS, también conocidas como propiedades personalizadas, se introdujeron en la especificación de CSS en 2016 y  compatibles por los navegadores web a partir del 2017. Actualmente, las variables CSS son compatibles con la mayoría de los navegadores web modernos.
Las variables CSS, también conocidas como propiedades personalizadas, permiten almacenar valores y reutilizarlos en diferentes partes de una hoja de estilos.

## Declaración
Antes de usarse, ha de declararse y ésto suele hacerse en el inicio de la hoja de estilos. Tiene la siguiente sintaxis en general:
````CSS

--nombre-variable: valor;
````

Ejemplo:
````CSS
--color-principal: #00ff00;
````

## Uso:

Para usar una variable CSS, se utiliza la función ````var()````:

````CSS
color: var(--color-principal);
````


````CSS
h1 {
  color: var(--color-principal);
}
````
En este ejemplo, el color de todos los elementos ````<h1>```` será verde (#00ff00).

## Ventajas del uso de variables:

- Reutilización de valores: Puedes usar el mismo valor en diferentes partes de tu hoja de estilos sin necesidad de repetirlo.
- Mantenimiento: Es más fácil mantener tu código CSS si usas variables.
- Legibilidad: El código CSS es más legible si usas nombres descriptivos para las variables.
- Flexibilidad: Puedes cambiar el valor de una variable en un solo lugar y se actualizará automáticamente en todo el código.
## Ámbito:

Las variables CSS tienen un ámbito o alcance, que determina dónde se pueden usar. El ámbito puede ser:

- Global: La variable se puede usar en cualquier parte del documento.
- Local: La variable solo se puede usar en el elemento donde se declara o en sus descendientes.
### Ejemplo de ámbito global:

````CSS
:root {
  --color-principal: #00ff00;
}

h1 {
  color: var(--color-principal);
}

p {
  color: var(--color-principal);
}
````
En este ejemplo, la variable --color-principal es global, por lo que se puede usar en los elementos ````<h1>```` y ````<p>````.

### Ejemplo de ámbito local:

````
.contenedor {
  --color-principal: #00ff00;

  h1 {
    color: var(--color-principal);
  }

  p {
    color: #000000;
  }
}
````
En este ejemplo, la variable --color-principal es local al elemento .contenedor. Solo se puede usar en el elemento ````<h1>```` que está dentro del contenedor.