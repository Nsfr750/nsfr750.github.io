---
lang: es
lang-niv: fonto
lang-ref: 019-jbk
layout: doc
order: 10
title: 'Buscador de PDF'
---

# Buscador de PDF Duplicados

[![Licencia: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Estilo de código: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Una potente herramienta para encontrar y gestionar archivos PDF duplicados en tu computadora. El Buscador de PDF Duplicados te ayuda a identificar y eliminar documentos PDF duplicados, ahorrando espacio en disco y organizando tus archivos de manera más eficiente.

## ✨ Características

- 🔍 **Comparación Inteligente de PDF**: Encuentra PDFs duplicados basándose en el contenido, no solo en nombres o tamaños de archivo
- 📝 **Comparación Basada en Texto**: Identifica duplicados incluso con pequeñas diferencias visuales mediante análisis de texto avanzado
- 👁 **Visor de PDF Integrado**: Previsualiza PDFs directamente dentro de la aplicación
- 📋 **Interfaz de Doble Panel**: Visualiza tanto la lista de archivos como los grupos de duplicados en pestañas separadas
- 🎯 **Filtrado Avanzado**: Filtra por tamaño de archivo, fecha de modificación y patrones de nombre
- 🚀 **Escaneo Rápido**: Algoritmos optimizados para escanear rápidamente grandes colecciones de PDF
- 🎨 **Interfaz Intuitiva**: Interfaz limpia y fácil de usar con soporte para temas claro/oscuro
- 🔄 **Procesamiento por Lotes**: Procesa múltiples archivos o carpetas completas de una vez
- 📊 **Análisis Detallado**: Visualiza detalles de archivos, vistas previas y resultados de comparación
- 🛠 **Herramientas Avanzadas**: Múltiples modos de selección, filtrado y opciones de ordenación
- 🌍 **Soporte Multilingüe**: Disponible en múltiples idiomas
- 📊 **Seguimiento de Progreso**: Barra de progreso en tiempo real para operaciones de procesamiento de archivos
- ⏱ **Archivos Recientes**: Acceso rápido a archivos abiertos recientemente con opciones de menú contextual

## 📦 Instalación

### Requisitos Previos

- Python 3.8 o superior
- pip (gestor de paquetes de Python)
- Backends opcionales para renderizado de PDF (retroceso automático seguro):
  - PyMuPDF (fitz) — predeterminado y agrupado a través de requirements
  - Ghostscript (para Wand) — instala Ghostscript y configura su ruta de ejecutable en Configuración

Consulta [PREREQUISITES.md](PREREQUISITES.md) para la configuración específica de la plataforma.

### Instalación desde el Código Fuente

1. Clona el repositorio:

   ```bash
   git clone https://github.com/Nsfr750/PDF_finder.git
   cd PDF_finder
   ```

2. Crea y activa un entorno virtual (recomendado):

   ```bash
   python -m venv venv
   .\venv\Scripts\activate  # Windows
   source venv/bin/activate  # Linux/Mac
   ```

3. Instala las dependencias necesarias:

   ```bash
   pip install -r requirements.txt
   ```

## Uso

1. Inicia la aplicación:

   ```bash
   python main.py
   ```

2. Haz clic en "Escanear Carpeta" para seleccionar un directorio y buscar PDFs duplicados.

3. Revisa los resultados en la ventana principal. Después de completar un escaneo, la lista de archivos se llena automáticamente con los PDFs escaneados y los grupos de duplicados.

4. Utiliza las herramientas para gestionar los duplicados:
   - Marca los archivos a conservar
   - Elimina los duplicados no deseados
   - Previsualiza los archivos antes de tomar medidas

## Características Clave en Detalle

### Comparación Inteligente de PDF

- Compara el contenido de PDF utilizando algoritmos avanzados de hashing
- Detecta documentos similares incluso con diferentes nombres de archivo o metadatos
- Umbral de similitud configurable para resultados afinados

### Optimizaciones de Rendimiento

- Escaneo multiproceso para un procesamiento más rápido
- Manejo eficiente de memoria para archivos PDF grandes
- Seguimiento del progreso y soporte de cancelación

### Experiencia de Usuario

- Interfaz moderna y receptiva
- Opciones de visualización personalizables
- Atajos de teclado completos
- Información detallada de archivos y vistas previas
- Barra de herramientas con espaciado mejorado y claridad visual
- El diálogo de configuración incluye un botón "Probar backends" para validar la disponibilidad de PyMuPDF y Ghostscript

### Backends de PDF y Retroceso

- Elige tu backend preferido en Configuración → Renderizado de PDF
- Usa "Probar backends" para verificar si Ghostscript está configurado correctamente
- Si falla el backend seleccionado, la aplicación retrocede a un backend disponible y muestra una advertencia en la barra de estado (localizada)

## Historial de Versiones

Consulta [CHANGELOG.md](CHANGELOG.md) para obtener una lista completa de cambios en cada versión.

## Contribuciones

¡Las contribuciones son bienvenidas! Por favor, lee nuestras [Pautas de Contribución](CONTRIBUTING.md) para obtener detalles sobre cómo contribuir a este proyecto.

## 📄 Licencia

Este proyecto está licenciado bajo la Licencia Pública General de GNU v3.0 - consulta el archivo [LICENCIA](LICENCIA) para más detalles.

## 🙏 Agradecimientos

- Gracias a todos los colaboradores que han ayudado a mejorar el Buscador de PDF Duplicados
- Desarrollado con ❤️ usando Python y PyQt6

## 🐞 Errores Conocidos

- La selección de idioma no funciona

---

📅 **Última Actualización**: Agosto 2025  
🐍 **Versión de Python**: 3.8+  
📜 **Licencia**: GPL-3.0
