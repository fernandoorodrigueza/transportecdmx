# ¿Cuánto cuesta mover la CDMX?

Micrositio estático para GitHub Pages, construido a partir del archivo de trabajo `cuánto pierde el transporte público de la cdmx.xlsx`.

## Archivos
- `index.html`: interfaz, estilos, gráficas e interacciones.
- `data.js`: datos procesados del libro de Excel.

## Publicar en GitHub Pages
1. Crea un repositorio nuevo en GitHub.
2. Sube `index.html` y `data.js` a la raíz del repositorio.
3. Abre **Settings → Pages**.
4. En **Build and deployment**, selecciona **Deploy from a branch**.
5. Elige la rama `main` y la carpeta `/ (root)`, y guarda.
6. Espera a que GitHub Pages publique la dirección del sitio.

No requiere Node, compilación ni backend. Las gráficas usan Chart.js desde CDN y las fuentes tipográficas se cargan desde Google Fonts. Para una versión completamente autónoma habría que descargar esas dependencias y servirlas localmente.

## Datos y metodología
- Periodo: 2020–2025.
- Sistemas: Metro, Metrobús, RTP y Transportes Eléctricos (trolebuses, Tren Ligero y Cablebús, según la agrupación del archivo).
- Costo promedio por pasajero = gastos de funcionamiento / pasajeros transportados.
- Ingreso promedio por pasajero = ingreso reportado por el concepto disponible en cada hoja / pasajeros transportados.
- Brecha = costo promedio − ingreso promedio.
- Los valores por pasajero en pesos constantes de 2025 se recalcularon con los promedios anuales del INPC de la hoja `inpc`: valor real = valor nominal × (INPC promedio anual 2025 / INPC promedio anual del año observado).
- Los ingresos, gastos, desahorro y déficit de las tablas financieras se presentan en pesos corrientes, sin deflactar.
- No se descuentan accesos de cortesía del total de pasajeros.
- La brecha por pasajero no es el monto exacto del subsidio público. Los conceptos de ingreso reportados tampoco son perfectamente homogéneos entre organismos.

## Fuentes oficiales de consulta
- Cuenta Pública CDMX: https://portal.infocdmx.org.mx/transparencia/cuenta-publica
- INEGI, ETUP: https://www.inegi.org.mx/programas/transporteurbano/
- INEGI, INPC: https://www.inegi.org.mx/programas/inpc/

## Antes de publicar
Revisar los documentos fuente de cada organismo y documentar el nombre exacto del estado financiero y de los rubros de gasto utilizados en cada año. También conviene validar si se deben restar los accesos de cortesía del Metro y homogeneizar el concepto de ingreso por pasajero entre los cuatro sistemas.
