# Guía de Iconografía - YoDenuncio

Esta guía establece los lineamientos para el uso de iconografía en el sistema de diseño YoDenuncio.

## Set de Iconos: Lucide

**Lucide Icons** es un set de iconos open-source, neutral y moderno que proporciona consistencia visual y flexibilidad.

- **Website**: https://lucide.dev
- **Licencia**: ISC License (open source)
- **Características**:
  - Más de 1000 iconos
  - Diseño consistente y limpio
  - Optimizado para interfaces
  - Compatible con stroke personalizable

### ¿Por qué Lucide?

- ✅ Set neutral (no atado a una marca específica)
- ✅ Stroke personalizable (usamos 1.5px)
- ✅ Consistencia visual en todo el set
- ✅ Open source y gratuito
- ✅ Actualizaciones frecuentes
- ✅ Excelente para aplicaciones móviles

## Especificaciones Técnicas

### Tamaños

Usamos cuatro tamaños estándar, definidos en tokens:

| Token | Tamaño | Uso |
|-------|--------|-----|
| `{icon/size/xs}` | 16px | Iconos muy pequeños, badges, inline text |
| `{icon/size/sm}` | 20px | Iconos secundarios, trailing icons en listas |
| `{icon/size/base}` | 24px | **Tamaño por defecto**, mayoría de casos |
| `{icon/size/lg}` | 32px | Iconos destacados, ilustraciones simples |

### Stroke Width

- **Token**: `{icon/strokeWidth}`
- **Valor**: `1.5px`
- **Nota**: Usar consistentemente en todos los iconos para mantener coherencia visual

### Colores

Usar tokens de color para iconos según contexto:

| Token | Uso |
|-------|-----|
| `{light/icon/default}` | Iconos normales |
| `{light/icon/subtle}` | Iconos secundarios, menos énfasis |
| `{light/icon/emphasis}` | Iconos importantes, mayor énfasis |
| `{light/icon/onPrimary}` | Iconos sobre fondo de color primario |
| `{light/interactive/default}` | Iconos interactivos, links |
| `{light/status/success}` | Estados exitosos |
| `{light/status/error}` | Estados de error |
| `{light/status/warning}` | Estados de advertencia |

## Mapeo de Iconos para Pantallas

### LoginScreen / RegistroScreen / ResetPassword

| Elemento | Icono Lucide | Tamaño |
|----------|--------------|--------|
| Email field | `Mail` | 20px |
| Password field | `Lock` | 20px |
| Show/Hide password | `Eye` / `EyeOff` | 20px |
| Back button | `ChevronLeft` o `ArrowLeft` | 24px |

### InicioDenuncias

| Elemento | Icono Lucide | Tamaño |
|----------|--------------|--------|
| Notificaciones | `Bell` | 24px |
| Perfil | `User` | 24px |
| Nueva denuncia (FAB) | `Plus` | 24px |
| Filtros | `Filter` | 20px |
| Estado: En progreso | `Clock` | 16px |
| Estado: Resuelta | `CheckCircle` | 16px |
| Estado: Rechazada | `XCircle` | 16px |
| Ubicación en card | `MapPin` | 16px |
| Fecha en card | `Calendar` | 16px |

### NuevaDenuncia

| Elemento | Icono Lucide | Tamaño |
|----------|--------------|--------|
| Cerrar | `X` | 24px |
| Agregar foto | `Camera` o `Image` | 20px |
| Agregar ubicación | `MapPin` | 20px |
| Categoría | `Tag` | 20px |
| Adjuntar archivo | `Paperclip` | 20px |
| Eliminar foto | `Trash2` | 16px |

### ReportDetail

| Elemento | Icono Lucide | Tamaño |
|----------|--------------|--------|
| Atrás | `ChevronLeft` | 24px |
| Opciones (menú) | `MoreVertical` | 24px |
| Compartir | `Share2` | 20px |
| Ubicación | `MapPin` | 24px |
| Comentarios | `MessageCircle` | 20px |
| Usuario (autor) | `User` | 16px |
| Fecha | `Calendar` | 16px |
| Enviar comentario | `Send` | 20px |

### PerfilVista

| Elemento | Icono Lucide | Tamaño |
|----------|--------------|--------|
| Editar | `Edit` o `Edit2` | 24px |
| Denuncias totales | `FileText` | 24px |
| Denuncias resueltas | `CheckCircle` | 24px |
| Configuración | `Settings` | 24px |
| Ayuda | `HelpCircle` | 24px |
| Cerrar sesión | `LogOut` | 24px |
| Chevron derecho | `ChevronRight` | 20px |

### EditarPerfil

| Elemento | Icono Lucide | Tamaño |
|----------|--------------|--------|
| Atrás | `ChevronLeft` | 24px |
| Guardar | `Check` | 24px |
| Cambiar foto | `Camera` | 24px |
| Nombre | `User` | 20px |
| Email | `Mail` | 20px |
| Teléfono | `Phone` | 20px |
| Contraseña | `Lock` | 20px |

### NotificacionesLista

| Elemento | Icono Lucide | Tamaño |
|----------|--------------|--------|
| Notificación general | `Bell` | 24px |
| Notificación comentario | `MessageCircle` | 24px |
| Notificación actualización | `Info` | 24px |
| Notificación resuelta | `CheckCircle` | 24px |
| Marcar como leída | `Check` | 20px |
| Eliminar | `X` | 20px |

### HelpSupport

| Elemento | Icono Lucide | Tamaño |
|----------|--------------|--------|
| FAQ | `HelpCircle` | 24px |
| Contacto | `Mail` | 24px |
| Chat | `MessageSquare` | 24px |
| Teléfono | `Phone` | 24px |
| Chevron (expandir) | `ChevronRight` | 20px |

### AcercaInformacion

| Elemento | Icono Lucide | Tamaño |
|----------|--------------|--------|
| Términos | `FileText` | 24px |
| Privacidad | `Shield` | 24px |
| Licencias | `Scale` | 24px |
| Link externo | `ExternalLink` | 16px |

### LogoutFlow

| Elemento | Icono Lucide | Tamaño |
|----------|--------------|--------|
| Logout icon | `LogOut` | 32px |
| Alert icon | `AlertCircle` | 32px |

## Navegación

### Top Navigation Bar

| Elemento | Icono Lucide | Tamaño | Notas |
|----------|--------------|--------|-------|
| Atrás (iOS) | `ChevronLeft` | 24px | Más delgado |
| Atrás (Android) | `ArrowLeft` | 24px | Material Design |
| Menú hamburguesa | `Menu` | 24px | 3 líneas |
| Buscar | `Search` | 24px | |
| Opciones | `MoreVertical` | 24px | Vertical (⋮) |
| Cerrar | `X` | 24px | |

### Bottom Tab Bar (si aplica)

| Elemento | Icono Lucide | Tamaño |
|----------|--------------|--------|
| Inicio | `Home` | 24px |
| Denuncias | `FileText` | 24px |
| Nueva denuncia | `Plus` o `PlusCircle` | 24px |
| Notificaciones | `Bell` | 24px |
| Perfil | `User` | 24px |

## Uso en Figma

### Importar Lucide Icons a Figma

**Opción 1: Plugin (Recomendado)**
1. Instalar plugin: "Lucide Icons" o "Iconify"
2. Buscar iconos por nombre
3. Insertar con stroke width 1.5px
4. Aplicar color desde tokens

**Opción 2: Manual**
1. Ir a https://lucide.dev
2. Buscar el icono
3. Copiar SVG
4. Pegar en Figma (Ctrl/Cmd + V)
5. Ajustar stroke a 1.5px
6. Aplicar color y tamaño

### Crear Componente de Icono

```
Component: Icon/[Nombre]
Properties:
  - Size: 16 | 20 | 24 | 32
  - Color: Default | Subtle | Emphasis | Primary

Auto Layout: Hug contents
Constraints: Center

Token Mapping:
  - 16px → {icon/size/xs}
  - 20px → {icon/size/sm}
  - 24px → {icon/size/base}
  - 32px → {icon/size/lg}
  - Stroke → {icon/strokeWidth}
```

### Organización

**En página 01 • Componentes**:

```
📁 Icons
  ├─ Navigation
  │  ├─ ChevronLeft
  │  ├─ ChevronRight
  │  ├─ ArrowLeft
  │  └─ Menu
  ├─ Actions
  │  ├─ Plus
  │  ├─ Edit
  │  ├─ Delete (Trash2)
  │  ├─ Share
  │  └─ Send
  ├─ Status
  │  ├─ CheckCircle
  │  ├─ XCircle
  │  ├─ AlertCircle
  │  └─ Clock
  ├─ User
  │  ├─ User
  │  ├─ Bell
  │  └─ Settings
  └─ Content
     ├─ FileText
     ├─ Image
     ├─ MapPin
     └─ MessageCircle
```

## Mejores Prácticas

### DO ✅

- Usar tamaños estándar (16, 20, 24, 32px)
- Mantener stroke width en 1.5px
- Aplicar colores desde tokens
- Usar iconos de Lucide para consistencia
- Alinear iconos al centro vertical del texto
- Usar tamaño 24px como default

### DON'T ❌

- No mezclar diferentes sets de iconos
- No usar stroke width variable
- No hardcodear colores
- No distorsionar proporciones del icono
- No usar iconos demasiado complejos
- No usar iconos demasiado pequeños (<16px)

## Accesibilidad

### Touch Targets

Incluso si el icono es pequeño (16-20px), asegurar que el área clickeable sea mínimo:
- **iOS**: 44×44px
- **Android**: 48×48px

Usar Auto Layout padding para expandir el área táctil.

### Contraste

- Iconos principales: mínimo 3:1 de contraste
- Iconos decorativos: pueden ser más sutiles
- Iconos interactivos: siempre con buen contraste

### Semántica

- Iconos interactivos necesitan label/aria-label
- No usar solo icono sin texto en acciones importantes
- En duda, agregar tooltip o label

## Alternativas y Fallbacks

Si Lucide no tiene un icono específico:

1. **Primera opción**: Buscar en Lucide con sinónimos
2. **Segunda opción**: Usar icono genérico cercano
3. **Tercera opción**: Crear custom icon siguiendo:
   - Stroke 1.5px
   - Estilo minimalista
   - Esquinas redondeadas
   - Proporciones consistentes

## Referencias

- **Lucide Icons**: https://lucide.dev
- **Iconify** (múltiples sets): https://iconify.design
- **Figma Icons Plugin**: https://www.figma.com/community/plugin/735098390272716381

## Anexo: Lista Completa de Iconos Usados

### Navegación (8)
- ArrowLeft, ChevronLeft, ChevronRight, ChevronDown
- Menu, X, MoreVertical, MoreHorizontal

### Acciones (10)
- Plus, Edit, Edit2, Trash2, Delete
- Share, Share2, Send, Save, Download

### Usuario (6)
- User, Bell, Settings, LogOut, Lock, Mail

### Estado (6)
- CheckCircle, XCircle, AlertCircle, Info, Clock, HelpCircle

### Contenido (8)
- FileText, Image, Camera, MapPin, Calendar
- MessageCircle, Tag, Paperclip

### Inputs (4)
- Eye, EyeOff, Search, Filter

### Sistema (4)
- Home, Phone, Shield, Scale

**Total**: ~46 iconos únicos

## Notas Finales

- La consistencia en iconografía es crítica para UX
- Revisar periódicamente el set Lucide para nuevas versiones
- Documentar cualquier custom icon agregado
- Mantener librería de iconos actualizada en Figma
