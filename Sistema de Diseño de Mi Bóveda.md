# 🎨 Sistema de Diseño de Mi Bóveda

Este documento es el registro central de todos los formatos personalizados. Sirve para mantener la consistencia visual y técnica en todas las notas.

## 🔤 Estilos de Texto (Inline - `<span>`)

| Vista Previa | Uso / Significado | Clase CSS | Template / Atajo |
| :--- | :--- | :--- | :--- |
| <span class="txt-concepto">Concepto Clave</span> | Definiciones, terminología técnica o ideas fundamentales. | `.txt-concepto` | Alt + C |

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
