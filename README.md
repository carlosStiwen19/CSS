# 🚀 Taller de Maquetación Semántica y Leyes de CSS

Repositorio de práctica individual desarrollado para el programa de formación en desarrollo de software, enfocado en la estructuración semántica con HTML5 y la comprensión profunda de la cascada, herencia y especificidad en CSS.

---

## 📊 Tabla de Puntos de Especificidad

Para resolver colisiones visuales de manera predecible y sin recurrir jamás a la mala práctica del `!important`, el proyecto implementa la jerarquía de selectores estándar:

| Tipo de Selector | Ejemplo en Código | Puntuación | Descripción del Peso |
| :--- | :--- | :---: | :--- |
| **Etiqueta (Tag)** | `header`, `p`, `article` | **1 pt** | Selector base de menor especificidad. |
| **Clase (Class)** | `.btn-comprar` | **10 pts** | Selector reutilizable de peso medio. |
| **ID (Identificador)** | `#btn-destacado` | **100 pts** | Selector único de máximo peso (aplasta clases y etiquetas). |

---

## 🛠️ Estructura y Características Técnicas

- **Maquetado Semántico Estricto:** Uso riguroso de bloques semánticos obligatorios (`<header>`, `<nav>`, `<main>`, `<aside>`, `<section>`, `<article>` y `<footer>`).
- **Herencia Global:** Declaración de la tipografía base y color de texto heredable desde la etiqueta `body`.
- **Selectores Combinados por Zonas:** Aislamiento de estilos (`header nav ul li a`, `aside ul li a`, `footer ul li a`) para evitar sobreescrituras accidentales entre menús.
- **Demostración de Cascada vs Especificidad:** Conflicto controlado donde `#btn-destacado` (100 pts) prevalece sobre `.btn-comprar` (10 pts) en el producto principal.

---

## 📦 Control de Versiones y Despliegue
- **Rama de Trabajo:** `develop`
- **Metodología de Commits:** Convventional Commits (`feat(styles): maquetar catalogo semantico y aplicar jerarquia CSS`)
## Hallazgos: El Modelo de Caja

1. **Diferencia práctica entre Margin y Padding:**
   El `padding` es el espacio de relleno interno que se encuentra entre el contenido de la caja y su borde (expande el área interior). Por su parte, el `margin` es el espacio de separación exterior que aleja a la caja de los demás elementos circundantes, evitando que colisionen visualmente.

2. **Por qué es obligatorio usar `box-sizing: border-box`:**
   Es indispensable porque cambia la forma en que el navegador calcula el ancho y alto total de los elementos. Al activarlo, los rellenos (`padding`) y los bordes (`border`) se suman hacia adentro del tamaño declarado, evitando que la caja ensanche de más y rompa la estructura del contenedor padre.

3. **Efecto en los elementos hermanos al aplicar un margen grande:**
   Cuando a un elemento se le asigna un margen exterior muy grande, empuja de manera directa a los elementos hermanos adyacentes, generando mayor distancia visual o forzándolos a bajar de línea (en comportamientos de bloque o `inline-block`) debido al espacio físico que ahora ocupa ese margen.