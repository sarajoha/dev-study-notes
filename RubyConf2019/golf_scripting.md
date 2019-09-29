## Golf scripting with Ruby: Helping Santa schedule Christmas - Ely Alvarado. 

Empresa happy

Code golf. Hacer un algoritmo lo más corto que se pueda (menor cantidad de líneas).

Bin packing problem

Empaquetamiento ortogonal en 2d

2bp Bl algoritmo

**Live golfing**

La forma más corta, no eficiente:
- Reducir tamaño de nombres de variables.
- Eliminar comentarios innecesarios.
- Funciones que se usan una sola vez, que sea código en línea.
- Reducir iteraciones
- Encadenar métodos.
- Eliminar todo espacio no necesario.
- Unir líneas.

Advertencia:
Muchas veces generas código inútil, pero aprendes a pensar fuera de la caja

Tips para Ruby
- Cadenas de caracteres de longitud uno (como `"a"`) se pueden reescribir con: `?a`
- Método `p` devuelve nil
- `!p` es true
- `!0` es falso
- Interpolación de string en vez de `.to_s`
- Se pueda usar notación científica para números mayores a mil
- `1.*2+3`, cambia precedencia de operaciones y hace la suma primero
- Para hacer arrays 
    - En vez de compact usar `array - p`
    - `array & array` devuelve valores únicos (es una intersección)