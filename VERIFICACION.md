# Verificación local — 7 de noviembre de 2026

## Completado

- `html-validate` 11.19.0: los documentos HTML pasaron sin errores ni advertencias (revisión del 7 de noviembre, antes de borrar las copias duplicadas). Hoy son 11: seis páginas principales y cinco detalles de vacante.
- `css-tree`: los cuatro archivos de `css/` pasan la revisión de sintaxis y propiedades, incluidos los descriptores `@font-face`.
- Cada documento tiene `lang="es"`, viewport, título, un `h1`, un `main`, encabezado, navegación y pie.
- Comprobación de IDs únicos, destinos locales y fragmentos: sin enlaces rotos.
- Campos asociados a etiquetas visibles mediante `for` e `id`.
- Todas las imágenes tienen `alt`; la ilustración decorativa usa `alt=""`.
- Sin atributos `style` ni bloques `<style>` en los HTML.
- Seis tarjetas de vacantes y tres solicitudes con estados distintos.
- Archivos de logo, ilustración y fuentes presentes y no vacíos. Logo de Figma: 1080 × 273px, presentado con la proporción del nodo de 300 × 75.833px. SVG de Figma: 264 × 88px; dimensiones nativas en escritorio y reducción proporcional en celular.
- No hay imágenes temporales de Figma ni fuentes remotas en el HTML/CSS final.
- Los formularios de registro y acceso omiten `name` en los controles que contienen datos personales o contraseñas, para impedir que la navegación estática los serialice en la URL. Se conserva la validación nativa con `required` y tipos apropiados.
- Se eliminaron las copias `registro_candidato.html` y `empresa_vacantes.html`, y los archivos `style.css` y `global.css`, para no tener código duplicado.

## Contraste calculado según luminancia relativa sRGB

| Texto | Fondo | Relación |
| --- | --- | --- |
| Azul `#202945` | Blanco | 14.34:1 |
| Azul | Coral `#ff815c` | 5.84:1 |
| Azul | Celeste `#cae4ef` | 10.83:1 |
| Azul | Pendiente `#ffdaa6` | 10.81:1 |
| Azul | Aceptada `#d9efdf` | 11.86:1 |
| Azul | Rechazada `#f8dce0` | 11.13:1 |
| Gris `#586079` (`--color-gris`) | Blanco | 6.24:1 |
| Azul | Coral hover `#f66c45` | 4.88:1 |
| Blanco | Azul hover `#334267` | 9.92:1 |

El foco utiliza contorno azul y una separación blanca para mantenerlo distinguible en los distintos fondos.

## Comprobado en Chromium el 8 de noviembre (script con Playwright)

- Sin desplazamiento horizontal a 320, 512, 720, 768, 1024 y 1440px en las seis páginas principales. 512, 720 y 384px equivalen a zoom 200 % desde 1024, 1440 y 768px.
- Todo el texto mide 18px o más; todos los botones y enlaces miden al menos 44px de alto.
- Contraste calculado sobre el color real de cada texto: ningún texto por debajo de 4.5:1 (3:1 en texto grande).
- Con Tab, cada elemento enfocable muestra contorno visible en las seis páginas.
- Sin IDs repetidos, enlaces ni anclas rotas, un solo h1 por página, títulos en orden, todos los campos con etiqueta y todas las imágenes con `alt`.
- Comparación visual con el Figma (escritorio): `index`, `login` y `mis-solicitudes` coinciden en colores, fuentes y estructura.
- En `mis-solicitudes.html`, Cancelar solo está activo en la solicitud Pendiente (RF-006).
- Botones `tel:` de AMAC (todas las páginas) y de la empresa (`vacante.html`) con números de ejemplo.

## Pendiente de comprobar en navegador

- Lighthouse Accessibility y su captura de puntuación.
- Validador W3C del servicio web. El validador local utilizado es `html-validate`; no equivale a una ejecución del servicio W3C.
- Recorrido manual con Shift+Tab y Enter, y zoom 200 % en el navegador real.

## Pendiente de información externa

- Teléfonos reales de AMAC y empresa para reemplazar los números de ejemplo.
- Términos y aviso de privacidad definitivos proporcionados por AMAC.
- Nombres y aportaciones del equipo, repositorio y URL de Vercel.
