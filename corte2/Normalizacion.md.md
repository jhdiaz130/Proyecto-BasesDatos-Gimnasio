# Normalización (1FN → 3FN)

En el diseño de la base de datos del gimnasio se aplicó la normalización hasta la **Tercera Forma Normal (3FN)** para asegurar consistencia, eliminar redundancias y optimizar el almacenamiento de la información.  

## Primera Forma Normal (1FN)
- Se eliminaron grupos repetidos y se aseguraron atributos atómicos.  
- Ejemplo: en la tabla **Cliente**, los campos `nombre` y `apellido` se almacenan por separado.  
- El teléfono de un cliente se guarda en un único campo, evitando listas o valores múltiples en la misma celda.  

✅ Todas las tablas cumplen con 1FN.  

## Segunda Forma Normal (2FN)
- Como todas las tablas utilizan claves primarias simples (un único atributo como PK), no existen dependencias parciales.  
- Cada atributo no clave depende directamente de la clave primaria.  

✅ Todas las tablas cumplen con 2FN.  

## Tercera Forma Normal (3FN)
- Se eliminaron dependencias transitivas.  
- Cada atributo depende únicamente de la clave primaria y no de otros atributos no clave.  
- Ejemplo: en la tabla **Plan**, el atributo `precio` depende de `id_plan` y no de otro campo.  

✅ Todas las tablas cumplen con 3FN.  

---

### Conclusión
El modelo relacional diseñado se encuentra normalizado hasta la **3FN**, lo que asegura que la base de datos esté organizada, sin redundancia de datos y con la integridad necesaria para su futura implementación en Python.
