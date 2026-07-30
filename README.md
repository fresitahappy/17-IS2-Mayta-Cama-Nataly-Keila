# Préstamos de equipos — Ingeniería de Software II

**Estudiante:** Mayta Cama Nataly Keila
**Código:** 227221
**Curso:** EST323 — Ingeniería de Software II
**Docente:** Tisnado Puma Julio César
**Ficha asignada:** N° 17 — Filtro por categoría

Miniaplicación estática para la actividad individual de aseguramiento de calidad de software. No usa base de datos ni servidor, guarda los registros en el navegador mediante `localStorage`.

## Funcionalidad inicial

- Registra un préstamo de un equipo disponible.
- Evita registrar datos incompletos, una fecha de devolución anterior a la fecha de préstamo y el préstamo simultáneo del mismo equipo.
- Muestra los préstamos y permite registrar la devolución.
- Conserva los datos del navegador mientras no se restablezcan desde la aplicación.

## Mejora implementada (Ficha 17)

Se agregó un selector **"Filtrar por categoría"** sobre la tabla de préstamos. Al elegir una categoría (Cómputo, Audiovisual, Redes o Laboratorio), la tabla muestra solo los préstamos de equipos que pertenecen a esa categoría. Si no hay préstamos en la categoría elegida, se muestra un mensaje de estado vacío. También se añadió una columna **"Categoría"** en la tabla para verificar el filtro a simple vista.

**Criterios de aceptación:**
- La categoría elegida muestra solo sus equipos.
- Una categoría sin registros muestra el estado vacío.

## Inicio rápido

1. Copie esta carpeta a su repositorio individual o use el repositorio base como plantilla.
2. Abra `index.html` en el navegador para probarla localmente.
3. Registre uno o más préstamos usando el formulario.
4. Use el selector "Filtrar por categoría" sobre la tabla para ver solo los préstamos de una categoría.
5. Publique la aplicación en GitHub Pages y proporcione los enlaces solicitados.

## Archivos principales

- `index.html`: estructura y controles de la aplicación, incluye el selector de filtro.
- `style.css`: diseño visual, incluye el estilo de la barra de filtro.
- `app.js`: catálogo, registros, validaciones, almacenamiento local y lógica del filtro por categoría.

## Casos de prueba de mi mejora

| Caso | Datos de entrada / acción | Resultado esperado | Resultado obtenido | Estado |
|---|---|---|---|---|
| CP-01: caso válido | Registrar préstamos de "Proyector Epson" y "Router TP-Link", luego elegir la categoría "Audiovisual" en el filtro. | La tabla muestra solo el préstamo del Proyector Epson (categoría Audiovisual). | Se mostró únicamente "Proyector Epson — Audiovisual". El préstamo del Router TP-Link no apareció. | Aprobado |
| CP-02: caso límite/inválido | Elegir la categoría "Laboratorio" sin tener préstamos registrados en ella. | Se muestra el mensaje de estado vacío, sin filas en la tabla. | Apareció el mensaje "No hay préstamos registrados en la categoría 'Laboratorio'." y la tabla quedó sin filas. | Aprobado |

## Entrega

- **URL del repositorio individual:** 
- **URL pública de GitHub Pages:** 
- README actualizado con los dos casos de prueba. 
