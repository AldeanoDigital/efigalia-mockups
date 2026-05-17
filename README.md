# Efigalia — Mockup navegable

Mockup interactivo de la futura **EfigaliApp** (Nuxt 4 + Supabase). Pensado para:

1. Validar UX del rediseño con el cliente final.
2. Validar las funcionalidades nuevas que no tenía la app HTML actual (dashboard de tareas, recepción con foto albarán + OCR de nº serie, vista de planificación por trabajo).
3. Compartir contexto visual con el colaborador externo.

## Cómo abrirlo

### En GitHub Pages (recomendado para enviar al cliente)

Una vez activado GitHub Pages en el repo: 🔗 https://aldeanodigital.github.io/efigalia-mockups/

### En local (sin instalar nada)

```bash
# Opción 1: abrir directamente en navegador
open index.html

# Opción 2: servidor local (recomendado para evitar issues con file://)
python3 -m http.server 8000
# luego visita http://localhost:8000
```

## Pantallas incluidas (8)

1. **Login** — full-screen
2. **Home admin** — cards completas + dashboard "Mis tareas" + resumen del día
3. **Home instalador** — cards filtradas + panel "Mi día" (cambia automáticamente al elegir rol "Instalador")
4. **Dashboard "Mis tareas"** — módulo nuevo: revisiones generadas por triggers al guardar visitas / puestas / mantenimientos
5. **Listado de partes diarios** — con filtros (obra, operario, fecha)
6. **Detalle/edición de un parte** — formulario completo con líneas, fotos, observaciones
7. **Recepción con foto albarán + nº serie** — funcionalidad nueva: OCR detecta nº serie del albarán, garantías heredadas
8. **Planificación semanal — vista por trabajo** — agrupa por tipo de actividad

Resto de módulos del menú lateral (Materiales, Visitas, Mantenimientos, Repostajes, KB, Cálculos, Administración) llevan a una pantalla "Próximamente" — están dentro del alcance fase 1 pero no se han mockupeado para mantener el demo enfocado.

## Truco: selector de rol en el header 👑🎯👷

Arriba a la derecha hay un selector de rol (Admin / Coordinador obra / Instalador). Cambiarlo:

- Modifica el avatar y nombre del usuario.
- Filtra los items del menú lateral según permisos.
- Cambia el contenido del home (admin ve cards completas + tareas; instalador ve "Mi día" con sus asignaciones).

Es el **truco más útil para el cliente**: puede experimentar la visibilidad por rol sin tener que loguearse de tres formas distintas.

## Qué NO es esto

- **No es código de producción**. Es HTML + Tailwind CDN + JS vanilla. La app real se hará en Nuxt 4.
- **No hay backend**. Todos los datos son fake (estáticos en el HTML).
- **No es fiel al pixel**. Es alta fidelidad visual pero los componentes finales serán de Nuxt UI, que tendrán pequeñas diferencias.
- **No es navegable al 100%**. Algunos botones no llevan a ningún sitio porque la pantalla destino no está en el mockup. Las 8 pantallas clave sí están enlazadas entre sí.

## Documentación de fondo

La doc completa del proyecto (PRD cerrado, matriz de visibilidad por rol, stack técnico, ADRs) vive en el repo hermano:

🔗 `AldeanoDigital/efigalia_docs` (privado, pedir acceso a Javier).

El [HANDOFF.md](https://github.com/AldeanoDigital/efigalia_docs/blob/main/HANDOFF.md) de ese repo es el punto único de entrada para entender el proyecto entero.

## Contacto

**Javier Rguez Fdez** (Aldeano Digital) — jrfsarria@gmail.com
