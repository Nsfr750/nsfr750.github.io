---
lang: es
lang-niv: fonto
lang-ref: 014-jbk
layout: page
title: 'Eliminador de Imágenes Duplicadas'
---

# Eliminador de Imágenes Duplicadas

Eliminador de Imágenes Duplicadas es una potente aplicación en Python diseñada para la gestión y eliminación eficiente de imágenes duplicadas. Aprovechando la biblioteca Wand (ImageMagick) para el procesamiento de imágenes, esta herramienta ofrece técnicas avanzadas de comparación visual para identificar y gestionar imágenes duplicadas con alta precisión.

## Características Principales

- **Procesamiento Avanzado de Imágenes**: Impulsado por Wand/ImageMagick para un soporte superior de formatos de imagen
- **Detección Visual de Duplicados**: Hash perceptual para identificar imágenes visualmente similares
- **Soporte Integral de Formatos**: Maneja todos los formatos principales, incluyendo JPEG, PNG, WEBP, PSD y más
- **Interfaz Intuitiva**: Interfaz gráfica fácil de usar con soporte para temas claro/oscuro
- **Soporte Multilingüe**: Internacionalización integrada con soporte para inglés e italiano
- **Procesamiento por Lotes**: Procesa eficientemente miles de imágenes
- **Vista Previa y Comparación**: Comparación lado a lado antes de realizar acciones
- **Operaciones Seguras**: Mueve a la papelera en lugar de eliminar permanentemente
- **Registro Detallado**: Registro completo de operaciones para trazabilidad

## Requisitos del Sistema

- **Python**: 3.8 o superior (se recomienda 3.10+)
- **ImageMagick**: Requerido para el procesamiento de imágenes con Wand
  - Windows: Instalar desde [ImageMagick Windows](https://imagemagick.org/script/download.php#windows)
  - macOS: `brew install imagemagick`
  - Linux: `sudo apt-get install libmagickwand-dev`
- **Memoria**: Mínimo 4GB, se recomiendan 8GB+ para colecciones grandes de imágenes
- **Almacenamiento**: Espacio suficiente para las imágenes que se están procesando + archivos temporales
- **Sistemas Operativos**:
  - Windows 10/11
  - macOS 10.15+
  - Linux con X11/Wayland

## ¿Por qué Wand/ImageMagick?

Eliminador de Imágenes Duplicadas utiliza Wand (una interfaz de Python para ImageMagick) por varias ventajas:

- Mayor soporte de formatos, incluyendo PSD, GIF y BMP
- Mejor gestión de memoria para imágenes grandes
- Comportamiento más consistente en diferentes plataformas
- Capacidades avanzadas de manipulación de imágenes
- Mantenimiento activo y actualizaciones de seguridad

## Uso

### Interfaz Principal

La aplicación presenta una interfaz moderna y fácil de usar con los siguientes componentes principales:

1. **Barra de Menú**: Acceso a todas las funciones y configuraciones de la aplicación
2. **Barra de Herramientas**: Acceso rápido a funciones de uso frecuente
3. **Explorador de Carpetas**: Navega y selecciona directorios para escanear
4. **Panel de Vista Previa**: Visualiza y compara imágenes lado a lado
5. **Panel de Resultados**: Muestra los duplicados encontrados con puntuaciones de similitud
6. **Barra de Estado**: Muestra el progreso de la operación e información del sistema

### Flujo de Trabajo Básico

1. **Seleccionar Carpeta de Origen**
   - Haz clic en el botón "Abrir Carpeta" o usa `Archivo > Abrir Carpeta`
   - La aplicación escaneará en busca de formatos de imagen compatibles
   - Formatos compatibles: JPEG, PNG, WEBP, PSD, BMP, GIF y más (a través de Wand/ImageMagick)

2. **Configurar Ajustes de Escaneo**
   - Ajusta el umbral de similitud (predeterminado: 90%)
   - Establece el tamaño mínimo de imagen a considerar
   - Elige qué propiedades de imagen comparar (tamaño, fecha, hash de contenido)

3. **Iniciar el Escaneo**
   - Haz clic en "Iniciar Escaneo" para comenzar la detección de duplicados
   - El progreso se muestra en la barra de estado
   - Pausa o detén el escaneo en cualquier momento

4. **Revisar Resultados**
   - Los grupos de duplicados se muestran con vistas previas
   - Ordena por tamaño de archivo, fecha o puntuación de similitud
   - Usa la herramienta de comparación lado a lado para verificación

5. **Gestionar Duplicados**
   - Selecciona imágenes para conservar o eliminar
   - Mueve duplicados a la papelera (recuperables) o elimínalos permanentemente
   - Exporta resultados a CSV/JSON como referencia

### Características Avanzadas

#### Procesamiento por Lotes

- Procesa múltiples carpetas en secuencia
- Guarda y carga configuraciones de escaneo
- Programa escaneos automáticos

#### Selección Inteligente

- Auto-selección de imágenes por criterios (más antiguas, más pequeñas, etc.)
- Conserva la versión de mayor resolución
- Preserva imágenes con patrones de nombres específicos

#### Herramientas de Comparación de Imágenes

- Modos de comparación lado a lado y superpuestos
- Zoom y desplazamiento sincronizados entre imágenes
- Comparación de histogramas y datos EXIF

#### Filtros Personalizados

- Filtra por dimensiones de imagen
- Filtra por fecha de creación/modificación
- Filtra por formato de imagen o perfil de color

#### Integración con Wand/ImageMagick

- Soporte avanzado de formatos de imagen
- Mejor manejo de perfiles de color y metadatos
- Soporte para formatos RAW de cámara cuando está habilitado en ImageMagick

### Atajos de Teclado

| Atajo         | Acción                           |
|---------------|----------------------------------|
| `Ctrl+O`     | Abrir carpeta                    |
| `Ctrl+F`     | Iniciar nuevo escaneo            |
| `Espacio`    | Alternar selección de imagen actual |
| `Supr`       | Mover seleccionado a la papelera |
| `Ctrl+Z`     | Deshacer última acción           |
| `F5`         | Actualizar vista                 |

## Optimización del Rendimiento

### Para Colecciones Grandes

- Usa el modo "Comparación Rápida" para un filtrado inicial
- Aumenta el tamaño mínimo de archivo para omitir miniaturas
- Programa escaneos en horarios de poca actividad para colecciones grandes

### Gestión de Memoria

- Cierra otras aplicaciones que consuman mucha memoria
- Ajusta los límites de recursos de ImageMagick si es necesario (ver Instalación)
- Procesa imágenes en lotes más pequeños

### Consideraciones de Almacenamiento

- Asegúrate de tener suficiente espacio libre para archivos temporales
- Procesa imágenes directamente desde la unidad de origen cuando sea posible
- Considera usar un SSD rápido para un mejor rendimiento

## Solución de Problemas

### Rendimiento Lento

- Verifica la configuración de políticas de ImageMagick (ver Instalación)
- Reduce el número de operaciones simultáneas
- Desactiva la vista previa en tiempo real para colecciones grandes

### Imágenes que Faltan

- Verifica que ImageMagick admita el formato de imagen
- Comprueba los permisos de archivo
- Busca mensajes de error en el visor de registros

### Resultados Inesperados

- Ajusta el umbral de similitud
- Verifica si los filtros son demasiado restrictivos
- Confirma que los metadatos de la imagen se estén leyendo correctamente

## Configuración

### Opciones Principales

#### Precisión de Comparación

- **Nivel de precisión (1-100)**:
  - Valores más bajos encuentran más duplicados
  - Valores más altos encuentran solo duplicados casi idénticos

#### Tamaños Mínimos

- **Ignorar imágenes por debajo de**:
  - Ancho mínimo (píxeles)
  - Alto mínimo (píxeles)
  - Tamaño mínimo (KB)

#### Formatos Soportados

- **Extensiones permitidas**:
  - .jpg, .jpeg
  - .png
  - .gif
  - .bmp
  - .webp

#### Carpetas Excluidas

- **Lista de carpetas a ignorar**:
  - Carpetas del sistema
  - Carpetas temporales
  - Carpetas específicas

### Consejos de Configuración

1. **Precisión**
   - Nivel 70-80 para un buen equilibrio
   - Nivel 90+ para comparaciones muy estrictas

2. **Memoria**
   - Monitorea el uso de RAM
   - Reduce la memoria caché si es necesario

3. **Copia de Seguridad**
   - Siempre guarda las configuraciones
   - Exporta informes antes de eliminar imágenes
