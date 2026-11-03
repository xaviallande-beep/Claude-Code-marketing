# Pleamar Escuela de Surf (ejemplo)

Landing page de ejemplo para una escuela de surf ficticia en Somo (Cantabria). Es el primer proyecto hecho con Claude Code en este repositorio.

## Qué incluye

- **Portada** con un vídeo en bucle de la playa, el mensaje principal, botones de reserva y un "parte de hoy" con el estado del mar y la curva de la marea.
- **Cursos y precios** con tres opciones. La más reservada va destacada.
- **Cómo es una clase**, paso a paso y con horarios.
- **Opiniones** (textos de ejemplo).
- **Test "¿Qué Quely eres?"**: tres preguntas con barra de progreso. Al terminar sale el producto que te corresponde con una explosión de galletas, y se puede añadir a la cesta desde ahí.
- **Rasca la harina**: la foto del obrador está cubierta de harina. Al rascar con el ratón o el dedo (el cursor es una galleta) cae harina y aparece un código de descuento del 10 % (QUELY1853, de demostración) que se aplica a la cesta con un botón. También se puede descubrir sin rascar.
- **Minijuego "¡Atrapa las galletas!"**: se mueve un bol con el ratón, el dedo o las flechas del teclado. Quelita +1 punto, Quelito +3, y las galletas quemadas quitan una vida (hay 3). Cada vez caen más rápido y más quemadas. Guarda el récord en el navegador. Se pausa solo si dejas de verlo.
- **Preguntas frecuentes** desplegables.
- **Formulario de reserva**. Es una demostración: no envía datos a ningún sitio.

La página se adapta al móvil y cambia a colores oscuros si el dispositivo usa el modo oscuro.

## Animaciones

- **Portada en capas**: al bajar, el vídeo se desplaza más despacio que la página y el título algo más rápido.
- **Curva de la marea**: se dibuja sola al cargar la página.
- **Al bajar por la página**: los bloques suben suavemente al entrar en pantalla, las tarjetas de cursos y las opiniones llegan escalonadas, los pasos de la clase entran desde la izquierda y la línea de cada opinión se dibuja de izquierda a derecha.
- **Ola que rompe** antes de "Reserva tu plaza": al bajar, un mar de fondo crece hasta formar una ola, la cresta se curva en tubo y rompe en espuma y gotas. Se dibuja con JavaScript en un SVG, recalculando la forma según el scroll. Con "reducir movimiento" se queda quieta formando el tubo, y sin JavaScript se ve una ondulación suave.

Las demás animaciones de scroll usan CSS (`animation-timeline`), sin JavaScript. En navegadores que no lo soportan, la página se ve completa y sin animar. Si el dispositivo tiene activado "reducir movimiento", no hay ninguna animación y la portada muestra la foto fija en lugar del vídeo.

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

---

# Quely · Cookies from Mallorca (carpeta `quely/`)

Web de una sola página hecha a partir del wireframe "MacBook Air" de Figma. Abre `quely/index.html` con doble clic: no hace falta instalar nada. La carpeta `quely/img/` tiene que estar junto al archivo para que se vean las fotos.

## Secciones

Portada · franja animada · Sobre nosotros · La isla · Productos · Test "¿Qué Quely eres?" · Opiniones · Rasca la harina · Minijuego · Preguntas frecuentes · Contacto · Pie.

## Qué se puede hacer

- **Español / inglés**: botón EN/ES en el menú. La primera vez elige el idioma del navegador y luego recuerda la elección.
- **Ficha de producto**: "Ver producto" (o clic en la tarjeta) abre una ficha con descripción, precio y cantidad.
- **Cesta**: "Comprar online", "Ver todos los productos", "Cajas regalo" y "Ofertas" abren la cesta. Al añadir algo, una galleta vuela hasta el botón y sube el contador. Se pueden cambiar cantidades, quitar productos y añadir más desde la propia cesta. Se guarda en el navegador aunque cierres la página.
- **Formulario de contacto**: comprueba que el nombre, el email y el mensaje estén bien antes de enviar.
- **Test "¿Qué Quely eres?"**: tres preguntas con barra de progreso. Al terminar sale el producto que te corresponde con una explosión de galletas, y se puede añadir a la cesta desde ahí.
- **Rasca la harina**: la foto del obrador está cubierta de harina. Al rascar con el ratón o el dedo (el cursor es una galleta) cae harina y aparece un código de descuento del 10 % (QUELY1853, de demostración) que se aplica a la cesta con un botón. También se puede descubrir sin rascar.
- **Minijuego "¡Atrapa las galletas!"**: se mueve un bol con el ratón, el dedo o las flechas del teclado. Quelita +1 punto, Quelito +3, y las galletas quemadas quitan una vida (hay 3). Cada vez caen más rápido y más quemadas. Guarda el récord en el navegador. Se pausa solo si dejas de verlo.
- **Preguntas frecuentes** desplegables. "Envíos" y "Devoluciones" del pie abren la pregunta que toca.

## Animaciones

- **Galletas que se pueden morder** en la portada: se apartan al pasar el ratón; tres mordiscos y se deshacen en migas, con sonido de crujido (se puede silenciar) y un contador.
- **Franja roja** que acelera y cambia de sentido según cómo bajas.
- **Horno interactivo**: al pulsar "Encender el horno" sube la temperatura y corre el tiempo. Las galletas pasan de masa cruda (brillante, irregular y con burbujas) a hinchadas, redondas y doradas. Un medidor muestra si van crudas, perfectas o quemadas, y el botón se pone verde y late cuando están en su punto. Si te pasas, se oscurecen y echan humo. Al sacarlas sale el resultado, y se cuentan las tandas perfectas. Las de los bordes de la bandeja se hacen un poco antes que las del centro.
- **Cifras** que cuentan solas, **tarjetas en 3D** que siguen al ratón y **galleta "volver arriba"** que se va comiendo según lees.
- **Logo gigante** del pie que se llena de rojo.
- **La isla**: una ilustración de Mallorca a todo el ancho, con mar, barcos, olivos que se mueven con el viento y un molino que gira más rápido si lo pulsas. El sol es una galleta gigante que se va poniendo detrás de las montañas según bajas.
- **Retratos ilustrados** en las opiniones (parpadean de vez en cuando) e **iconos dibujados** en "Nuestra historia".

Con "reducir movimiento" activado en el dispositivo, todo se ve completo y sin animar.

## Para publicarla de verdad

Al principio del código JavaScript de `quely/index.html` (busca `Shop settings`) hay tres cosas por rellenar:

| Qué | Para qué | Mientras esté vacío |
|---|---|---|
| `PRODUCTS` (precios) | Los precios que se muestran: **ahora son de ejemplo** (2,50 €, 2,95 € y 1,95 €). | Se ven los de ejemplo. |
| `SHOP_URL` | Dirección de la tienda online a la que lleva "Finalizar compra". | Sale un aviso de "modo demo" y no se hace ningún pedido. |
| `FORM_ENDPOINT` | Dirección que recibe los mensajes del formulario (por ejemplo, un formulario gratuito de [Formspree](https://formspree.io)). | Sale "modo demo" y el mensaje no se envía. |

Además:

- Las **opiniones** son los textos de ejemplo del wireframe: hay que cambiarlas por opiniones reales.
- Las **fotos de los productos** (`img/quelitas.webp`, `img/quelitos.webp`, `img/merienda.webp`) son las que se pasaron, con el fondo blanco quitado. La del obrador (`img/obrador.webp`) está ampliada al doble porque la original era pequeña.
- El resto de imágenes (galletas, paisaje, retratos e iconos) están **dibujadas con código**.
- Todos los textos están juntos en el código (busca `const I18N`), en inglés y en español, para cambiarlos fácilmente.
