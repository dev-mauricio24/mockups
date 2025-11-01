# Guía de Contribución - YoDenuncio Design System

Esta guía describe cómo contribuir y mantener el sistema de diseño YoDenuncio.

## 🔄 Flujo de Trabajo

### Actualizando Tokens

1. **En Figma**:
   - Hacer cambios en los estilos
   - Exportar desde Tokens Studio plugin
   - Guardar como `design-tokens.json`

2. **En el Repositorio**:
   ```bash
   # Reemplazar archivo de tokens
   cp /path/to/exported/tokens.json tokens/design-tokens.json
   
   # Commit cambios
   git add tokens/design-tokens.json
   git commit -m "Update design tokens: [descripción de cambios]"
   git push
   ```

3. **Documentar Cambios**:
   - Actualizar `tokens/brand-colors-notes.md` si cambian colores
   - Actualizar README si hay cambios estructurales

### Actualizando Componentes

1. **Modificar Guías**:
   - Editar `docs/guia-de-componentes.md`
   - Agregar nuevos componentes con especificaciones completas
   - Incluir variantes, estados, y uso de tokens

2. **Actualizar Mapeos**:
   - Si afecta pantallas, actualizar `docs/mapeo-pantallas.md`
   - Documentar nuevos patrones o flujos

### Actualizando Iconografía

1. **Nuevos Iconos**:
   - Agregar a la lista en `docs/iconography.md`
   - Especificar uso y contexto
   - Mantener consistencia con Lucide

2. **Cambios de Tamaños**:
   - Actualizar tokens en `design-tokens.json`
   - Documentar en `iconography.md`

## 📝 Estándares de Documentación

### Formato de Markdown

- Usar headers jerárquicos (H1, H2, H3)
- Incluir tablas para especificaciones
- Agregar ejemplos cuando sea útil
- Usar emojis para mejorar escaneo visual

### Estructura de Documentos

```markdown
# Título Principal

Breve introducción

## Sección Principal

Contenido...

### Subsección

Detalles...

## Referencias

Enlaces y recursos
```

### Tokens en Documentación

Cuando referenciar tokens, usar formato:
- `{token/path}` para tokens (ej: `{spacing/md}`)
- `#HEX` para colores específicos
- `Npx` para valores fijos

## 🎨 Estándares de Diseño

### Tokens

**Naming Convention**:
```
global/category/subcategory/property
light/category/subcategory/property
```

**Ejemplos**:
- `global/brand/primary`
- `light/text/primary`
- `global/spacing/md`

### Colores

- Siempre usar tokens, nunca valores hardcoded
- Documentar propósito de cada color
- Mantener contraste accesible (mínimo 4.5:1)

### Espaciado

- Usar escala consistente (4px base)
- Múltiplos de 4: 4, 8, 16, 24, 32, 48, 64
- Documentar casos de uso para cada nivel

### Tipografía

- Mantener Roboto como fuente base
- Documentar jerarquía clara
- Especificar line heights para legibilidad

## 🔍 Checklist de Revisión

Antes de hacer commit, verificar:

### Para Tokens
- [ ] JSON es válido (no hay errores de sintaxis)
- [ ] Tokens siguen naming convention
- [ ] Valores son consistentes con escala
- [ ] Referencias `{token}` son correctas
- [ ] Documentación actualizada

### Para Documentación
- [ ] Markdown bien formateado
- [ ] Links internos funcionan
- [ ] Ejemplos son claros
- [ ] Tablas están completas
- [ ] Sin errores ortográficos graves

### Para Assets
- [ ] SVGs son válidos
- [ ] Tamaño apropiado (no muy pesados)
- [ ] Colores usan tokens cuando posible
- [ ] Versiones necesarias (color, mono)

## 🐛 Reportar Problemas

### Template de Issue

```markdown
## Descripción
[Descripción clara del problema]

## Ubicación
- Archivo: `path/to/file.md`
- Línea: 123

## Comportamiento Esperado
[Qué debería pasar]

## Comportamiento Actual
[Qué está pasando]

## Solución Propuesta
[Si tienes una idea de cómo arreglarlo]
```

## 📦 Sincronización Figma ↔ Repo

### Figma → Repositorio

1. Exportar tokens desde Tokens Studio
2. Reemplazar `tokens/design-tokens.json`
3. Commit con mensaje descriptivo
4. Push al repositorio

### Repositorio → Figma

1. Pull cambios del repositorio
2. Abrir Tokens Studio en Figma
3. Import → Seleccionar `design-tokens.json`
4. Apply to document

## 🚀 Releases

### Versionado

Usar Semantic Versioning:
- **Major** (1.0.0): Cambios breaking (rediseño completo)
- **Minor** (0.1.0): Nuevas features (nuevos componentes)
- **Patch** (0.0.1): Fixes (correcciones de tokens)

### Crear Release

1. Actualizar versión en README.md
2. Crear tag:
   ```bash
   git tag -a v1.0.0 -m "Release 1.0.0: Design system baseline"
   git push origin v1.0.0
   ```
3. Documentar cambios en release notes

## 📚 Recursos

- [Tokens Studio Docs](https://docs.tokens.studio/)
- [Figma Best Practices](https://www.figma.com/best-practices/)
- [Design Tokens W3C](https://www.w3.org/community/design-tokens/)
- [Semantic Versioning](https://semver.org/)

## 💡 Tips

### Mantenimiento Regular

- Revisar tokens mensualmente
- Actualizar documentación cuando hay cambios
- Mantener sincronía Figma ↔ Repo
- Validar links y referencias

### Organización

- Un commit por tipo de cambio
- Mensajes de commit descriptivos
- Branch por feature grande
- PR para cambios significativos

### Comunicación

- Documentar decisiones importantes
- Explicar el "por qué" de cambios
- Mantener equipo informado
- Solicitar feedback cuando necesario

## 🤝 Colaboración

### Pull Requests

1. Fork o branch del repositorio
2. Hacer cambios
3. Commit con mensajes claros
4. Push y crear PR
5. Describir cambios en PR
6. Esperar revisión

### Code Review

Revisar:
- Consistencia con estándares
- Calidad de documentación
- Validez de tokens/assets
- Impacto en sistema existente

## 📧 Contacto

Para preguntas o sugerencias:
- Abrir issue en GitHub
- Documentar en el issue template
- Ser específico y claro

---

**Última actualización**: Noviembre 2025  
**Versión del sistema**: 1.0.0
