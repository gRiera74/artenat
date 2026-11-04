# ArteNat: reglas del proyecto

- Web estática (HTML/CSS/JS) publicada con GitHub Pages desde `main`. Dominio en `CNAME`.
- Páginas: `index.html`, `presupuesto.html`, `gracias.html`.
- Estilos compartidos en `css/styles.css`, con variables en `:root` (colores, fuentes).
  Cada página tiene una clase en `<body>` (`page-home`, `page-budget`, `page-thanks`);
  los estilos específicos de una página van con ese prefijo.
- Las galerías de `index.html` salen de `galleriesData` (script de módulo en el `<head>`);
  las fotos están en `imagenes/`.
- Todo cambio debe ser responsive (móvil, tablet, escritorio).
- Para cambios estéticos, aplicar el menor impacto posible: primero CSS, luego HTML
  y solo si es imprescindible JS.
- No renombrar ni borrar imágenes, ni tocar `CNAME`, `robots.txt`, `sitemap.xml`
  ni `google6c8d366536190fae.html` sin avisarme.
- Mantener textos, enlaces y SEO (títulos, meta, JSON-LD, alt de imágenes)
  salvo que se pida lo contrario.
- No añadir librerías ni frameworks.
- Previsualización local con Live Server (127.0.0.1:5500).

## Decisiones de diseño (no revertir sin avisarme)

- Tipografía: Inter (texto) y Merriweather 700 (títulos y texto del logo), cargadas
  desde Google Fonts. Mantener las fuentes de reserva en `:root`.
- Color primario `#85664C` (elegido por contraste de accesibilidad). No volver a `#8C6D53`.
- En la cabecera de la home, el párrafo se parte en dos líneas en escritorio con
  `<br class="hero-break">` tras "patrimonio."; el salto se oculta por debajo de 820 px.
- En móvil, la cabecera de la home no es fija (`position: static`); en escritorio sí.
- Al añadir variantes de una clase base (por ejemplo `section.content-section`),
  tener en cuenta la especificidad: la regla de la variante debe ser igual o más específica.
- El botón de WhatsApp va fuera de `<main>`, antes del `<footer>`, igual en todas las páginas.

## Pendiente

- El logo SVG está repetido en las tres páginas; sacarlo a `imagenes/logo.svg`.
- Optimizar el peso de las imágenes de `imagenes/` (recomprimir sin cambiar nombres).