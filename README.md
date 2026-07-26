# Archipiélago Vivo · Repositorio de Imágenes de Entidades

Repositorio oficial de imágenes utilizadas por el mapa colaborativo de **Archipiélago Vivo**.

Su finalidad es almacenar de forma centralizada las imágenes asociadas a las entidades del proyecto para que puedan ser referenciadas mediante una URL estable desde Google Sheets, uMap y cualquier otra aplicación del ecosistema.

---

# Objetivos

- Centralizar todos los recursos gráficos del proyecto.
- Mantener URLs permanentes para evitar enlaces rotos.
- Facilitar la automatización del mapa.
- Mantener una organización sencilla y escalable.
- Reducir la dependencia de servicios externos.

---

# Organización

Las imágenes se almacenan utilizando **el mismo identificador único (ID) de la entidad en Google Sheets**.

El nombre de la entidad **no forma parte del nombre del archivo**.

Esto permite cambiar nombres, categorías o cualquier otro dato sin modificar la URL de la imagen.

Ejemplo:

```
entities/
├── AV-000001.webp
├── AV-000002.webp
├── AV-000003.webp
├── AV-000004.webp
└── AV-000005.webp
```

---

# Convención de nombres

Cada archivo debe llamarse exactamente igual que el **ID de la entidad**.

Ejemplos:

```
AV-000001.webp
AV-000245.webp
AV-001327.webp
```

No utilizar:

```
plastiman.webp
logo-plastiman.webp
empresa1.jpg
foto.png
```

El nombre visible de la entidad pertenece únicamente a la base de datos.

---

# Formatos admitidos

## Recomendado

- WebP

## Compatibles

- PNG
- JPG

---

# Especificaciones recomendadas

- lado mayor: 1200 px
- calidad WebP: 80–90 %
- fondo transparente cuando sea posible
- imagen optimizada para web

---

# Contenido recomendado

Siempre que sea posible utilizar:

- logotipo oficial
- fotografía representativa
- retrato (personas)
- fachada o espacio físico
- imagen institucional

Evitar:

- capturas de pantalla
- imágenes pixeladas
- marcas de agua
- fotografías con texto superpuesto
- imágenes excesivamente pesadas

---

# Relación con Google Sheets

Cada entidad dispone de un identificador único.

Ejemplo:

| ID | Nombre |
|----|---------|
| AV-000001 | Plastiman Canario |
| AV-000002 | Asociación Ejemplo |

La columna **Image** puede construirse automáticamente a partir del ID.

Ejemplo:

```
https://raw.githubusercontent.com/Archipielago-Vivo/entity-images/main/entities/AV-000001.webp
```

De esta forma no es necesario escribir manualmente ninguna URL.

---

# Flujo de trabajo

1. Crear la entidad en Google Sheets.
2. Asignar un ID único.
3. Obtener la imagen.
4. Optimizarla.
5. Guardarla con el nombre del ID.
6. Subirla al repositorio.
7. La URL queda automáticamente disponible para el mapa.

---

# Buenas prácticas

Antes de subir una imagen comprobar que:

- representa correctamente a la entidad;
- tiene una resolución suficiente;
- está optimizada para web;
- utiliza el ID correcto;
- no existe otra versión anterior.

---

# Derechos de autor

Las imágenes continúan perteneciendo a sus respectivos autores o titulares.

Siempre que sea posible:

- utilizar imágenes proporcionadas por la propia entidad;
- utilizar material con licencias compatibles;
- indicar la fuente en la ficha correspondiente del mapa.

Este repositorio actúa únicamente como almacenamiento y distribución técnica de los archivos.

---

# Estabilidad de URLs

Una vez publicada una imagen:

- el ID **no debe cambiar**;
- el nombre del archivo **no debe cambiar**;
- la ruta **debe permanecer estable**.

Si una imagen necesita actualizarse, deberá sustituirse el archivo existente manteniendo exactamente el mismo nombre.

Esto garantiza que todos los enlaces continúen funcionando sin necesidad de modificar Google Sheets ni uMap.

---

# Proyecto

Este repositorio forma parte de **Archipiélago Vivo**, una iniciativa colaborativa para documentar y visibilizar el ecosistema social, cultural, científico, económico, ambiental e institucional de Canarias.

Más información:

https://github.com/Archipielago-Vivo

---

# Licencia

Salvo que se indique lo contrario, el contenido de este repositorio se distribuye únicamente como recurso técnico para el funcionamiento del proyecto.

Los derechos de cada imagen pertenecen a sus respectivos autores o titulares.
