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
