## Optimización de Rails para mortales = Uriel Hernandez


Principio de Pareto.

CTO y cofounder de [código facilito](https://codigofacilito.com/).


Hay que medir primero, para eso está MiniProfiler.

Cuánto tiempo tarda la página en carga? cuánto tardan los queries?

 Da insight del rendimiento de la app.

Complete guide to Rails performance. Referencia de cuánto es rápido y cuánto tiempo es lento.

Otra es New Relic. 

Qué parte de la  aplicación está tomando más tiempo. Dónde está respondiendo más lento.

Las mejoras:
- Actualizar versiones de Ruby, Rails y demás gemas.
- Las bases de datos y las consultas: 
    - Hacer índices para consultas más rápidas. Índice para la pk, que es el id de forma default.
    - Puede haber mal uso de índices
    - Usar campos con índices para ordenar o filtrar

`lol_dba` gem, reporta qué índices hacen falta en la app.

Evitar length para hacer conteos, usar count.

N+1 queries:
- Cuando se hace un query a una relación, se hace un query más por cada récord.
- Se puede precargar la relación para no hacer tantos llamados a la bd. 
- Bullet avisa cuando hay un problema de N+1 query.


Evalúa las soluciones, podemos introducir más problemas

Optimizar el frontend
- Comprimir assets:
    - Gzip - heroku deflater
    - Brotli

- Archivos independientes para features de temporada
- Evaluar cada librería
- Budget para el tamaño de los assets

urielhdz GitHub

Rails Performance fundamentals en pluralsight