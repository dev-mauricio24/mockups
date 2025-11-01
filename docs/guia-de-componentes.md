# Guía de Componentes - YoDenuncio

Esta guía define los componentes base del sistema de diseño YoDenuncio, sus variantes y cómo construirlos en Figma usando Auto Layout y los tokens importados.

## Principios de Diseño

- **Auto Layout First**: Todos los componentes deben usar Auto Layout para ser responsive
- **Token-Based**: Usar tokens de diseño en lugar de valores fijos
- **Variantes**: Crear variantes para estados y contextos diferentes
- **Reutilizable**: Diseñar para máxima reutilización

## Componentes Base

### 1. Buttons (Botones)

**Variantes**:
- **Type**: Primary, Secondary, Tertiary, Ghost
- **State**: Default, Hover, Active, Disabled
- **Size**: Small, Medium, Large

**Especificaciones**:
```
Primary Button:
- Background: {light/interactive/default}
- Text: {light/text/onPrimary}
- Border Radius: {borderRadius/md} (8px)
- Padding: {spacing/sm} {spacing/md} (8px 16px)
- Font: Roboto Medium, {fontSize/base} (16px)
- Height: 40px (Small), 48px (Medium), 56px (Large)

Secondary Button:
- Background: transparent
- Border: 1px {light/interactive/default}
- Text: {light/interactive/default}

Tertiary Button:
- Background: {light/background/secondary}
- Text: {light/text/primary}

Ghost Button:
- Background: transparent
- Text: {light/interactive/default}
- No border
```

**Auto Layout**:
- Direction: Horizontal
- Gap: {spacing/sm} (8px) entre icono y texto
- Padding horizontal: {spacing/md} (16px)
- Padding vertical: {spacing/sm} (8px)
- Hug contents

### 2. Input Fields (Campos de Entrada)

**Variantes**:
- **State**: Default, Focus, Error, Disabled
- **Size**: Medium, Large
- **Type**: Text, Password, Email, Number

**Especificaciones**:
```
Text Input:
- Background: {light/background/tertiary}
- Border: 1px {light/border/default}
- Border Radius: {borderRadius/md} (8px)
- Padding: {spacing/sm} {spacing/md} (8px 16px)
- Font: Roboto Regular, {fontSize/base} (16px)
- Height: 40px (Medium), 48px (Large)

Focus State:
- Border: 2px {light/interactive/default}

Error State:
- Border: 1px {light/status/error}
- Helper text color: {light/status/error}
```

**Auto Layout**:
- Container: Vertical
- Gap: {spacing/xs} (4px)
- Componentes: Label, Input Field, Helper Text

### 3. Cards (Tarjetas)

**Variantes**:
- **Elevation**: Flat, Raised
- **Type**: Basic, Interactive

**Especificaciones**:
```
Card:
- Background: {light/background/tertiary}
- Border Radius: {borderRadius/lg} (12px)
- Padding: {spacing/md} (16px)
- Shadow (Raised): {shadow/md}

Interactive Card:
- Hover: {shadow/lg}
- Cursor: pointer
```

**Auto Layout**:
- Direction: Vertical
- Gap: {spacing/md} (16px)
- Fill container width
- Hug contents height

### 4. Navigation Bar (Barra de Navegación)

**Variantes**:
- **Platform**: iOS, Android
- **Type**: Top Bar, Bottom Tab Bar

**Especificaciones**:
```
Top Navigation Bar:
- Background: {light/background/tertiary}
- Height: 56px (Android), 44px (iOS)
- Padding: {spacing/sm} {spacing/md}
- Shadow: {shadow/sm}

Bottom Tab Bar:
- Background: {light/background/tertiary}
- Height: 56px (Android), 49px (iOS + safe area)
- Items: 3-5 tabs
- Active color: {light/interactive/default}
- Inactive color: {light/icon/subtle}
```

**Auto Layout**:
- Direction: Horizontal
- Distribution: Space between
- Padding: {spacing/md}

### 5. List Items (Elementos de Lista)

**Variantes**:
- **Type**: Single Line, Two Line, Three Line
- **Leading**: None, Icon, Avatar, Checkbox
- **Trailing**: None, Icon, Text, Switch

**Especificaciones**:
```
List Item:
- Height: 56px (Single), 72px (Two line), 88px (Three line)
- Padding: {spacing/md} (16px)
- Divider: 1px {light/border/subtle}

Leading Icon:
- Size: {icon/size/base} (24px)
- Margin right: {spacing/md}

Trailing Icon:
- Size: {icon/size/sm} (20px)
- Margin left: {spacing/sm}
```

**Auto Layout**:
- Direction: Horizontal
- Align: Center
- Gap: {spacing/md}
- Fill container

### 6. Chips/Tags

**Variantes**:
- **Type**: Default, Outlined, Status
- **State**: Default, Selected
- **Size**: Small, Medium

**Especificaciones**:
```
Chip:
- Background: {light/background/secondary}
- Border Radius: {borderRadius/full}
- Padding: {spacing/xs} {spacing/sm} (4px 8px)
- Font: Roboto Medium, {fontSize/sm} (14px)
- Height: 24px (Small), 32px (Medium)

Selected:
- Background: {light/interactive/default}
- Text: {light/text/onPrimary}
```

### 7. Icons (Iconos)

**Especificaciones**:
- **Set**: Lucide Icons
- **Stroke Width**: {icon/strokeWidth} (1.5px)
- **Sizes**: 
  - XS: {icon/size/xs} (16px)
  - SM: {icon/size/sm} (20px)
  - Base: {icon/size/base} (24px)
  - LG: {icon/size/lg} (32px)
- **Colors**: Tokens de {light/icon/*}

Ver `iconography.md` para detalles completos.

### 8. Typography Components (Componentes de Texto)

**Estilos**:
```
Heading 1:
- Font: Roboto Bold
- Size: {fontSize/4xl} (36px)
- Line Height: {lineHeight/tight} (120%)
- Color: {light/text/primary}

Heading 2:
- Font: Roboto Bold
- Size: {fontSize/3xl} (30px)
- Line Height: {lineHeight/tight}

Heading 3:
- Font: Roboto Medium
- Size: {fontSize/2xl} (24px)
- Line Height: {lineHeight/normal} (150%)

Body:
- Font: Roboto Regular
- Size: {fontSize/base} (16px)
- Line Height: {lineHeight/normal}

Body Small:
- Font: Roboto Regular
- Size: {fontSize/sm} (14px)
- Line Height: {lineHeight/normal}

Caption:
- Font: Roboto Regular
- Size: {fontSize/xs} (12px)
- Line Height: {lineHeight/normal}
- Color: {light/text/tertiary}
```

### 9. Modals/Dialogs

**Variantes**:
- **Type**: Alert, Confirmation, Form
- **Size**: Small, Medium, Large

**Especificaciones**:
```
Modal:
- Background: {light/background/tertiary}
- Border Radius: {borderRadius/xl} (16px)
- Shadow: {shadow/xl}
- Max Width: 400px (Small), 560px (Medium), 720px (Large)
- Padding: {spacing/lg} (24px)

Backdrop:
- Background: rgba(0, 0, 0, 0.5)
```

**Auto Layout**:
- Direction: Vertical
- Gap: {spacing/lg} (24px)
- Sections: Header, Content, Actions

### 10. Forms

**Componentes**:
- Form Container
- Field Group (Label + Input + Helper)
- Field Row (múltiples campos en horizontal)
- Action Bar (botones de acción)

**Auto Layout**:
```
Form:
- Direction: Vertical
- Gap: {spacing/lg} (24px)
- Padding: {spacing/md}

Field Group:
- Gap: {spacing/xs} (4px)

Action Bar:
- Direction: Horizontal
- Gap: {spacing/sm} (8px)
- Justify: End
```

## Construcción en Figma

### Pasos Generales

1. **Crear Frame Base**
   - Usar Auto Layout (Shift + A)
   - Nombrar según convención: `Component/Variant`

2. **Aplicar Tokens**
   - Usar estilos de color generados
   - Aplicar spacing tokens
   - Usar typography styles

3. **Configurar Variantes**
   - Seleccionar frames → Create Component Set
   - Agregar propiedades: Type, State, Size, etc.

4. **Testear Responsividad**
   - Redimensionar componentes
   - Verificar Auto Layout constraints
   - Asegurar que mantiene proporciones

### Tips de Auto Layout

- **Hug Contents**: Para componentes que se ajustan a su contenido (botones)
- **Fill Container**: Para componentes que ocupan espacio disponible (inputs)
- **Fixed Size**: Para componentes con tamaño específico (iconos)
- **Min/Max Width**: Para controlar límites de responsive

## Nomenclatura

```
Component/Variant/State/Size

Ejemplos:
- Button/Primary/Default/Medium
- Input/Text/Focus/Large
- Card/Interactive/Hover/Default
- ListItem/TwoLine/Default/Trailing Icon
```

## Organización en Figma

**Página: 01 • Componentes**

```
📁 Atoms
  ├─ Icons
  ├─ Colors
  └─ Typography

📁 Molecules
  ├─ Buttons
  ├─ Input Fields
  ├─ Chips
  └─ List Items

📁 Organisms
  ├─ Navigation
  ├─ Cards
  ├─ Forms
  └─ Modals

📁 Documentation
  ├─ Token Samples
  ├─ Spacing Guide
  └─ Color Palette
```

## Estados Interactivos

Todos los componentes interactivos deben tener:

1. **Default** - Estado inicial
2. **Hover** - Mouse sobre elemento (solo web/tablet)
3. **Active/Pressed** - Click o tap activo
4. **Focus** - Elemento seleccionado (importante para accesibilidad)
5. **Disabled** - Elemento no disponible

## Accesibilidad

- **Contraste**: Mínimo 4.5:1 para texto normal, 3:1 para texto grande
- **Touch Targets**: Mínimo 44×44px (iOS), 48×48px (Android)
- **Focus States**: Siempre visible para navegación por teclado

## Próximos Pasos

1. Construir componentes en la página **01 • Componentes**
2. Crear plantillas en **02 • Plantillas**
3. Ensamblar pantallas usando componentes (ver `mapeo-pantallas.md`)

## Referencias

- [Figma Auto Layout](https://help.figma.com/hc/en-us/articles/360040451373)
- [Material Design Components](https://m3.material.io/components)
- [iOS Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines)
