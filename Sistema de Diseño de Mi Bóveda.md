# 🎨 Sistema de Diseño de Mi Bóveda

Este documento es el registro central de todos los formatos personalizados. Sirve para mantener la consistencia visual y técnica en todas las notas.

## 🔤 Estilos de Texto (Inline - `<span>`)

| Vista Previa | Uso / Significado | Clase CSS | Template / Atajo |
| :--- | :--- | :--- | :--- |
| <span class="txt-concepto">Concepto Clave</span> | Definiciones, terminología técnica o ideas fundamentales. | `.txt-concepto` | Alt + C |
| <span class="txt-resaltado">Texto resaltado</span> | Para resaltar algún texto. | `.txt-resaltado` | Por definir |
| <span class="txt-negativo">Texto negativo</span> | Para destacar información negativa. | `.txt-negativo` | Por definir |
| <span class="txt-otros">Texto otros</span> | Texto para categoría otros. | `.txt-otros` | Por definir |
| <span class="txt-tamano-28">Texto 28px</span> | Texto grande sin convertirlo en título. | `.txt-tamano-28` | `Fmt - Tamaño 28` |
| <span class="txt-tamano-22">Texto 22px</span> | Texto mediano sin convertirlo en título. | `.txt-tamano-22` | `Fmt - Tamaño 22` |
| <span class="txt-tamano-18">Texto 18px</span> | Texto ligeramente más grande sin convertirlo en título. | `.txt-tamano-18` | `Fmt - Tamaño 18` |
| <span class="txt-tamano-14">Texto 14px</span> | Texto más compacto para contenido secundario. | `.txt-tamano-14` | `Fmt - Tamaño 14` |
| <span class="txt-tamano-12">Texto 12px</span> | Texto muy pequeño para notas de apoyo. | `.txt-tamano-12` | `Fmt - Tamaño 12` |

## 📚 Diccionario de Propiedades CSS (Referencia)

Usa estas variables dentro de tus llaves `{ ... }` en el archivo CSS para crear nuevos estilos.

### 1. El Color (`color` y `background-color`)

*   `color: #hex;` → Cambia el color de las letras.
    *   Ejemplos: `#ff0000` (rojo), `#5ccfe6` (celeste), `#98c379` (verde).
*   `background-color: #hex;` → Cambia el fondo del texto (resaltado).
    *   Tip: Usa `rgba(0,0,0,0.1)` para fondos semi-transparentes muy sutiles.

### 2. El Cuerpo (`font-weight` y `font-style`)

*   `font-weight: bold;` → Pone el texto en negrita.
*   `font-weight: normal;` → Quita la negrita (útil si el tema de Obsidian la pone por defecto).
*   `font-style: italic;` → Pone el texto en cursiva.
*   `font-style: normal;` → Texto derecho.

### 3. Decoraciones (`text-decoration` y `border`)

*   `text-decoration: underline;` → Subrayado simple.
*   `text-decoration: line-through;` → Texto tachado.
*   `border-bottom: 2px solid #hex;` → Crea un subrayado de color más grueso y personalizable que el estándar.

### 4. Ajustes de Espaciado (Para resaltados con fondo)

Si usas `background-color`, añade estos para que no se vea "apretado":

*   `padding: 0 4px;` → Añade un poco de aire a los lados del texto.
*   `border-radius: 4px;` → Redondea las esquinas del color de fondo.

## 🛠️ Especificaciones Técnicas

### 1. Archivo CSS (Snippets)

**Ruta:** `.obsidian/snippets/mis-estilos.css`

```css
.txt-concepto {
    color: #5ccfe6;
    font-weight: bold;
    font-style: italic;
}

.txt-resaltado {
    color: #ffd95a;
    font-weight: bold;
    text-decoration: underline;
}

.txt-negativo {
    color: #ff4d4d;
    font-weight: bold;
    font-style: italic;
}

.txt-otros {
    color: #ff69b4;
    font-weight: bold;
}

.txt-tamano-28 {
    font-size: 28px;
    font-weight: bold;
}

.txt-tamano-22 {
    font-size: 22px;
    font-weight: bold;
}

.txt-tamano-18 {
    font-size: 18px;
    font-weight: bold;
}

.txt-tamano-14 {
    font-size: 14px;
    font-weight: bold;
}

.txt-tamano-12 {
    font-size: 12px;
    font-weight: bold;
}
```

### 2. Dependencias de Software

*   **Plugin:** Templater
*   **Carpeta de Plantillas:** `Plantillas` (Ajustado a tu estructura actual)

## 📝 Instrucciones para agregar nuevos estilos

1.  **Definir:** Elegir función y nombre (ej. `.txt-duda`).
2.  **CSS:** Añadir la clase al archivo `.css` usando el Diccionario de Propiedades.
3.  **Template:** Crear nota en la carpeta de plantillas con `<span class="nombre-clase"><% tp.file.selection() %></span>`.
4.  **Hotkey:** Asignar atajo en Templater y Hotkeys de Obsidian.
5.  **Registrar:** Añadir la nueva fila a la tabla de arriba en este documento.
