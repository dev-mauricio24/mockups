# YoDenuncio - Design System & Mockups

Sistema de diseño base para la reconstrucción de las 13 pantallas de la aplicación YoDenuncio en Figma.

## 📋 Contenido del Repositorio

### 🎨 Design Tokens
- **`tokens/design-tokens.json`** - Tokens de diseño en formato Tokens Studio
  - Colores de marca y neutrales
  - Tipografía (Roboto)
  - Espaciado y radios
  - Sombras
  - Variables de iconografía

- **`tokens/brand-colors-notes.md`** - Notas sobre la paleta de colores

### 📚 Documentación
- **`docs/figma-import.md`** - Guía de importación y setup en Figma
- **`docs/guia-de-componentes.md`** - Definición de componentes base con Auto Layout
- **`docs/mapeo-pantallas.md`** - Mapeo de las 13 pantallas a componentes
- **`docs/iconography.md`** - Lineamientos de iconografía (Lucide Icons)

### 🎭 Brand Assets
- **`assets/logo/yo-denuncio-mark.svg`** - Isotipo/marca principal
- **`assets/logo/yo-denuncio-lockup.svg`** - Logo con texto
- **`assets/logo/yo-denuncio-mark-monochrome.svg`** - Versión monocromática

### 🖼️ Mockups Originales
13 pantallas PNG en el directorio raíz:
1. `LoginScreen.png` - Inicio de sesión
2. `RegistroScreen.png` - Registro de usuario
3. `ResetPassword.png` - Recuperación de contraseña
4. `InicioDenuncias.png` - Lista de denuncias
5. `NuevaDenuncia.png` - Formulario de nueva denuncia
6. `ReportDetail.png` - Detalle de denuncia
7. `ConfirmacinResumen.png` - Confirmación de envío
8. `PerfilVista.png` - Perfil de usuario
9. `EditarPerfil.png` - Edición de perfil
10. `NotificacionesLista.png` - Lista de notificaciones
11. `HelpSupport.png` - Ayuda y soporte
12. `AcercaInformacion.png` - Acerca de la app
13. `LogoutFlow.png` - Confirmación de cierre de sesión

## 🚀 Inicio Rápido

### 1. Configurar Figma

```
1. Crear archivo nuevo en Figma
2. Crear páginas:
   - 00 • Tokens
   - 01 • Componentes
   - 02 • Plantillas
   - 03 • Pantallas (iOS)
   - 04 • Pantallas (Android)
```

### 2. Importar Tokens

```
1. Instalar plugin "Tokens Studio for Figma"
2. Abrir plugin → Settings → Import
3. Seleccionar tokens/design-tokens.json
4. Activar sets: global ✅ y light ✅
5. Apply to document
```

Ver guía completa: [`docs/figma-import.md`](docs/figma-import.md)

### 3. Construir Componentes

Seguir [`docs/guia-de-componentes.md`](docs/guia-de-componentes.md) para crear:
- Buttons (4 variantes)
- Input Fields
- Cards
- Navigation Bars
- List Items
- Y más...

### 4. Ensamblar Pantallas

Usar [`docs/mapeo-pantallas.md`](docs/mapeo-pantallas.md) para:
- Identificar componentes por pantalla
- Aplicar Auto Layout
- Instanciar componentes
- Ajustar para iOS y Android

## 🎨 Sistema de Diseño

### Colores de Marca

| Color | Valor | Uso |
|-------|-------|-----|
| Primary | `#FF6B35` | Botones primarios, elementos destacados |
| Secondary | `#2D3142` | Texto principal, navegación |
| Accent | `#4F5D75` | Elementos secundarios |

### Tipografía

- **Familia**: Roboto
- **Tamaños**: 12, 14, 16, 18, 20, 24, 30, 36 px
- **Pesos**: Regular (400), Medium (500), Bold (700)

### Iconografía

- **Set**: Lucide Icons
- **Stroke**: 1.5px
- **Tamaños**: 16, 20, 24, 32 px

Ver: [`docs/iconography.md`](docs/iconography.md)

### Espaciado

- XS: 4px
- SM: 8px
- MD: 16px
- LG: 24px
- XL: 32px
- 2XL: 48px
- 3XL: 64px

## 📱 Plataformas

### iOS
- **Resolución**: 390×844 px (iPhone 12/13/14)
- **Safe Areas**: Top 47px, Bottom 34px
- **Navegación**: Chevron left, center title

### Android
- **Resolución**: 411×891 px (Pixel 5)
- **Safe Areas**: System bars
- **Navegación**: Arrow left, left title

## 📖 Flujo de Trabajo

1. **Importar tokens** → Generar estilos en Figma
2. **Construir componentes** → Usar Auto Layout y tokens
3. **Crear variantes** → Estados y contextos diferentes
4. **Ensamblar pantallas** → Instanciar componentes
5. **Validar** → Responsive, accesibilidad, consistencia

## ✅ Validación

### Checklist por Pantalla

- [ ] Usa instancias de componentes (no elementos sueltos)
- [ ] Aplica tokens (no valores hardcoded)
- [ ] Tiene Auto Layout configurado
- [ ] Es responsive
- [ ] Contempla estados (vacío, loading, error)
- [ ] Cumple accesibilidad (contraste, touch targets)
- [ ] Es consistente con otras pantallas

## 🔄 Próximos Pasos

1. Ajustar colores mediante muestreo directo en Figma
2. Incorporar SVGs definitivos del logo (si se proveen)
3. Reconstruir las 13 pantallas con componentes
4. Exportar y sincronizar cambios al repositorio

## 📝 Notas Importantes

- ⚠️ **Colores aproximados**: Los valores actuales se ajustarán en Figma con muestreo directo de los logos
- 🔧 **Solo modo claro**: Esta versión soporta únicamente light mode
- 🎯 **Token-first**: Siempre usar tokens en lugar de valores fijos
- ♿ **Accesibilidad**: Mínimo 4.5:1 contraste para texto, touch targets 44×44px (iOS) / 48×48px (Android)

## 🛠️ Herramientas Necesarias

- **Figma** - Editor de diseño
- **Tokens Studio for Figma** - Plugin para tokens
- **Roboto** - Fuente (Google Fonts)
- **Lucide Icons** - Plugin o web (lucide.dev)

## 📚 Recursos

- [Tokens Studio Docs](https://docs.tokens.studio/)
- [Figma Auto Layout Guide](https://help.figma.com/hc/en-us/articles/360040451373)
- [Lucide Icons](https://lucide.dev)
- [Material Design 3](https://m3.material.io/)
- [iOS Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines)

## 📄 Licencia

Proyecto educativo. Assets de marca (logos) son propiedad de YoDenuncio.

## 👥 Contribuir

Para ajustes o mejoras:
1. Modificar archivos correspondientes
2. Documentar cambios
3. Commit con mensaje descriptivo
4. Push al repositorio

---

**Versión**: 1.0.0  
**Última actualización**: Noviembre 2025  
**Modo**: Light Mode  
**Plataformas**: iOS (390×844) | Android (411×891)
