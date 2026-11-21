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
| `ludoteca.html` | Ludoteca v0.1 |
| `distribuidor_eventos.html` | Distribuidor de Eventos v0.3 |
| `manual_distribuidor_eventos.html` / `.pdf` | Manual del Distribuidor (v0.2) |
| `planos/AVALON-SALAS-COLORES.dxf` | Plano del local de la asociación (planta baja y altillo, en metros, zonas por colores) |
| `ejemplos/sala_prueba.dxf` | Un DXF sencillo para probar |

## Ludoteca

- **Juegos:** tabla editable como una hoja de cálculo (código, título, editorial, jugadores, duración, edad, categoría, idioma, estado, propietario, estantería, balda, lomo, préstamo y notas). Filtros, orden por columnas, acciones sobre varios juegos. Importa CSV de Excel/LibreOffice o de BoardGameGeek y exporta CSV.
- **Plano y estanterías:** DXF del local, estanterías con largo, fondo, baldas, giro y zona de acceso delante; imán entre estanterías; ocupación de cada balda según el lomo de las cajas; arrastrar juegos a una estantería o balda; buscador «¿Dónde está…?».
- **Préstamos:** con plazo, avisos de retraso e historial.
- **Listados en PDF:** plano, inventario por estantería y balda, catálogo alfabético, préstamos y carteles de estantería.

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
