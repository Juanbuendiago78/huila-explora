# Huila Explora

Sitio web demostrativo para promocionar destinos turísticos del departamento del Huila. Está construido con HTML5, Tailwind CSS 4 (CLI) y JavaScript vanilla.

## Requisitos

- Node.js 20 o superior (recomendado).
- npm, incluido con Node.js.
- Un navegador actualizado.

## Estructura

```text
huila-explora/
├── index.html
├── package.json
├── README.md
├── src/
│   ├── input.css
│   └── output.css
├── js/
│   └── script.js
└── images/
    └── README.md
```

## Instalación y ejecución

1. Abre una terminal dentro de la carpeta `huila-explora`.
2. Instala Tailwind CSS 4 y su CLI:

   ```bash
   npm install
   ```

3. Compila el CSS una vez:

   ```bash
   npm run build:css
   ```

4. Para desarrollar, deja la compilación observando cambios:

   ```bash
   npm run dev
   ```

5. Abre `index.html` en el navegador. También puedes usar la extensión Live Server de Visual Studio Code para recargar automáticamente los cambios HTML.

> `src/output.css` es un archivo generado. El comando `npm run build:css` lo reemplaza con el CSS compilado real de Tailwind. Ejecuta ese comando después de modificar `src/input.css` o las clases de `index.html`.

## Comandos disponibles

- `npm run build:css`: genera el CSS optimizado.
- `npm run dev`: mantiene Tailwind en modo observación y recompila al detectar cambios.

## Funcionalidades

- Navegación adaptable con menú hamburguesa en pantallas pequeñas.
- Alternancia entre tema claro y oscuro; la preferencia se guarda en `localStorage`.
- Tarjetas de destinos con enlaces que seleccionan el destino en el formulario.
- Acordeón de preguntas frecuentes: botones nativos navegables con Tab y activables con Enter o Espacio.
- Menú móvil: botón accesible con Tab, Enter y Espacio; enlaces recorribles con Tab; cierre con Escape.
- Selector de destino: control HTML nativo compatible con teclado y tecnologías de asistencia.
- Validación de campos obligatorios, correo electrónico, nombre y mensaje.
- Mensajes de error junto a cada campo y confirmación visual al validar.

## Nota sobre el formulario

El formulario es una demostración frontend: valida los datos en el navegador, pero **no envía correos ni guarda solicitudes**. Para recibir mensajes reales se necesita un backend o un servicio de formularios, además de definir cómo se protegerán y tratarán los datos personales.

## Imágenes y tipografías

Las imágenes de ejemplo se cargan desde URLs de Unsplash y las fuentes Poppins e Inter desde Google Fonts. Se requiere conexión a internet para visualizarlas. Puedes reemplazar las URLs por archivos propios dentro de `images/` y actualizar los atributos `src` del HTML.

## Prueba manual de teclado y diseño responsive

1. En computador, pulsa `Tab` desde el inicio y verifica que cada enlace y botón muestre un contorno visible.
2. Llega a cada pregunta frecuente con `Tab`; pulsa `Enter` o `Espacio` para abrirla o cerrarla.
3. En el formulario, enfoca el selector de destino con `Tab`; usa las flechas para cambiar de opción y confirma con `Enter` (el comportamiento de `Espacio` depende del navegador y del sistema operativo porque es un `<select>` nativo).
4. Activa la vista móvil desde las herramientas del navegador (ancho menor de 768 px). Enfoca el botón hamburguesa con `Tab`, ábrelo con `Enter` o `Espacio` y recorre sus enlaces con `Tab`. Cada enlace se activa con `Enter`.
5. Con el menú abierto, pulsa `Escape`: debe cerrarse y el foco debe volver al botón hamburguesa.
6. Repite la prueba en un teléfono real, tanto en orientación vertical como horizontal.

## Accesibilidad

Se incluyen etiquetas asociadas a los controles, textos alternativos, regiones de estado, atributo `aria-expanded`, enlace para saltar al contenido y estilos de foco visibles. Conviene verificar el contraste final y probar el sitio con teclado y lector de pantalla antes de publicarlo.
