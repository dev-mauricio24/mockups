# Mapeo de Pantallas - YoDenuncio

Este documento mapea las 13 pantallas existentes del repositorio a los componentes del sistema de diseño, facilitando su reconstrucción en Figma.

## Dimensiones de Pantalla

### iOS
- **Resolución**: 390×844 px
- **Dispositivo de referencia**: iPhone 12/13/14 (6.1")
- **Safe Areas**: Top 47px, Bottom 34px

### Android
- **Resolución**: 411×891 px
- **Dispositivo de referencia**: Pixel 5 / dispositivo estándar
- **Safe Areas**: Ajustar según system bars

## Lista de Pantallas

### 1. LoginScreen.png

**Descripción**: Pantalla de inicio de sesión

**Componentes necesarios**:
- Logo marca (YoDenuncio lockup)
- Input/Text (Email)
- Input/Password
- Button/Primary (Iniciar Sesión)
- Button/Ghost (¿Olvidaste tu contraseña?)
- Button/Tertiary (Crear cuenta)

**Layout**:
- Container: Vertical, Center aligned
- Spacing: {spacing/lg} entre secciones
- Logo: Top, margin {spacing/2xl}
- Form: Center
- Actions: Bottom

**Tokens clave**:
- Background: {light/background/primary}
- Inputs: {borderRadius/md}
- Primary button: {brand/primary}

---

### 2. RegistroScreen.png

**Descripción**: Pantalla de registro de nuevo usuario

**Componentes necesarios**:
- Navigation/TopBar (con botón atrás)
- Input/Text (Nombre completo)
- Input/Email
- Input/Password
- Input/Password (Confirmar contraseña)
- Checkbox + Text (Términos y condiciones)
- Button/Primary (Registrarse)

**Layout**:
- Top bar: Fixed
- Form: Scrollable container
- Vertical spacing: {spacing/md}
- Bottom action: Fixed

**Tokens clave**:
- Form gap: {spacing/md}
- Button height: 48px
- Checkbox size: 20px

---

### 3. ResetPassword.png

**Descripción**: Recuperación de contraseña

**Componentes necesarios**:
- Navigation/TopBar (con botón atrás)
- Typography/Heading2 (título)
- Typography/Body (instrucciones)
- Input/Email
- Button/Primary (Enviar enlace)

**Layout**:
- Container: Vertical
- Content padding: {spacing/lg}
- Gap entre elementos: {spacing/md}

**Tokens clave**:
- Text/secondary: Instrucciones
- Interactive/default: Botón

---

### 4. InicioDenuncias.png

**Descripción**: Pantalla principal con lista de denuncias

**Componentes necesarios**:
- Navigation/TopBar (título, perfil, notificaciones)
- Chips/Tags (Filtros: Todas, En Progreso, Resueltas)
- Card/Interactive (para cada denuncia)
  - Typography/Heading3 (título)
  - Typography/Caption (fecha, estado)
  - Chip/Status
- Button/Primary (FAB - Nueva Denuncia)

**Layout**:
- Top bar: Fixed
- Filters: Horizontal scroll, padding {spacing/md}
- List: Scrollable, gap {spacing/sm}
- FAB: Fixed, bottom right

**Tokens clave**:
- Card shadow: {shadow/md}
- Card radius: {borderRadius/lg}
- FAB: {brand/primary}, {shadow/lg}

---

### 5. NuevaDenuncia.png

**Descripción**: Formulario para crear nueva denuncia

**Componentes necesarios**:
- Navigation/TopBar (título, cerrar)
- Input/Text (Título)
- Input/TextArea (Descripción)
- Button/Secondary (Agregar foto)
- Button/Secondary (Agregar ubicación)
- Chip/Tag (Categoría seleccionada)
- Button/Primary (Enviar denuncia)

**Layout**:
- Form: Vertical, scrollable
- Spacing: {spacing/md}
- Bottom actions: Fixed bar
- Media previews: Horizontal scroll

**Tokens clave**:
- Form gap: {spacing/lg}
- TextArea min height: 120px
- Button bar: {shadow/sm}

---

### 6. ReportDetail.png

**Descripción**: Detalle de una denuncia específica

**Componentes necesarios**:
- Navigation/TopBar (atrás, opciones)
- Image gallery (fotos adjuntas)
- Chip/Status (estado de la denuncia)
- Typography/Heading2 (título)
- Typography/Caption (fecha, autor)
- Typography/Body (descripción)
- Card (Ubicación con mapa)
- ListItem (Comentarios/actualizaciones)
- Input/Text + Button (Agregar comentario)

**Layout**:
- Content: Scrollable
- Sections: Vertical, gap {spacing/lg}
- Gallery: Horizontal scroll
- Comments: List, gap {spacing/sm}

**Tokens clave**:
- Content padding: {spacing/md}
- Section divider: {border/subtle}
- Status chip: Dynamic color

---

### 7. ConfirmacinResumen.png

**Descripción**: Confirmación después de enviar denuncia

**Componentes necesarios**:
- Modal/Confirmation o Full screen
- Icon (Success - checkmark)
- Typography/Heading2 (Confirmación)
- Typography/Body (Mensaje)
- Card/Summary (Resumen de denuncia)
- Button/Primary (Ver denuncia)
- Button/Ghost (Volver al inicio)

**Layout**:
- Container: Vertical, center
- Icon: {icon/size/lg}, color {status/success}
- Content: Center aligned
- Actions: Bottom

**Tokens clave**:
- Success color: {brand/success}
- Card: {borderRadius/lg}
- Modal shadow: {shadow/xl}

---

### 8. PerfilVista.png

**Descripción**: Perfil del usuario

**Componentes necesarios**:
- Navigation/TopBar (título, editar)
- Avatar (grande, circular)
- Typography/Heading2 (nombre)
- Typography/Caption (email, fecha registro)
- ListItem (Estadísticas: denuncias totales, resueltas, etc.)
- Button/Secondary (Editar perfil)
- ListItem/Action (Configuración, Ayuda, Cerrar sesión)

**Layout**:
- Header: Avatar + info, center aligned
- Stats: Grid 2x2 o list
- Actions: List, dividers

**Tokens clave**:
- Avatar size: 80px
- List divider: {border/subtle}
- Padding: {spacing/lg}

---

### 9. EditarPerfil.png

**Descripción**: Edición de datos del perfil

**Componentes necesarios**:
- Navigation/TopBar (atrás, guardar)
- Avatar + Button/Ghost (Cambiar foto)
- Input/Text (Nombre)
- Input/Email (Email)
- Input/Text (Teléfono)
- Input/Password (Cambiar contraseña - expandible)
- Button/Primary (Guardar cambios)

**Layout**:
- Form: Vertical, scrollable
- Avatar: Center, top
- Fields: Gap {spacing/md}
- Save button: Fixed bottom or in top bar

**Tokens clave**:
- Form spacing: {spacing/md}
- Avatar size: 100px
- Input height: 48px

---

### 10. NotificacionesLista.png

**Descripción**: Lista de notificaciones

**Componentes necesarios**:
- Navigation/TopBar (título, opciones)
- ListItem/ThreeLine (para cada notificación)
  - Icon (tipo de notificación)
  - Typography/Body (mensaje)
  - Typography/Caption (tiempo)
  - Badge (no leída)

**Layout**:
- List: Vertical, scrollable
- Items: Dividers {border/subtle}
- Unread indicator: Badge or background

**Tokens clave**:
- Item padding: {spacing/md}
- Badge color: {brand/primary}
- Unread background: {background/secondary}

---

### 11. HelpSupport.png

**Descripción**: Ayuda y soporte

**Componentes necesarios**:
- Navigation/TopBar (atrás, título)
- Card/Interactive (FAQs)
  - Icon (question mark)
  - Typography/Heading3
  - Icon (chevron)
- Button/Secondary (Contactar soporte)
- ListItem (Recursos adicionales)

**Layout**:
- Content: Scrollable
- Cards: Gap {spacing/sm}
- Sections: Gap {spacing/lg}

**Tokens clave**:
- Card: {borderRadius/lg}
- Icon size: {icon/size/base}
- Interactive hover: {shadow/lg}

---

### 12. AcercaInformacion.png

**Descripción**: Acerca de la aplicación

**Componentes necesarios**:
- Navigation/TopBar (atrás, título)
- Logo (YoDenuncio mark, centrado)
- Typography/Heading3 (nombre app)
- Typography/Caption (versión)
- Typography/Body (descripción)
- ListItem (Enlaces: Términos, Privacidad, Licencias)

**Layout**:
- Content: Scrollable, center aligned
- Logo: Top section
- Description: Padded {spacing/lg}
- Links: List at bottom

**Tokens clave**:
- Logo size: 120px
- Text align: Center
- Link color: {interactive/default}

---

### 13. LogoutFlow.png

**Descripción**: Confirmación de cerrar sesión

**Componentes necesarios**:
- Modal/Alert
- Icon (log out)
- Typography/Heading3 (¿Cerrar sesión?)
- Typography/Body (mensaje confirmación)
- Button/Primary (Cerrar sesión)
- Button/Ghost (Cancelar)

**Layout**:
- Modal: Center screen
- Content: Vertical, center aligned
- Actions: Horizontal, gap {spacing/sm}

**Tokens clave**:
- Modal: {borderRadius/xl}
- Modal shadow: {shadow/xl}
- Backdrop: rgba(0,0,0,0.5)

---

## Patrones Comunes

### Navigation Patterns

**Top Bar estándar**:
- Height: 56px (Android), 44px (iOS)
- Leading: Back button o menu icon
- Title: Center (iOS) o Left (Android)
- Trailing: Actions (1-2 icons)

**Bottom Tab Bar** (si aplica):
- Height: 56px (Android), 49px + safe area (iOS)
- 3-5 tabs máximo
- Icon + Label (opcional)

### Form Patterns

**Field spacing**: {spacing/md} (16px)
**Section spacing**: {spacing/lg} (24px)
**Label to input**: {spacing/xs} (4px)
**Helper text**: {fontSize/xs}, {text/tertiary}

### Card Patterns

**Content padding**: {spacing/md} (16px)
**Element spacing**: {spacing/sm} (8px)
**Shadow**: {shadow/md}
**Radius**: {borderRadius/lg} (12px)

## Flujos de Usuario

### Autenticación
1. LoginScreen → InicioDenuncias
2. LoginScreen → RegistroScreen → InicioDenuncias
3. LoginScreen → ResetPassword → LoginScreen

### Denuncias
1. InicioDenuncias → NuevaDenuncia → ConfirmacinResumen → ReportDetail
2. InicioDenuncias → ReportDetail

### Perfil
1. InicioDenuncias → PerfilVista → EditarPerfil → PerfilVista
2. PerfilVista → LogoutFlow → LoginScreen

### Otros
1. Cualquier pantalla → NotificacionesLista
2. PerfilVista → HelpSupport
3. PerfilVista → AcercaInformacion

## Proceso de Reconstrucción

### Para cada pantalla:

1. **Analizar mockup original** (archivo .png)
2. **Identificar componentes** del sistema de diseño
3. **Crear frame** con dimensiones correctas
4. **Usar instancias** de componentes de la página 01 • Componentes
5. **Aplicar Auto Layout** para responsividad
6. **Ajustar tokens** (colores, espaciado, tipografía)
7. **Verificar estados** (empty, loading, error si aplica)
8. **Duplicar para iOS y Android** si hay diferencias

### Tips:

- Usar **Components** en lugar de copiar elementos
- Aprovechar **Variants** para diferentes estados
- Usar **Constraints** para responsive behavior
- Documentar **diferencias iOS/Android** si las hay

## Validación

### Checklist por pantalla:

- [ ] Usa instancias de componentes (no elementos sueltos)
- [ ] Aplica tokens de diseño (no valores hardcoded)
- [ ] Tiene Auto Layout configurado
- [ ] Responsive (se adapta a cambios de tamaño)
- [ ] Estados contemplados (vacío, loading, error)
- [ ] Accesible (contraste, touch targets)
- [ ] Consistente con otras pantallas

## Recursos

- Mockups originales: Directorio raíz del repositorio
- Componentes base: Página 01 • Componentes en Figma
- Tokens: `tokens/design-tokens.json`
- Guía de componentes: `docs/guia-de-componentes.md`

## Notas

- Priorizar iOS primero (página 03), luego Android (página 04)
- Documentar diferencias platform-specific
- Las imágenes en mockups son placeholder, usar elementos de marca
- Iconografía: Lucide icons (ver `iconography.md`)
