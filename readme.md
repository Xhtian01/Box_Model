# Box Model

Describe como se dimensionan los elementos en una página web.

- ## Padding

  Define el espaciado exterior alrededor de un elemento. Crea un espacio entre el borde del elemento y los elemenos adyacentes.

  ```
  .element {
  padding: 10px 20px; /* 10px arriba y abajo, 20px derecha e izquierda */
  }
  ```

  ### Colapso de margenes verticales

  Es un comportamiento en donde los margenes verticales de los elementos se combinan en lugar de sumarse.

  ```
   .padre {
    margin-top: 20px;
  }
  .hijo {
    margin-top: 30px;
  }

  /* El margen superior del hijo (30px) colapsará con el margen superior del padre (20px), resultando en un margen total de 30px en lugar de 50px. */
  ```

- ## Margin

  Define el espacio entre el contenido del elemento y su borde

  ```
  elemento {
  margin: 15px;
  }
  ```

  ### Margin Negativo

  Cuando aplicamos un margin negativo el elemento se va a desplazar en la direccion opuesta a la que normalmente se desplazaría con un margin positivo.

  ```
   elemento {
    margin-top: -20px; /* Mueve el elemento 20px hacia arriba */
   }
  ```

- ## Border

  Es una línea que rodea el contenido y el padding del elemento

  ```
  contenedor {
  border: 1px solid black;
  }
  ```

# Selector Universal

Se utiliza para seleccionar todos los elementos de la página web y se le aplicará el estilo que nosotros deseemos.

```
* {
  margin: 0;
  padding: 0;
}
```

# Box-sizing: border-box

Se utiliza para que cuando añadimos un padding o border no incrementará el tamaño total del elemento.

```
.elemento {
  box-sizing: border-box;
  width: 200px;
  padding: 20px;
  border: 10px solid black;
}

/* Aquí, el ancho total del elemento seguirá siendo 200px, ya que el padding y el borde están incluidos en los 200px definidos. */
```

# Posicionamiento

- ## Relative

  El elemento se posiciona en el flujo normal del documento, se puede desplazar respecto a su posición original usando las propiedades top, right, bottom, left.

```
.relative {
  position: relative;
  top: 20px; /* Mueve el elemento 20px hacia abajo */
  left: 10px; /* Mueve el elemento 10px hacia la derecha */
}
```

- ## Absolute

  El elemento se posiciona respecto a su elemento padre mas cercano. Si no tiene un elemento padre asignado, se va a posicionar respecto al contenedor inicial del documento.

  ```
  .padre {
  position: relative;
  }

  .hijo{
  position: absolute;
  top: 20px; /* Posiciona el elemento 20px desde el borde superior del elemento padre */
  left: 10px; /* Posiciona el elemento 10px desde el borde izquierdo de elemento padre */
  }
  ```

- ## Fixed

  El elemento se posiciona respecto al contenedor inicial del documento, permanecerá en la misma posición cuando se haga scroll en la página.

  ```
  .fixed {
  position: fixed;
  top: 10px; /* Posiciona el elemento 10px desde el borde superior del viewport */
  right: 10px; /* Posiciona el elemento 10px desde el borde derecho del viewport */
  }
  ```

- ## Sticky

  El elemento se va a comportar como "relative" y se convierte en un elemento "fixed" al alcanzar un umbral durante el scroll.

  ```
  .sticky {
  position: sticky;
  top: 0; /* El elemento se pegará en la parte superior del contenedor padre cuando se haga scroll */
  }
  ```

# Propiedades

- ## top

  Define la distancia entre el borde superior del elemento y el borde superior del contenedor de referencia.

  ```
  .element {
  top: 20px; /* Mueve el elemento 20px hacia abajo */
  }
  ```

- ## right

  Define la distancia entre el borde derecho del elemento y el borde derecho del contenedor de referencia.

  ```
  .element {
  right: 20px; /* Mueve el elemento 20px hacia la izquierda */
  }
  ```

- ## bottom

  Define la distancia entre el borde derecho del elemento y el borde derecho del contenedor de referencia.

  ```
  .element {
  bottom: 20px; /* Mueve el elemento 20px hacia arriba */
  }
  ```

- ## left

  Define la distancia entre el borde derecho del elemento y el borde derecho del contenedor de referencia.

  ```
  .element {
  left: 20px; /* Mueve el elemento 20px hacia la derecha */
  }
  ```

- ## z-index
  Determina el orden en que los elementos se superponen unos a otros. Un elemento con un z-index mayor se apilará por encima de un elemento con un z-index menor.

```
  .box1 {
    background-color: red;
    top: 50px;
    left: 50px;
    z-index: 1; /* Apilará por encima de .box3 */
  }

  .box2 {
    background-color: blue;
    top: 100px;
    left: 100px;
    z-index: 2; /* Apilará por encima de .box1 y .box3 */
  }

  .box3 {
    background-color: green;
    top: 150px;
    left: 150px;
    z-index: 0; /* Apilará por debajo de .box1 y .box2 */
  }
```
