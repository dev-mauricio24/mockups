# Guía de Importación de Tokens en Figma

Esta guía explica cómo importar y configurar los tokens de diseño del proyecto YoDenuncio en Figma.

## Prerequisitos

1. Cuenta de Figma (plan gratuito o superior)
2. Plugin "Tokens Studio for Figma" instalado
   - Instalar desde: https://www.figma.com/community/plugin/843461159747178978

## Estructura del Archivo Figma

Crear el archivo con las siguientes páginas en orden:

1. **00 • Tokens** - Documentación y muestras de tokens
2. **01 • Componentes** - Biblioteca de componentes base
3. **02 • Plantillas** - Plantillas y layouts reutilizables
4. **03 • Pantallas (iOS)** - Pantallas finales para iOS (390×844)
5. **04 • Pantallas (Android)** - Pantallas finales para Android (411×891)

## Pasos de Importación

### 1. Abrir Tokens Studio

1. En Figma, abrir el plugin: **Plugins → Tokens Studio for Figma**
2. En el panel del plugin, ir a la pestaña **Settings** (⚙️)

### 2. Importar Tokens

1. Click en **Import** o **Load from file**
2. Seleccionar el archivo: `tokens/design-tokens.json`
3. El plugin cargará todos los token sets: `global` y `light`

### 3. Activar el Tema Light

1. En la pestaña principal del plugin, buscar **Token Sets**
2. Activar los siguientes sets (checkboxes):
   - ✅ **global** - Tokens base (marca, tipografía, espaciado)
   - ✅ **light** - Tema de modo claro
3. Click en **Apply to document** o similar para generar los estilos en Figma

### 4. Verificar Estilos Generados

Después de aplicar, verificar en Figma que se hayan creado:

#### Colores (Color Styles)
- **Brand**: `brand/primary`, `brand/secondary`, `brand/accent`
- **Neutrales**: `neutral/50` a `neutral/900`
- **Light/Background**: `light/background/primary`, `secondary`, `tertiary`
- **Light/Text**: `light/text/primary`, `secondary`, `tertiary`
- **Light/Border**: `light/border/default`, `subtle`, `emphasis`
- **Light/Icon**: `light/icon/default`, `subtle`, `emphasis`
- **Light/Interactive**: `light/interactive/default`, `hover`, `active`, `disabled`
- **Light/Status**: `light/status/success`, `warning`, `error`, `info`

#### Tipografía (Text Styles)
- Familia de fuente: **Roboto**
- Tamaños: `xs` (12), `sm` (14), `base` (16), `lg` (18), `xl` (20), `2xl` (24), `3xl` (30), `4xl` (36)
- Pesos: `regular` (400), `medium` (500), `bold` (700)
- Line heights: `tight` (120%), `normal` (150%), `relaxed` (175%)

#### Efectos (Effects)
- **Sombras**: `shadow/sm`, `shadow/base`, `shadow/md`, `shadow/lg`, `shadow/xl`

#### Variables de Iconos
- **Tamaños**: `icon/size/xs` (16), `sm` (20), `base` (24), `lg` (32)
- **Stroke**: `icon/strokeWidth` (1.5)

### 5. Configurar Fuente Roboto

1. Asegurarse de que la fuente **Roboto** está disponible en Figma
2. Si no está disponible:
   - Ir a **Text → Font** en Figma
   - Buscar "Roboto" en Google Fonts
   - Activar en Figma: https://fonts.google.com/specimen/Roboto

## Uso de Tokens

### En Componentes
- Usar estilos generados en lugar de valores hardcodeados
- Ejemplo: aplicar `light/background/primary` para fondos
- Ejemplo: aplicar `light/text/primary` para texto principal

### En Auto Layout
- Usar tokens de spacing: `spacing/sm` (8), `spacing/md` (16), `spacing/lg` (24)
- Aplicar en padding, gap, y margins de Auto Layout

### En Iconos
- Tamaño por defecto: `icon/size/base` (24px)
- Stroke width: `icon/strokeWidth` (1.5px)
- Color: tokens de `light/icon/*`

## Sincronización

### Actualizar Tokens
Si se modifican los tokens en el archivo JSON:
1. En Tokens Studio, click en **Import** nuevamente
2. Seleccionar el archivo actualizado
3. Click en **Update** o **Apply**
4. Los estilos de Figma se actualizarán automáticamente

### Exportar Cambios
Si se ajustan tokens directamente en Figma:
1. En Tokens Studio, click en **Export**
2. Guardar como `design-tokens.json`
3. Reemplazar el archivo en el repositorio
4. Commit los cambios

## Próximos Pasos

1. ✅ Importar tokens siguiendo esta guía
2. 📖 Leer `guia-de-componentes.md` para construir componentes base
3. 🗺️ Consultar `mapeo-pantallas.md` para ensamblar las 13 pantallas
4. 🎨 Ver `iconography.md` para lineamientos de iconografía

## Recursos Adicionales

- Tokens Studio docs: https://docs.tokens.studio/
- Figma Auto Layout: https://help.figma.com/hc/en-us/articles/360040451373
- Google Fonts - Roboto: https://fonts.google.com/specimen/Roboto

## Notas

- Los colores son aproximados y se ajustarán mediante muestreo directo en Figma
- Para ajustes de color, ver: `tokens/brand-colors-notes.md`
- Soporte únicamente para modo claro en esta versión
