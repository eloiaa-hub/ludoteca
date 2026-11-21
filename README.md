# Ludoteca · Juegos, estanterías y mesas del club

Dos programas para una asociación de juegos de mesa que comparten el mismo plano del local:

- **Ludoteca** (`ludoteca.html`): base de datos de los juegos, estanterías colocadas sobre el plano, préstamos y listados.
- **Distribuidor de Eventos** (`distribuidor_eventos.html`): reparto de mesas, sillas y personas en la sala para jornadas y torneos.

**Web:** https://eloiaa-hub.github.io/ludoteca/

Son archivos HTML de un solo fichero: funcionan sin instalar nada y sin internet (doble clic). Para que se pasen el plano, los dos tienen que estar **en la misma carpeta**.

## Contenido

| Archivo | Qué es |
|---|---|
| `index.html` | Página principal |
| `ludoteca.html` | Ludoteca v0.2 |
| `manual_ludoteca.html` / `.pdf` | Manual de la Ludoteca: instalación, uso y cómo está hecho |
| `distribuidor_eventos.html` | Distribuidor de Eventos v0.3 |
| `manual_distribuidor_eventos.html` / `.pdf` | Manual del Distribuidor de Eventos (v0.3) |
| `planos/AVALON-SALAS-COLORES.dxf` | Plano del local de la asociación (planta baja y altillo, en metros, zonas por colores) |
| `ejemplos/sala_prueba.dxf` | Un DXF sencillo para probar |

## Ludoteca

- **Juegos:** ficha de cada juego (juego, mínimo y máximo de jugadores, dueño, condición, estante #, nivel de estante, fecha de entrega, fecha de devolución y anotaciones, más editorial, duración, edad, categoría, idioma y lomo) con campos obligatorios y comprobaciones (máximo ≥ mínimo, devolución ≥ entrega). Cada juego tiene un ID único y fechas de creación y de último cambio. Tabla editable como una hoja de cálculo, búsqueda por nombre o dueño, filtros por jugadores, duración, condición, estante y disponibilidad. Importa CSV de Excel/LibreOffice o de BoardGameGeek y exporta CSV.
- **Datos:** se guardan solos en la base de datos del navegador (IndexedDB), con una copia por día (30 días) y, en Chrome/Edge, también en un archivo `.json` vinculado de tu carpeta. Copias `.json` y CSV cuando quieras.
- **Plano y estanterías:** DXF del local, estanterías con largo, fondo, baldas, giro y zona de acceso delante; imán entre estanterías; ocupación de cada balda según el lomo de las cajas; arrastrar juegos a una estantería o balda; buscador «¿Dónde está…?».
- **Préstamos:** fecha de entrega y de devolución prevista, avisos de retraso e historial con la fecha real.
- **Listados en PDF:** plano, inventario por estantería y balda, catálogo alfabético, préstamos y carteles de estantería.

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

Programas: [EUPL-1.2](https://eupl.eu/1.2/es/) · Manual: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.es)

© 2026 Eloi A.A.
