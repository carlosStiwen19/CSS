# Proyecto Catálogo CSS - Modelo de Caja

Este repositorio contiene el desarrollo del **Momento 2: Misión de Apropiación** del programa de formación del SENA, enfocado en la aplicación estricta del modelo de caja tradicional y la estructuración semántica de interfaces web.

## Estructura del Proyecto
- **index.html**: Archivo principal con la maquetación semántica (`header`, `main`, `aside`, `footer`, `article`).
- **estilos.css**: Hoja de estilos con reglas tradicionales (`inline-block`, `box-sizing: border-box`, `padding`, `margin`).
- **img/**: Carpeta que almacena los recursos gráficos oficiales como el logo de la heladería.

---

## Hallazgos: El Modelo de Caja

1. **Diferencia práctica entre Margin y Padding:**
   - El **Padding** es el espacio de relleno interno que se ubica entre el contenido de un elemento y su borde, permitiendo que los textos o elementos internos no queden pegados a los límites de la caja.
   - El **Margin** es el margen exterior que separa de manera física a un elemento de los demás elementos hermanos que lo rodean en la pantalla, evitando colisiones visuales directas.

2. **Por qué es obligatorio usar `box-sizing: border-box`:**
   - Es fundamental porque le indica al navegador que incluya tanto el relleno (*padding*) como los bordes (*border*) dentro de las dimensiones totales de ancho y alto que se le hayan asignado al elemento. Esto evita que las cajas se desborden o se descuadren al sumarles tamaños adicionales.

3. **Cómo se ven afectados los elementos hermanos cuando le aplicas un margen grande a uno de ellos:**
   - Al aplicarle un margen exterior muy grande a un elemento en particular, este empuja de forma evidente a los elementos hermanos adyacentes o inferiores, alterando el flujo tradicional de la interfaz y pudiendo provocar saltos de línea no deseados en diseños basados en bloques o `inline-block`.
 
 Qué significa BEM (Block, Element, Modifier) y cómo se escribe visualmente.

Por qué dividir el CSS en varios archivos facilita el trabajo en equipo.

Cómo esta metodología evita la guerra de especificidad manteniendo un peso plano (valor 10). 

## Hallazgos: Arquitectura Total con Flexbox

1. **Control del pie de página con `min-height: 100vh` y `flex-direction: column`:** 
   Al convertir el contenedor global en una columna flexible con altura mínima del 100% del viewport y asignar `flex: 1` al contenedor central, se garantiza que el contenido principal ocupe todo el espacio vertical disponible, fijando el pie de página al fondo de la pantalla.

2. **Reemplazo de márgenes laterales mediante `gap`:** 
   La propiedad `gap` en contenedores flexibles como listas de navegación y paneles laterales permite definir un espaciado uniforme y predecible únicamente entre elementos hermanos, eliminando márgenes manuales.

3. **Tarjetas resistentes a distintas longitudes de texto:** 
   La combinación de un eje vertical (`flex-direction: column`) en la tarjeta y `flex-grow: 1` en la descripción permite que las tarjetas absorban textos largos manteniendo los botones y precios alineados de forma idéntica en la base.