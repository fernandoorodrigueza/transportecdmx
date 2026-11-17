# ¿Cuánto cuesta mover la CDMX?

Micrositio estático para GitHub Pages. Esta versión incorpora los datos dentro de `index.html`, así que no depende de que `data.js` se encuentre en una ruta separada.

## Archivos
- `index.html`: página, estilos, datos, interacciones y gráficas. Es el único archivo indispensable para publicar el sitio.
- `data.js`: copia independiente de los datos procesados, útil como respaldo y para futuras actualizaciones. La página no lo necesita para funcionar.
- `cuánto pierde el transporte público de la cdmx.xlsx`: libro original de trabajo; no es necesario subirlo para que funcionen las gráficas. Si lo haces, quedará públicamente accesible.

## Publicar o corregir en GitHub Pages
1. Descomprime el ZIP.
2. En el repositorio, reemplaza el `index.html` anterior por el nuevo.
3. Puedes subir también `data.js` como respaldo, pero no es requisito.
4. En **Settings → Pages**, verifica que la publicación use la rama `main` y la carpeta `/ (root)`.
5. Espera a que termine el despliegue y recarga la página publicada con `Ctrl + F5` para evitar la versión guardada en caché.

Las gráficas utilizan Chart.js desde CDN y las fuentes tipográficas se cargan desde Google Fonts. Si la red bloquea esos servicios externos, los datos y controles seguirán integrados, pero las gráficas o las fuentes pueden no mostrarse correctamente.

## Datos y metodología
- Periodo: 2020–2025.
- Sistemas: Metro, Metrobús, RTP y Transportes Eléctricos.
- Costo promedio por pasajero = gastos de funcionamiento / pasajeros transportados.
- Ingreso promedio por pasajero = ingreso reportado por el concepto disponible en cada hoja / pasajeros transportados.
- Brecha = costo promedio − ingreso promedio.
- Los valores por pasajero en pesos constantes de 2025 se recalcularon con los promedios anuales del INPC incluidos en el libro.
- Los ingresos, gastos, desahorro y déficit de las tablas financieras se presentan en pesos corrientes.
- No se descuentan accesos de cortesía del total de pasajeros.
- La brecha por pasajero no es el monto exacto del subsidio público. Los conceptos de ingreso tampoco son perfectamente homogéneos entre organismos.

## Fuentes de consulta
- Cuenta Pública CDMX: https://portal.infocdmx.org.mx/transparencia/cuenta-publica
- INEGI, ETUP: https://www.inegi.org.mx/programas/transporteurbano/
- INEGI, INPC: https://www.inegi.org.mx/programas/inpc/
