---
lang: es
lang-niv: fonto
lang-ref: 016-jbk
layout: doc
order: 7
title: 'NFC'
---

# 🚀 Aplicación Lectora/Grabadora NFC

[![Licencia: GPL v3](https://img.shields.io/badge/Licencia-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Estilo de código: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Una potente aplicación basada en PySide6 para leer y escribir en varios tipos de etiquetas NFC con funciones avanzadas y una interfaz fácil de usar.

## Instalación

### Requisitos Previos

- Python 3.9 o superior
- Hardware lector NFC (ACR122U, ACR1252U, etc.)

### Inicio Rápido

1. Clona el repositorio:

   ```bash
   git clone https://github.com/Nsfr750/NFC.git
   cd NFC
   ```

2. Crea y activa un entorno virtual:

   ```bash
   python -m venv venv
   .\venv\Scripts\activate  # Windows
   source venv/bin/activate  # Linux/Mac
   ```

3. Instala las dependencias:

   ```bash
   pip install -r requirements.txt
   ```

4. Ejecuta la aplicación:

   ```bash
   python main.py
   ```

Para instrucciones detalladas de instalación, consulta [PREREQUISITOS.md](PREREQUISITOS.md).

## Características

- **Soporte Multi-etiqueta**: Soporte completo para varios tipos de etiquetas NFC incluyendo:
  - NTAG (NTAG213, NTAG215, NTAG216)
  - MIFARE Classic (1K, 4K)
  - MIFARE Ultralight
  - FeliCa (Sony)
  - Tarjetas ISO 14443 Tipo A/B

- **Soporte Integral de Etiquetas**: [Ver operaciones soportadas](docs/supported_operations.md) para todos los tipos de etiquetas

- **Operaciones NDEF**:
  - Leer y escribir registros NDEF
  - Crear y gestionar múltiples registros NDEF
  - Soporte para varios tipos de registros NDEF (Texto, URI, Póster Inteligente, etc.)
  - Vista hexadecimal para inspección de datos en bruto

- **Gestión de Etiquetas**:
  - Leer información de la etiqueta (UID, distribución de memoria, capacidades)
  - Escribir datos en etiquetas con validación
  - Bloquear etiquetas para evitar escrituras no autorizadas
  - Formatear etiquetas para uso NDEF

- **Interfaz de Usuario**:
  - Diseño moderno y receptivo con sphinx_rtd_theme
  - Soporte para temas Claro/Oscuro/Sistema
  - Detección de etiquetas en tiempo real y actualizaciones de estado
  - Panel detallado de información de la etiqueta
  - Visor de registros con opciones de filtrado
  - Documentación completa en inglés e italiano

- **Características de Seguridad**:
  - 🔒 Protección con contraseña para operaciones sensibles
  - 🔑 Cifrado seguro de contraseñas con PBKDF2
  - 🔄 Funcionalidad para cambiar contraseña
  - ⚙️ Alternar para habilitar/deshabilitar la protección por contraseña
  - 🔐 Operaciones protegidas incluyen Herramientas de Etiqueta, Base de Datos y Clonador

- **Características Avanzadas**:
  - Modo de emulación de etiqueta (experimental)
  - Operaciones por lotes para procesar múltiples etiquetas
  - Ejecución de comandos personalizados
  - Sistema de registro con múltiples niveles de detalle
  - Documentación API para desarrolladores
  - Guía de solución de problemas para problemas comunes
  - Directrices de contribución para colaboración de código abierto

## 🚀 Requisitos

- Python 3.8 o superior
- Lector/Grabador NFC compatible:
  - ACR122U
  - PN532 (vía USB/UART)
  - Lectores compatibles con PC/SC
- Windows 10/11 o Linux con soporte PC/SC
- Paquetes Python requeridos (ver `requirements.txt`)

## 📖 Documentación

La documentación completa está disponible en inglés e italiano, incluyendo:

- Guía del Usuario
- Referencia de la API
- Guía de Solución de Problemas
- Preguntas Frecuentes
- Directrices de Contribución

Para construir la documentación localmente:

```bash
# Instalar requisitos de documentación
pip install -r requirements-docs.txt

# Construir documentación en español
cd docs/ESP
make html
```

La documentación estará disponible en el directorio `_build/html` de la carpeta de cada idioma.

## 📦 Instalación

1. Clona este repositorio:

   ```bash
   git clone https://github.com/Nsfr750/NFC.git
   cd NFC
   ```

2. Crea y activa un entorno virtual (recomendado):

   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate

   # Linux/macOS
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Instala los paquetes requeridos:

   ```bash
   pip install -r requirements.txt
   ```

4. (Opcional) Instala los controladores PC/SC si no están instalados:
   - Windows: Instala [controladores CCID](https://ccid.apdu.fr/)
   - Linux: Instala los paquetes `pcscd` y `libpcsclite-dev`

5. Ejecuta la aplicación:

   ```bash
   python main.py
   ```

## 🚀 Uso

### Operaciones Básicas

1. **Conecta tu lector NFC**
   - La aplicación detectará automáticamente los dispositivos soportados
   - El estado de la conexión se muestra en la barra de estado

2. **Lee una etiqueta**
   - Coloca una etiqueta NFC cerca del lector
   - La información de la etiqueta se mostrará en la ventana principal
   - Ver el diseño de memoria detallado en el editor hexadecimal

3. **Escribe en una etiqueta**
   - Navega a la pestaña "Escribir"
   - Selecciona el tipo de registro (Texto, URI, etc.)
   - Ingresa tu contenido y haz clic en "Escribir en Etiqueta"

4. **Bloquea una etiqueta**
   - Usa el botón "Bloquear" para evitar escrituras posteriores
   - Algunas etiquetas admiten bloqueo permanente (¡ten cuidado!)

### 🛠️ Características Avanzadas

- **Emulación de Etiqueta**: Emula una etiqueta NFC (experimental)
- **Comandos Personalizados**: Envía comandos APDU en bruto a la etiqueta
- **Vista de Memoria**: Inspecciona y edita la memoria en bruto de la etiqueta
- **Registros**: Visualiza registros detallados de operaciones con opciones de filtrado

### ⚙️ Configuración

Accede a la configuración mediante `Herramientas > Configuración` o presiona `Ctrl+,`:

- **General**:
  - Conexión automática al inicio
  - Selección de idioma
  - Buscar actualizaciones

- **NFC**:
  - Tiempo de espera del lector
  - Lectura automática al detectar etiqueta
  - Sonido al detectar etiqueta

- **Interfaz**:
  - Tema (Claro/Oscario/Sistema)
  - Tamaño y tipo de fuente
  - Comportamiento de la ventana

- **Avanzado**:
  - Nivel de registro
  - Comandos personalizados
  - Opciones de desarrollador

### ⌨️ Atajos de Teclado

| Atajo       | Acción                     |
|-------------|----------------------------|
| `Ctrl+N`    | Nuevo proyecto             |
| `Ctrl+A`    | Abrir archivo              |
| `Ctrl+G`    | Guardar datos actuales     |
| `Ctrl+Mayús+G` | Guardar como...          |
| `Ctrl+L`    | Leer etiqueta              |
| `Ctrl+E`    | Escribir en etiqueta       |
| `Ctrl+B`    | Borrar etiqueta            |
| `Ctrl+K`    | Bloquear etiqueta          |
| `Ctrl+,`    | Abrir configuración        |
| `F1`        | Mostrar ayuda              |
| `F5`        | Actualizar etiqueta        |
| `Ctrl+Q`    | Salir de la aplicación     |

## 🤝 Contribuciones

¡Las contribuciones son bienvenidas! Aquí hay formas en que puedes ayudar:

1. Reporta errores abriendo un issue
2. Sugiere nuevas funciones o mejoras
3. Envía pull requests
4. Mejora la documentación
5. Comparte tus comentarios e ideas

## 📝 Licencia

Este proyecto está licenciado bajo la Licencia GPL-3.0

## 👤 Autor

- **Nsfr750**
  - Correo: [nsfr750@yandex.com](mailto:nsfr750@yandex.com)
  - GitHub: [@Nsfr750](https://github.com/Nsfr750)
  - Discord: [Únete a nuestra comunidad](https://discord.gg/ryqNeuRYjD)

## 💖 Apoyo

Si encuentras útil este proyecto, considera apoyar su desarrollo:

- [Conviértete en Patrocinador](https://www.patreon.com/Nsfr750)
- [Dona a través de PayPal](https://paypal.me/3dmega)
- Dona Monero:

  ```text
  47Jc6MC47WJVFhiQFYwHyBNQP5BEsjUPG6tc8R37FwcTY8K5Y3LvFzveSXoGiaDQSxDrnCUBJ5WBj6Fgmsfix8VPD4w3gXF
  ```

## 📞 Contacto

Para soporte, solicitudes de funciones o preguntas, por favor abre un issue en [GitHub](https://github.com/Nsfr750/NFC/issues) o únete a nuestro [servidor de Discord](https://discord.gg/ryqNeuRYjD).
