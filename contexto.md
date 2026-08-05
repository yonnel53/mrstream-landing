# Contexto del proyecto MrStream Landing

Este archivo reúne información central sobre los fondos, colores y dónde encontrar los assets del proyecto. Revisa este archivo antes de hacer cambios visuales importantes. Contiene además las indicaciones sobre el flujo de trabajo y pasos a seguir para mantener coherencia visual.

## Imágenes de fondo
- `fondo.webp` (raíz): imagen principal para escritorio. Archivo grande; se recomienda optimizar antes de producción.
- `fondo-mobile.webp` (raíz): versión pensada para móviles. Usada en media queries.

Recomendaciones:
- Para pruebas locales usa un servidor HTTP (`python3 -m http.server 8000`) y abre `http://localhost:8000`.
- Evitar `background-attachment: fixed` en iOS; el CSS actual ya incluye un workaround.
- Antes de reemplazar una imagen, crea una copia con nombre `fondo-NOMBRE-bck.webp` y verifica en `http://localhost:8000`.

## Paleta de colores
- Color principal (brand): #0a58ca (azul oscuro) — utilizado en botones y acentos.
- Fondo principal: gradientes y `fondo.webp` (imagen) — controlar contraste con texto blanco/negro.
- Texto principal: #111827 (casi negro)
- Texto secundario: #6b7280 (gris medio)

Nota: si se requiere actualizar la paleta, modificar `global.css` y documentar el cambio aquí antes de aplicar.

## Logos y favicons
- `MrS - Logo Original.png` (raíz o `images/`): logo principal; reemplaza las etiquetas `<h1>` con `<img>` cuando sea necesario.
- `icono.png` (raíz): favicon usado en los cuatro HTML. Rutas relativas ya ajustadas.

## Estructura y archivos clave
- `index.html` — landing principal.
- `laptops/index.html` — catálogo laptops.
- `laptops-gaming/index.html` — catálogo gaming.
- `monitores/index.html` — catálogo monitores.
- `global.css` — hojas de estilo globales (fondo, paleta, layout).

## Flujo de trabajo recomendado
1. Abrir y leer `contexto.md` (este archivo).
2. Ejecutar servidor local: `python3 -m http.server 8000`.
3. Probar cambios en `http://localhost:8000` en escritorio y móvil (o emulador).
4. Antes de editar `global.css` o imágenes de fondo, comentar en este archivo la intención y la ruta del nuevo asset.
5. Crear backup del asset original (por ejemplo `cp fondo.webp fondo.webp.bak`).

## Checklist antes de hacer cambios visuales
- [ ] Revisar `contexto.md`
- [ ] Confirmar rutas de assets
- [ ] Hacer backup de archivos a modificar
- [ ] Probar en servidor local
- [ ] Solicitar revisión si el cambio afecta la paleta o el fondo global

## Explicación previa a los cambios
Cualquier cambio propuesto deberá ser documentado aquí con una breve explicación de por qué se hace, los archivos a cambiar y el impacto esperado. Ejemplo de entrada:

```
Fecha: 2026-08-04
Autor: <tu nombre>
Cambio: reemplazo `fondo.webp` por `fondo-optimizado.webp`
Archivos: `global.css`, `index.html`, `laptops/index.html`, `laptops-gaming/index.html`, `monitores/index.html`
Impacto: imagen de fondo optimizada (menor peso), sin cambios en composición visual.
Pruebas: abrir `http://localhost:8000` en Chrome y Safari móvil.
```

---

Si estás de acuerdo, dime qué cambio quieres registrar primero y lo documentamos aquí antes de aplicarlo.
