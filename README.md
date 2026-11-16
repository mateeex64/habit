# Habit — primera versión

Aplicación personal de seguimiento de hábitos (PWA).

## Incluye
- Crear y editar hábitos.
- Categorías y filtros.
- Marcar hábitos completados por día.
- Progreso diario, rachas y resumen mensual.
- Vista de la última semana.
- Guardado local en el navegador (`localStorage`), sin cuenta.

## Cómo probarla
1. Descomprimí el ZIP.
2. Abrí `index.html` en un navegador para probar las funciones básicas.
3. Para instalarla como PWA y habilitar el modo sin conexión, los archivos deben servirse desde un sitio HTTPS (por ejemplo, un hosting estático gratuito). Abrir el archivo directamente no habilita el service worker ni la instalación PWA.

## Privacidad y límites de esta versión
Los datos permanecen en el almacenamiento local del navegador/dispositivo. Si borrás los datos del sitio o cambiás de navegador/dispositivo, podés perderlos. Todavía no hay sincronización ni copia de seguridad/exportación.

## Próximos pasos recomendados
- Exportar/importar una copia de seguridad.
- Elegir días de la semana para cada hábito.
- Recordatorios.
- Historial mensual más detallado.
- Publicación en hosting estático HTTPS para instalarla en Android y PC.

## Actualización v1.1
- Exportación e importación de copias JSON desde el botón "Copia de seguridad".
- Selección de días de la semana para cada hábito.
- Calendario mensual navegable con indicador de días completados y resumen del día seleccionado.
- Al importar, la copia reemplaza los datos actuales previa confirmación.

## Actualización v1.2
- Gráfico de los últimos 30 días (porcentaje de hábitos programados cumplidos por día; tocá una barra para ver el detalle).
- Rachas corregidas: tanto la racha global como la de cada hábito saltean los días en que no estaban programados, y un día de hoy todavía sin completar no corta la racha.
- "Este mes", progreso de hoy y categorías cuentan solo hábitos programados.
- Estadísticas mensuales para el mes elegido en el calendario: cumplimiento, completados, días perfectos, comparación con el mes anterior y ranking por hábito.
- Recordatorios: resumen diario con hora configurable y hora opcional por hábito (botón "Recordatorios"). Se envían con la app abierta o en segundo plano; sin servidor no se puede garantizar el aviso con la app totalmente cerrada.
- Las copias de seguridad ahora incluyen la configuración de recordatorios (las copias anteriores siguen siendo compatibles).
- El service worker busca primero la versión nueva, así las actualizaciones llegan sin borrar la caché.

## Instalar en el celular (Android)
1. Subí esta carpeta a un hosting estático HTTPS (GitHub Pages, Netlify o Cloudflare Pages).
2. Abrí el link en Chrome del celular.
3. Menú ⋮ → "Instalar app" (o "Añadir a la pantalla de inicio").
4. Abrí Habit desde el ícono: se ve a pantalla completa y funciona sin conexión. Para recibir recordatorios, activá "Recordatorios" dentro de la app y aceptá el permiso.

## Actualización v1.3
- Rediseño: negro cálido con acento dorado, títulos en serif y barra inferior con cuatro secciones (Hoy, Progreso, Calendario, Ajustes), en lugar de una sola pantalla larga.
- Frase motivacional del día en la pantalla Hoy y una frase al completar cada hábito. Cada hábito puede tener su frase propia (se edita con "···"); si no, Habit elige una distinta cada día.
- Nuevo logo: emblema con el 24.
- Se pueden eliminar hábitos (doble toque en "Eliminar" dentro de la edición).
- Se pueden marcar o corregir días pasados desde Calendario.
- Cada hábito guarda su fecha de inicio: un hábito nuevo ya no baja los porcentajes de días anteriores. Los hábitos existentes toman como inicio su primer día con registros.
- Los filtros por categoría solo aparecen si hay más de una categoría en uso.
- Recordatorios y copia de seguridad pasaron a la sección Ajustes.
- Las copias de versiones anteriores se pueden importar sin problemas.

## Cómo actualizar la app publicada
Entrá al repositorio en github.com, tocá Add file → Upload files, subí todos los archivos de esta carpeta (reemplazan a los viejos) y confirmá con Commit changes. En uno o dos minutos la app se actualiza; si no se ve, cerrala por completo y volvé a abrirla.
