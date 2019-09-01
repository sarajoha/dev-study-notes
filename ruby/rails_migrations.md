Las migraciones van a actualizar el esquema de la base de datos `db/schema.rb`

Para correr las migraciones se ejecuta:
`rails db:migrate`

Para revisar el estatus de las migraciones:
`rails db:migrate:status`

Generar migracion vacia:
`rails generate migration MigrationName`
Al hacerlo de esta forma, el archivo se crear con el timestamp y con la funcion `change` vacia.
Dentro de esta funcion se escribe el codigo para modificar el esquema.

Las migraciones se pueden revertir usando
`rails db:rollback`


### Crear tablas

- Al crear una tabla nueva no hace falta agragar una columna para el `id`, se agrega de forma implicita.
- Cuando se genera una migracion para crear una tabla, la linea de `t.timestamp` agraga dos campos a la tabla,
    el de `created_at` y `updated_at`


Una migracion para crear una tabla tendria esta estructura:

```
create_table :table_name do |t|
    t.column_type :column_name
    .
    .
    .
end
```

Una para modificar una tabla seria asi:
```
change_table :table_name do |t|
    t.remove :column_name
    t.column_type :column_name # agregar una columna
    t.rename :old_column_name, :new_column_name 
end
```


Y una para cambiar columnas directamente se veria asi:
```
:remove_column, :table_name, :column_name, :desired_change
:add_column            "            "             "          
:change_column         "            "             "          # este cambio no es reversible!
:change_column_null    "            "             "
:change_column_default "            "             "          # este cambio no es reversible! mejor usar es de la linea de abajo
:change_column_default "            "      from: current, to: desired_change # este cambio es reversible          
```