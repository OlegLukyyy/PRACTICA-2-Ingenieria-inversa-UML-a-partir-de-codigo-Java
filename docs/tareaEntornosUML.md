# Cuestiones de análisis – Diagrama de Clases UML

## ¿Qué tipo de relación existe entre Agenda y Contacto?

La relación entre `Agenda` y `Contacto` es una **asociación de uno a muchos (1..\*)**, ya que una agenda puede contener varios contactos.  
Esta relación puede interpretarse como una **agregación**, puesto que los contactos existen de forma independiente y podrían pertenecer a otra agenda o existir fuera de ella.

---

## ¿Qué tipo de relación existe entre Contacto y Telefono?

La relación entre `Contacto` y `Telefono` es de **uno a muchos (1..\*)**.  
Se modela como una **composición**, ya que los teléfonos forman parte del contacto y no tienen sentido dentro del sistema sin estar asociados a uno. Al eliminar un contacto, también se eliminan sus teléfonos.

---

## ¿Qué tipo de relación existe entre Contacto y Direccion?

La relación entre `Contacto` y `Direccion` es de **uno a uno (1..1)**.  
Se trata de una **composición**, porque la dirección pertenece exclusivamente a un contacto y no se comparte con otros. Si el contacto desaparece, su dirección también deja de existir.

---

## ¿Por qué los tipos TipoTelefono y TipoVia se modelan como enumerados?

`TipoTelefono` y `TipoVia` se modelan como **enumerados** porque representan conjuntos **cerrados y predefinidos de valores posibles**.  
El uso de enumerados evita valores incorrectos, mejora la legibilidad del código y facilita el mantenimiento, además de reflejar correctamente el dominio del problema en el modelo UML.

---

## ¿Qué relaciones del diagrama son asociaciones simples y cuáles podrían interpretarse como agregación o composición?

- **Agenda – Contacto**: agregación
- **Contacto – Telefono**: composición
- **Contacto – Direccion**: composición
- **Direccion – TipoVia**: asociación simple
- **Telefono – TipoTelefono**: asociación simple
