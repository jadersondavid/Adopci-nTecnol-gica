# Transformación Digital - Laboratorios Laproff

## 🚀 Solución para GitHub Pages

### Problema de Logos
Los logos originales (`laproff.png` y `prototipado.webp`) pueden no cargar correctamente en GitHub Pages debido a rutas de archivos.

### ✅ Solución Implementada

#### 1. **SVGs Inline como Fallback Principal**
- **Laproff Logo**: SVG con gradiente azul y texto "LP"
- **Prototipado Logo**: SVG con gradiente violeta y checkmark
- **Ventaja**: Siempre funcionan, no dependen de archivos externos

#### 2. **Sistema de Detección Automática**
- JavaScript detecta automáticamente si las imágenes están disponibles
- Si las imágenes cargan: Muestra la imagen real
- Si las imágenes fallan: Mantiene el SVG inline

#### 3. **Funcionalidad de Upload Preservada**
- Los botones de upload siguen funcionando
- Las imágenes subidas reemplazan tanto SVGs como imágenes originales

### 📁 Estructura de Archivos

```
Prototipado/
├── index.html          # Página principal con SVGs inline
├── laproff.png         # Logo Laproff (opcional)
├── prototipado.webp    # Logo Prototipado (opcional)
└── README.md           # Este archivo
```

### 🔧 Cómo Funciona

1. **Carga Inicial**: Se muestran los SVGs inline
2. **Detección**: JavaScript verifica si las imágenes están disponibles
3. **Intercambio**: Si las imágenes cargan, se muestran automáticamente
4. **Fallback**: Si no cargan, se mantienen los SVGs

### 🎨 Personalización

#### Para Cambiar los SVGs:
```html
<!-- Logo Laproff -->
<svg class="logo-svg laproff-svg" width="128" height="128">
  <!-- Modificar aquí el contenido SVG -->
</svg>

<!-- Logo Prototipado -->
<svg class="logo-svg prototype-svg" width="96" height="96">
  <!-- Modificar aquí el contenido SVG -->
</svg>
```

#### Para Agregar Nuevas Imágenes:
1. Sube la imagen al repositorio
2. Actualiza la función `checkImageAvailability()` en el JavaScript
3. Agrega el elemento `<img>` correspondiente

### 🌐 Compatibilidad

- ✅ **GitHub Pages**: Funciona perfectamente
- ✅ **Local Development**: Funciona con servidor local
- ✅ **Navegadores Modernos**: Soporte completo
- ✅ **Responsive**: Se adapta a diferentes tamaños de pantalla

### 🚀 Despliegue

1. Sube todos los archivos a tu repositorio de GitHub
2. Activa GitHub Pages en la configuración del repositorio
3. Los logos se mostrarán automáticamente (SVGs o imágenes según disponibilidad)

### 📝 Notas Técnicas

- **SVGs Inline**: No requieren archivos externos
- **Detección Automática**: Usa `Image.onload` y `Image.onerror`
- **Fallback Graceful**: Siempre hay algo visible
- **Performance**: SVGs son ligeros y escalables

---

**Desarrollado para Laboratorios Laproff** 🧪
*Transformación Digital Integral*
