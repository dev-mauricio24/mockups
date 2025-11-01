# Importación y setup en Figma (Tokens + Componentes + Pantallas)

Este documento explica cómo importar los tokens, crear estilos en Figma y reconstruir las 13 pantallas usando componentes con Auto Layout.

## 1) Preparación del archivo Figma
- Crea un archivo con páginas:
  - 00 • Tokens
  - 01 • Componentes
  - 02 • Plantillas (Templates)
  - 03 • Pantallas (iOS)
  - 04 • Pantallas (Android)
- Tamaños base:
  - iOS: 390×844 (iPhone 15)
  - Android: 411×891 (Pixel 7)
- Grid y espaciado:
  - Grid base: 4/8 px
  - Gutter sugerido: 16 px en móviles
  - Margen lateral: 16 px

## 2) Importar tokens con Tokens Studio
1. Instala el plugin "Tokens Studio for Figma".
2. Abre la página "00 • Tokens".
3. En Tokens Studio, importa `tokens/design-tokens.json` (opción "Import").
4. Selecciona el tema "light" como activo.
5. Sincroniza variables a estilos:
   - Colores → Paint Styles
   - Tipografías → Text Styles
   - Sombras → Effect Styles
   - Radii/Stroke/Spacing → Variables (para usar en Auto Layout)

Nota: Colores provisionales; se ajustarán después de extraer la paleta real de los mockups. Tipografía: Roboto.

## 3) Crear componentes base con Auto Layout
En "01 • Componentes":
- Botones (Filled, Tonal, Outline, Text)
  - Estado: Default, Hover, Pressed, Disabled
  - Tamaño: S, M, L
  - Icono: Leading / Trailing / None
- App Bar / Top Bar
  - Con/sin botón back
  - Con/sin acción derecha
  - Título: Center / Start
- Bottom Navigation (hasta 5 ítems) con variante "Active item"
- Inputs (TextField)
  - Estado: Default, Focused, Error, Disabled
  - Con/sin helper
  - Leading/Trailing icon
- Cards / List Items
  - One-line / Two-line / Three-line
  - Leading: Avatar / Icon / None
  - Trailing: Meta / Switch / Chevron
- Chips: Filter, Assist, Input (con/sin icono)
- Banners / Snackbars / Dialogs
- Badges / Avatares / Empty states

Usa Auto Layout en todos los componentes (padding, gap, align) y constraints para que respondan a contenido variable.

## 4) Reconstrucción de pantallas
- Frames base:
  - iOS: 390×844 (Safe Areas: 44 top / 34 bottom)
  - Android: 411×891 (Status bar ~24dp; Navigation según variante)
- Coloca instancias de componentes y rellena con el contenido de cada mockup.
- Imágenes/ilustraciones: como "fills" en contenedores con relación de aspecto fija.

## 5) Ajustes finos tras análisis
- Paleta definitiva: se extrae de los mockups y se actualiza en `tokens/design-tokens.json`. Luego sincroniza de nuevo con Tokens Studio.
- Tipografía: Roboto (weights y tamaños equivalentes iOS/Android).
- Iconografía: Material Symbols / SF Symbols como base; vectorizaré logos/íconos propios.

## 6) Estructura y naming
- Tokens: `color/*`, `type/*`, `space/*`, `radius/*`, `shadow/*`, `stroke/*`
- Componentes: `Cmp/Button/*`, `Cmp/TextField/*`, `Cmp/List/*`, `Cmp/AppBar/*`, etc.
- Pantallas:
  - `SCR/Login`, `SCR/Registro`, `SCR/ResetPassword`, `SCR/InicioDenuncias`, `SCR/NuevaDenuncia`, `SCR/ReportDetail`, `SCR/ConfirmacionResumen`, `SCR/NotificacionesLista`, `SCR/PerfilVista`, `SCR/EditarPerfil`, `SCR/HelpSupport`, `SCR/AcercaInformacion`, `SCR/LogoutFlow`

## 7) Exportación de assets
- Iconos: SVG 24×24 / 20×20 (dp/pt equivalentes).
- Imágenes: @1x, @2x, @3x si se requiere para handoff.

## 8) Accesibilidad
- Contraste mínimo WCAG AA.
- Touch target ≥ 44 px.
- Estados focus/hover/pressed/disabled visibles.

---
Tras fijar paleta y densidades específicas, se actualizarán tokens y estilos automáticamente desde Tokens Studio.