# Guía de componentes (Auto Layout + Variantes)

Esta guía define la librería base para reconstruir las pantallas de los mockups.

## 1) App Bar / Top Bar
- Props:
  - `type`: CenterTitle | StartTitle
  - `leading`: None | Back | Menu
  - `trailing`: None | OneAction | TwoActions
  - `elevated`: true/false
- Estados: Default, Scrolled

## 2) Bottom Navigation
- Ítems: 3–5
- Props:
  - `label`: Shown | Hidden
  - `activeIndex`: 0..4

## 3) Buttons
- Variantes: Filled | Tonal | Outline | Text
- Tamaños: S (32) | M (40) | L (48)
- Icono: None | Leading | Trailing
- Estados: Default | Hover | Pressed | Disabled

## 4) Text Fields
- Variantes: Filled | Outline
- Estado: Default | Focused | Error | Disabled
- Props: HelperText on/off, Leading icon, Trailing icon, Password toggle

## 5) List Items / Cells
- Densidad: One-line | Two-line | Three-line
- Leading: None | Icon | Avatar | Image
- Trailing: None | Chevron | Meta | Switch

## 6) Cards
- Variantes: Base | WithMedia | Elevated | Outlined
- Props: Header (title + subtitle), Body, Actions

## 7) Chips
- Variantes: Filter | Assist | Input
- Estados: Selected | Unselected | Disabled
- Icon: on/off

## 8) Dialogs / Banners / Snackbars
- Dialog: Title + body + actions (Primary / Secondary)
- Snackbar: Leading icon opcional + action
- Banner: Informativo con CTA opcional

## 9) Avatars / Badges
- Avatar: 24 / 32 / 40 / 56
- Badge: Dot | Count

## Propiedades recomendadas
- Spacing: variables `space/*`
- Radius: variables `radius/*`
- Colors: `color/*` (semánticos), evitar hex directos
- Typography: `type/*` (styles) con Roboto

## Accesibilidad
- Contraste mínimo AA
- Touch target ≥ 44 px
- Estados focus visibles y coherentes.