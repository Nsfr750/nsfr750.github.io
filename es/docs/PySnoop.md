---
lang: es
lang-niv: fonto
lang-ref: 020-jbk
layout: doc
order: 11
title: 'PySnoop'
---

# PySnoop

[![Licencia: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.7+](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![Estilo de código: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Una aplicación moderna basada en Python para leer, escribir y analizar datos de bandas magnéticas de tarjetas. Este proyecto es una continuación del proyecto original StripeSnoop, reconstruido con Python moderno y una interfaz fácil de usar.

## ✨ Características

- **Lectura de tarjetas**: Lee tarjetas de banda magnética utilizando lectores compatibles
- **Gestión de base de datos**: Almacena y gestiona datos de tarjetas de forma segura
- **Múltiples formatos**: Exporta/Importa datos de tarjetas en varios formatos
- **Interfaz gráfica moderna**: Interfaz de usuario intuitiva con soporte para temas
- **Multiplataforma**: Funciona en Windows, macOS y Linux
- **Ejecutable independiente**: Se puede compilar como un único archivo ejecutable para una fácil distribución
- **Versiones de depuración**: Configuración especial de depuración para solución de problemas
- **Seguridad**: Almacenamiento seguro para datos sensibles de tarjetas
- **Validación**: Validación integrada de números de tarjeta (C10/Luhn)
- **Documentación**: Documentación completa y ejemplos

## 🚀 Instalación

### Requisitos previos

- Python 3.7 o superior
- pip (gestor de paquetes de Python)
- Git (opcional, para desarrollo)

### Inicio rápido

1. Clona el repositorio:

   ```bash
   git clone https://github.com/Nsfr750/PySnoop.git
   cd PySnoop
   ```

2. Crea y activa un entorno virtual:

   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Instala las dependencias:

   ```bash
   pip install -r requirements.txt
   ```

## 🏗️ Construyendo la aplicación

PySnoop puede compilarse en un ejecutable independiente usando Nuitka. Proporcionamos dos scripts de compilación:

### Versión de depuración

```bash
.\snoop_debug.bat
```

Esto crea una versión de depuración de la aplicación con la ventana de consola habilitada para solución de problemas.

### Versión de lanzamiento

```bash
.\snoop.bat
```

Esto crea una versión optimizada de lanzamiento de la aplicación.

### Salidas de compilación

- Versión de depuración: `build\PySnoop_debug.exe`
- Versión de lanzamiento: `build\PySnoop.exe`

## 🛠️ Desarrollo
   ```bash
   pip install -r requirements.txt
   ```

## 💻 Uso

### Modo gráfico (Recomendado)

```bash
python pysnoop_gui.py
```

### Interfaz de línea de comandos

```bash
python pysnoop.py [opciones]
```

### Opciones disponibles

```bash
-h, --help      Muestra el mensaje de ayuda y sale
-v, --verbose   Habilita la salida detallada
--version       Muestra la información de la versión
```

## 🔌 Dispositivos compatibles

- Lector/Grabador de tarjetas de banda magnética MSR605
- Otros lectores de tarjetas compatibles con HID (experimental)

## 📚 Documentación

Para documentación detallada, incluyendo referencia de API y ejemplos de uso, por favor visita la [documentación](https://nsfr750.github.io/PySnoop/ "Documentación de PySnoop").

## 🤝 Contribuciones

¡Las contribuciones son bienvenidas! Por favor, lee nuestras [pautas de contribución](CONTRIBUTING.md) para comenzar.

## 📄 Licencia

Este proyecto está licenciado bajo la Licencia GPLv3 - ver el archivo [LICENCIA](LICENCIA) para más detalles.

## 🙏 Apoyo

Si encuentras útil este proyecto, considera apoyar su desarrollo:

[![Donar vía PayPal](https://img.shields.io/badge/Donar-PayPal-blue.svg)](https://paypal.me/3dmega)
[![Conviértete en Patrocinador](https://img.shields.io/badge/Apoya-Patreon-naranja.svg)](https://www.patreon.com/Nsfr750)

## 📧 Contacto

Para preguntas o soporte, por favor abre un problema o contacta a [Nsfr750](mailto:nsfr750@yandex.com).

## Créditos

- Basado en el proyecto original StripeSnoop (http://stripesnoop.sourceforge.net)

## Cómo contribuir

¡Las contribuciones son bienvenidas! No dudes en enviar una solicitud de extracción.
