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