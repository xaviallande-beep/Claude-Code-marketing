# Pleamar Escuela de Surf (ejemplo)

Landing page de ejemplo para una escuela de surf ficticia en Somo (Cantabria). Es el primer proyecto hecho con Claude Code en este repositorio.

## Qué incluye

- **Portada** con un vídeo en bucle de la playa, el mensaje principal, botones de reserva y un "parte de hoy" con el estado del mar y la curva de la marea.
- **Cursos y precios** con tres opciones. La más reservada va destacada.
- **Cómo es una clase**, paso a paso y con horarios.
- **Opiniones** (textos de ejemplo).
- **Preguntas frecuentes** desplegables.
- **Formulario de reserva**. Es una demostración: no envía datos a ningún sitio.

La página se adapta al móvil y cambia a colores oscuros si el dispositivo usa el modo oscuro.

## Animaciones

- **Portada en capas**: al bajar, el vídeo se desplaza más despacio que la página y el título algo más rápido.
- **Curva de la marea**: se dibuja sola al cargar la página.
- **Al bajar por la página**: los bloques suben suavemente al entrar en pantalla, las tarjetas de cursos y las opiniones llegan escalonadas, los pasos de la clase entran desde la izquierda y la línea de cada opinión se dibuja de izquierda a derecha.

Las animaciones de scroll usan CSS (`animation-timeline`), sin JavaScript. En navegadores que no lo soportan, la página se ve completa y sin animar. Si el dispositivo tiene activado "reducir movimiento", no hay ninguna animación y la portada muestra la foto fija en lugar del vídeo.

## Imagen y vídeo de portada

Generados con [Higgsfield](https://higgsfield.ai):

1. **Imagen**: modelo Z Image, a partir de una descripción de texto (0,15 créditos).
2. **Vídeo**: modelo Minimax Hailuo 2.3 Fast, animando esa imagen (4 créditos, 6 segundos).
3. **Preparación para la web**: el vídeo se ha recortado a 4,9 segundos con un fundido cruzado entre el final y el principio, para que el bucle no dé saltos. Se ha quitado el audio y se ha comprimido de 1,6 MB a 775 KB. La imagen está en dos tamaños (1920 y 960 px) para que el móvil descargue la pequeña.

## Cómo verla

Descarga el proyecto (botón **Code → Download ZIP** en GitHub), descomprímelo y abre `index.html` con doble clic en cualquier navegador. No hace falta instalar nada.

## Archivos

| Archivo      | Qué es                                                  |
|--------------|---------------------------------------------------------|
| `index.html` | Toda la página: el contenido, el diseño (CSS) y el formulario (JavaScript). |
| `img/portada.mp4` | Vídeo en bucle de la portada. |
| `img/portada.jpg`, `img/portada-960.jpg` | Foto de la portada, que se ve mientras carga el vídeo o si no se puede reproducir. |
| `README.md`  | Este archivo.                                           |
