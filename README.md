# Ludoteca · Juegos, estanterías y mesas del club

Programas para una asociación de juegos de mesa que comparten el mismo plano del local:

- **Catálogo de juegos** (`catalogo.html`): versión para los socios, solo consulta, pensada para el móvil. Lee los datos de la rama `datos` (los sube el editor conectado a GitHub) o, si no hay, `catalogo.json`.

- **Ludoteca, editor** (`ludoteca.html`): control de los juegos del club (de quién es cada uno y en qué estante y nivel está), con fotos de portada, etiquetas QR, estanterías sobre el plano y listados.
- **Distribuidor de Eventos** (`distribuidor_eventos.html`): reparto de mesas, sillas y personas en la sala para jornadas y torneos.

**Web:** https://eloiaa-hub.github.io/ludoteca/

Son archivos HTML de un solo fichero: funcionan sin instalar nada y sin internet (doble clic). Para que se pasen el plano, los dos tienen que estar **en la misma carpeta**.

## Contenido

| Archivo | Qué es |
|---|---|
| `index.html` | Página principal |
| `catalogo.html` | Catálogo de juegos para los socios (lectores) |
| `catalogo.json` | Datos del catálogo; lo genera el editor con «Publicar para lectores» y se sube aquí |
| `ludoteca.html` | Ludoteca (editor) v0.5 |
| `manual_ludoteca.html` / `.pdf` | Manual de la Ludoteca: instalación, uso y cómo está hecho |
| `distribuidor_eventos.html` | Distribuidor de Eventos v0.3 |
| `manual_distribuidor_eventos.html` / `.pdf` | Manual del Distribuidor de Eventos (v0.3) |
| `planos/AVALON-SALAS-COLORES.dxf` | Plano del local de la asociación (planta baja y altillo, en metros, zonas por colores) |
| `ejemplos/sala_prueba.dxf` | Un DXF sencillo para probar |

## Ludoteca

- **Juegos:** ficha de cada juego con foto de portada: juego, mínimo y máximo de jugadores, dueño (la Asociación o el socio que lo cede), condición, fecha de entrega al club, fecha de devolución al dueño, estante #, nivel y anotaciones, más editorial, duración, edad, categoría, idioma y lomo. Campos obligatorios y comprobaciones (máximo ≥ mínimo, devolución ≥ entrega). ID único y fechas de creación y de último cambio. Tabla editable como una hoja de cálculo, búsqueda, filtros por jugadores, duración, condición, estante, dueño y situación (en el club / devuelto).
- **Fotos de portada:** desde un archivo, la cámara del móvil, arrastrando la imagen o pegándola. Salen en la tabla, la ficha, los listados y el Excel.
- **Etiquetas QR** (21 por A4, 63 × 38 mm): al escanearlas se abre la ficha del juego en el catálogo, con su estante marcado en el plano.
- **☁️ Guardar en GitHub (v0.5, para pruebas):** varios editores sobre la misma ludoteca. Cada uno conecta en *Archivo* con su token (dueño: fine-grained, solo este repo, *Contents: Read and write*; colaboradores: classic con `public_repo`). Los cambios se suben solos como commits a la rama `datos` (`datos/ludoteca.json`, `datos/catalogo.json`, `datos/fotos/`), se juntan juego a juego si dos personas editan a la vez y el catálogo los lee directamente (hasta 5 min de caché). El token se queda en el navegador de cada uno.
- **Publicar para lectores:** genera `catalogo.json` (juegos en el club, miniaturas y plano). Se sube al repo con *Add file → Upload files* y el catálogo se actualiza en uno o dos minutos.
- **Excel (.xlsx) con fotos**, CSV y copia completa en `.json`. Importa CSV de Excel/LibreOffice o de BoardGameGeek.
- **Datos:** se guardan solos en la base de datos del navegador (IndexedDB), con una copia por día (30 días) y, en Chrome/Edge, también en un archivo `.json` vinculado de tu carpeta.
- **Plano y estanterías:** DXF del local, estanterías con largo, fondo, baldas, giro y zona de acceso delante; imán entre estanterías; ocupación de cada balda según el lomo de las cajas; arrastrar juegos a una estantería o balda; buscador «¿Dónde está…?».
- **Listados en PDF:** plano, inventario por estantería y nivel, juegos por dueño, catálogo alfabético y carteles de estantería.
- **Préstamos a socios (opcional):** ocultos por defecto; se activan en Archivo → Opciones.

## Instalación

No necesita servidor ni base de datos aparte. Descarga el repositorio (**Code → Download ZIP**), descomprímelo en una carpeta y abre `ludoteca.html` con doble clic en Chrome o Edge. En **💾 Archivo → 🔗 Vincular…** elige dónde guardar el `.json` de los datos. Los detalles, en el manual.

## Plano del club

Los dos programas llevan dentro el plano de **Avalon** (planta baja y altillo) y empiezan con él la primera vez. Las 6 zonas de color del plano son las zonas útiles. Para volver a ponerlo: **🏠 Plano del club**. El DXF original está en `planos/`.

## Plano compartido

Los dos programas trabajan en centímetros con el eje Y hacia arriba y leen el DXF igual (líneas, polilíneas, arcos, bloques y sombreados sólidos de color). Si el DXF dice unas unidades que no cuadran con su tamaño (por ejemplo, «mm» en un plano dibujado en metros), se corrigen solas y se avisa.

- 📚 **Ludoteca** (en el Distribuidor) y 🍽️ **Distribuidor de mesas** (en la Ludoteca) abren el otro programa con el mismo plano.
- Las estanterías y su zona de acceso pasan al Distribuidor como obstáculos para las mesas; las mesas pasan a la Ludoteca de referencia.
- También se puede traer el último trabajo del otro programa guardado en el navegador, o abrir su archivo `.json`.

## Licencia

Programas: [EUPL-1.2](https://eupl.eu/1.2/es/) · Manuales: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.es) · La Ludoteca incluye [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) de Kazuhiko Arase (MIT)

© 2026 Eloi A.A.
