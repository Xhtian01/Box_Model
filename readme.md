# Box Model

Describe como se dimensionan los elementos en una página web.

- ## Padding

  Define el espaciado exterior alrededor de un elemento. Crea un espacio entre el borde del elemento y los elemenos adyacentes.
  Cuando aplicamos un margin negativo el elemento se va a desplazar en la direccion opuesta a la que normalmente se desplazaría con un margin positivo.

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
