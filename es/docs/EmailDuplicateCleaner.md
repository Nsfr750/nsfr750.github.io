---
lang: es
lang-niv: fonto
lang-ref: 013-jbk
layout: doc
order: 4
title: 'Email Duplicate Cleaner'
---

# 📧 Limpiador de Correos Duplicados

Una herramienta completa en Python diseñada para escanear, identificar y eliminar correos electrónicos duplicados en múltiples clientes de correo. Incluye interfaces web, de escritorio y de línea de comandos.

## 🚀 Versión

**Versión Actual:**
[![Versión en GitHub](https://img.shields.io/badge/versi%C3%B3n-v2.5.2-green)](https://github.com/Nsfr750/EmailDuplicateCleaner)
[![Documentación](https://img.shields.io/badge/documentaci%C3%B3n-disponible-brightgreen)](https://github.com/Nsfr750/EmailDuplicateCleaner/blob/master/README.md)
[![Versiones de Python](https://img.shields.io/badge/python-3.8%20|%203.9%20|%203.10%20|%203.11%20|%203.12-blue)](https://www.python.org/)
[![Licencia: GPL v3](https://img.shields.io/badge/Licencia-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![PyPI](https://img.shields.io/pypi/v/email-duplicate-cleaner)](https://pypi.org/project/email-duplicate-cleaner/)
[![Donar](https://img.shields.io/badge/Donar-PayPal-green.svg)](https://paypal.me/3dmega)
[![Soporte](https://img.shields.io/badge/Soporte-Patreon-ff69b4.svg)](https://www.patreon.com/Nsfr750)

## ✨ Novedades en la Versión 2.5.2

- 🚀 Actualizado a la versión 2.5.2
- 🐛 Corregida la visualización del número de versión en el diálogo Acerca de
- 📚 Documentación actualizada con los últimos cambios

## ✨ Novedades en la Versión 2.5.1

- 🐛 Corregido error de importación de QAction en la interfaz gráfica de PySide6
- 🌐 Añadidas traducciones completas al inglés
- 📄 Incluido archivo de licencia GPL-3.0
- 🔄 Mejorado el manejo de errores en la inicialización de la interfaz gráfica
- ⬆️ Actualizadas dependencias para mayor estabilidad

## ✨ Características

### 🔍 Detección de Duplicados

- Múltiples criterios de detección:
  - Estricto: Comparación exhaustiva
  - Solo Contenido: Análisis del cuerpo del mensaje
  - Encabezados: Coincidencia basada en metadatos
  - Asunto+Remitente: Identificación enfocada

### 📊 Análisis de Correos

- Análisis avanzado de correos electrónicos:
  - Análisis de remitentes: Identifica principales remitentes y dominios
  - Análisis temporal: Visualiza patrones de correo a lo largo del tiempo
  - Análisis de archivos adjuntos: Tipos, tamaños y frecuencias
  - Análisis de hilos: Visualiza y gestiona conversaciones
  - Análisis de duplicados: Información detallada sobre la detección
  - Informes exportables en múltiples formatos (Texto, HTML, JSON)

### 🖥️ Soporte para Múltiples Interfaces

- **Interfaz Web** - Diseño moderno y receptivo con modo claro/oscuro
- **Interfaz de Escritorio** - Experiencia nativa de escritorio con PySide6
- **Interfaz de Línea de Comandos** - Potente soporte para automatización y scripts

### 🌓 Experiencia de Usuario Mejorada

- Interfaz web moderna con modo claro/oscuro
- Vista previa interactiva con actualizaciones en tiempo real
- Sistema de ayuda completo
- Modo depuración con registro detallado
- Modo demostración para pruebas y aprendizaje

### 🔒 Compatibilidad con Clientes de Correo

Soporte para:

- Mozilla Thunderbird
- Apple Mail
- Microsoft Outlook
- Formatos genéricos mbox/maildir

### 🏗️ Aspectos Técnicos Destacados

- Interfaz web moderna construida con Flask
- SQLAlchemy para gestión de bases de datos
- Sistema de ayuda completo con contenido dinámico
- Arquitectura modular con clara separación de responsabilidades
- Compatibilidad multiplataforma
- Amplio manejo de errores y registro

## 🛠️ Requisitos Previos

- Python 3.8 o superior
- pip
- Sistemas operativos compatibles: Windows, macOS, Linux

## 🚀 Inicio Rápido

### 💰 Apoya Este Proyecto

Si encuentras útil esta herramienta, por favor considera apoyar su desarrollo:

- [![Donar](https://img.shields.io/badge/Donar-PayPal-green.svg)](https://paypal.me/3dmega) Apoya a través de PayPal
- [![Soporte](https://img.shields.io/badge/Soporte-Patreon-ff69b4.svg)](https://www.patreon.com/Nsfr750) Conviértete en Patrocinador
- :money_with_wings: **Monero (XMR)**: 
  ```
  47Jc6MC47WJVFhiQFYwHyBNQP5BEsjUPG6tc8R37FwcTY8K5Y3LvFzveSXoGiaDQSxDrnCUBJ5WBj6Fgmsfix8VPD4w3gXF
  ```

## 📦 Instalación

1.  Clona el repositorio:

    ```bash
    git clone https://github.com/Nsfr750/EmailDuplicateCleaner.git
    cd EmailDuplicateCleaner
    ```

2.  Instala las dependencias:

    ```bash
    pip install -r requirements.txt
    ```

### Ejecutando la Aplicación

#### Interfaz Web

```bash
python app.py
```

Accede en `http://localhost:5000`

#### Interfaz de Escritorio

```bash
python email_cleaner_gui.py
```

#### Demostración por Línea de Comandos

```bash
python email_duplicate_cleaner.py --demo
```

## 🤝 Contribuciones

¿Interesado en contribuir? ¡Consulta nuestras [Pautas de Contribución](CONTRIBUTING.md)!

## 📄 Licencia

Este proyecto está licenciado bajo la Licencia MIT.

## 🐛 Problemas

¿Encontraste un error? [Abre un informe](https://github.com/Nsfr750/EmailDuplicateCleaner/issues)

## 📊 Métodos de Detección

- `strict`: ID del mensaje + Fecha + De + Asunto + Contenido
- `content`: Solo contenido
- `headers`: ID del mensaje + Fecha + De + Asunto
- `subject-sender`: Solo campos de Asunto y Remitente

## Características de Seguridad

- Siempre conserva al menos una copia de cada correo
- Conserva el correo más antiguo por defecto
- Correos originales recuperables desde la papelera
- Modo demostración para pruebas seguras

## Estructura del Proyecto

- `email_cleaner_web.py`: Interfaz web
- `email_cleaner_gui.py`: Interfaz gráfica de escritorio
- `email_duplicate_cleaner.py`: Funcionalidad principal y CLI
- `static/`: Recursos web (CSS, JS)
- `templates/`: Plantillas HTML

## Flujos de Trabajo

- Modo Demostración: Se ejecuta con correos de prueba
- Ayuda: Muestra información de uso
- Modo Interfaz Gráfica: Inicia la interfaz de escritorio
- Modo Web: Inicia el servidor web

## Estructura de la Interfaz Gráfica

- **Interfaz Gráfica (`email_cleaner_gui.py`)**: Una interfaz gráfica fácil de usar construida con Tkinter. Proporciona una forma intuitiva de seleccionar clientes de correo, escanear carpetas y gestionar duplicados.
- **Línea de Comandos (`email_cleaner_cli.py`)**: Una interfaz de línea de comandos para usuarios que prefieren trabajar en la terminal.
- **Web (`app.py`)**: Una interfaz web construida con Flask, accesible desde cualquier navegador.

### Módulos Auxiliares (`struttura/`)

El directorio `struttura/` contiene todos los módulos auxiliares que soportan la interfaz gráfica, como ventanas de diálogo y menús.

- **`menu.py`**: Gestiona la creación y funcionalidad de la barra de menú principal, manteniendo el archivo principal de la interfaz gráfica limpio y enfocado en su diseño central.
- **`about.py`**, **`help.py`**, **`sponsor.py`**: Definen las ventanas de diálogo `Acerca de`, `Ayuda` y `Patrocinador`, cada una encapsulada en su propia clase.
- **`log_viewer.py`**: Un visor de registros simple para mostrar los registros de la aplicación.

## Características de la Interfaz Gráfica

- **Interfaz Intuitiva**: Una interfaz gráfica limpia y fácil de usar para gestionar cuentas de correo y buscar duplicados.
- **Selección Múltiple**: Usa `Mayús+Flechas` y `Ctrl+Flechas` para seleccionar múltiples buzones y carpetas.
- **Soporte Multilingüe**: Disponible en inglés e italiano.
