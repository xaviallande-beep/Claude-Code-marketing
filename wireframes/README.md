# Wireframes · Task 15

Wireframes de la landing de Pleamar en dos versiones, escritorio y móvil, con las anotaciones de los principios de diseño de pantalla aplicados.

| Archivo | Qué es |
|---|---|
| `desktop.svg` | Wireframe de escritorio (1440 px, rejilla de 12 columnas). Se importa en Figma. |
| `mobile.svg` | Wireframe de móvil (390 px, rejilla de 4 columnas), con la barra fija de reserva aparte. Se importa en Figma. |
| `desktop.png`, `mobile.png` | Las mismas imágenes para verlas sin abrir Figma. |
| `reflection.md` | Borrador en inglés de la reflexión que pide la tarea. |

## Cómo pasarlos a Figma

1. Crea un archivo de diseño nuevo en Figma, con una página por persona del equipo (la tarea lo pide así).
2. Arrastra `desktop.svg` y `mobile.svg` al lienzo. Figma los convierte en capas que se pueden editar. Los textos usan la fuente Inter, que ya viene en Figma.
3. Cada sección es un grupo con nombre (`01 Header`, `02 Hero`…). La rejilla, la línea de pliegue y los números rojos están en capas aparte (`Layout grid`, `Fold line`, `Annotation markers`), así que puedes ocultarlas.
4. Para que cuente como trabajo hecho en Figma, rehaz lo básico con sus herramientas:
   - Pon cada versión dentro de un **Frame** con el tamaño de su plantilla (Desktop 1440 / iPhone 14).
   - Añade un **Layout grid**: 12 columnas, margen 120 y separación 24 en escritorio; 4 columnas, margen 16 y separación 16 en móvil.
   - Convierte los botones en un **componente** con dos **variantes** (principal y secundario) y úsalo en todos.
   - Agrupa los campos del formulario y las tarjetas con **Auto layout**.
   - En el modo **Prototype**, selecciona la barra de reserva del móvil y marca *Position: Fixed* para que se quede abajo al hacer scroll.
5. Repasa `reflection.md` y cámbialo para que cuente lo que hiciste tú de verdad.

## Qué cambia del escritorio al móvil

- El menú pasa a un botón de hamburguesa y "Reservar" se convierte en una barra fija abajo, donde llega el pulgar.
- Los botones ocupan todo el ancho y miden 52 px de alto.
- El parte del mar baja debajo de la portada.
- El curso más reservado aparece el primero y los otros dos se muestran resumidos.
- Los pasos de la clase pasan de una línea horizontal a una vertical.
- Las opiniones se convierten en un carrusel que se desliza con el dedo.
- Teléfono y WhatsApp pasan a ser botones: en el móvil se llama con un toque.
- El formulario va en una sola columna y las opciones de nivel son tarjetas grandes, fáciles de pulsar.
