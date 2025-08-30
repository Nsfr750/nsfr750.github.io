---
lang: es
lang-niv: fonto
lang-ref: 018-jbk
layout: doc
order: 9
title: 'OpenPGP'
---

# Documentación de la Aplicación OpenPGP GUI

Bienvenido a la documentación oficial de la **Aplicación OpenPGP GUI**.

## Visión General
Esta aplicación proporciona una interfaz moderna y fácil de usar para la gestión de claves OpenPGP, cifrado, descifrado, firma de mensajes, verificación y generación de certificados SSL. Todas las operaciones criptográficas se realizan localmente para garantizar la máxima privacidad.

# Características

- Interfaz de usuario moderna con ttkbootstrap (tema Superhero)
- Generar, cargar y exportar pares de claves OpenPGP
- Establecer nombre de la clave, correo electrónico, contraseña y verificar huella digital
- Cifrar y descifrar mensajes
- Firmar y verificar mensajes (firmas separadas)
- Exportar clave pública en formato ASCII (.asc)
- Visualizar huella digital para verificación de seguridad
- Generar certificados SSL con CN personalizado
- Limpiar/reiniciar todos los campos con un clic
- **Sistema de registro centralizado** (información, advertencias, errores, excepciones no capturadas)
- **Visor de registros con filtrado en tiempo real** (TODOS, INFORMACIÓN, ADVERTENCIA, ERROR)
- Usa `log_info`, `log_warning`, `log_error` para entradas de registro personalizadas
- Captura y muestra automática de trazas en el visor de registros
- Barra de menú dinámica con diálogos Acerca de, Ayuda, Visor de Registros, Patrocinador, Versión
- Versión semántica e información de versión
- Estructura modular (`struttura`, `gui`, etc.)
- Fácil extensibilidad y personalización de temas (a través de ttkbootstrap)

# Comenzando

## Requisitos
- Python 3.9 o superior
- PySide6 (incluido en los requisitos)
- pgpy (incluido en los requisitos)
- cryptography (incluido en los requisitos)
- pyperclip (incluido en los requisitos)

> **Nota**: La aplicación ha sido migrada de Tkinter/ttkbootstrap a PySide6 para una interfaz de usuario más moderna y mantenible.

## Instalación
1. Clona o descarga este repositorio.
2. (Opcional) Crea un entorno virtual:
   ```
   python -m venv venv
   venv\Scripts\activate
   ```
3. Instala las dependencias:
   ```
   pip install -r requirements.txt
   ```

## Ejecutando la Aplicación
Ejecuta desde la raíz del proyecto:
```
python main.py
```

Si ves errores de importación, asegúrate de estar ejecutando desde la raíz y no desde una subcarpeta.

# Guía del Usuario

## Vista General de la Ventana Principal
- Ingresa tu nombre, correo electrónico y contraseña para la generación de claves.
- Selecciona el algoritmo (actualmente RSA; próximamente más).
- Usa los botones para generar, cargar o exportar claves.
- Se muestra la huella digital de la clave cargada/generada para verificación.
- Usa el área de texto para ingresar mensajes para cifrar, descifrar, firmar o verificar.
- Exporta tu clave pública para compartirla de forma segura.
- Genera certificados SSL desde la interfaz gráfica.
- Usa el botón 'Limpiar' para reiniciar todos los campos.

## Barra de Menú
- **Archivo**: Exportar clave pública, Salir
- **Registro**: Ver registro (con filtros para TODOS, INFORMACIÓN, ADVERTENCIA, ERROR)
- **Ayuda**: Ayuda, Acerca de, Patrocinador

## Registro y Visor de Registros
- Toda la información, advertencias, errores y excepciones no capturadas se registran automáticamente.
- Usa `log_info(msg)`, `log_warning(msg)`, `log_error(msg)` en tus scripts para entradas de registro personalizadas.
- El Visor de Registros (Registro > Ver Registro) te permite filtrar y ver registros por nivel.
- Si falta el archivo de registro, se muestra el último rastreo de ejecución si está disponible.

## Consejos
- Todas las operaciones criptográficas son locales (sin nube).
- Para mejores resultados, usa contraseñas seguras.
- La ventana de registro proporciona retroalimentación y detalles de errores.

# Uso Avanzado

## Exportando Claves Públicas
- Usa el botón 'Exportar Clave Pública' o la opción del menú para guardar tu clave pública en formato ASCII (.asc).

## Verificación de Huella Digital
- Siempre verifica la huella digital antes de compartir tu clave pública para mayor seguridad.

## Generación de Certificados SSL
- Ingresa el Nombre Común (CN) deseado en el campo de nombre.
- Haz clic en el botón 'Generar Certificado SSL' para crear un certificado autofirmado.

## Extendiendo la Aplicación
- Puedes agregar soporte para más algoritmos (ECC, Ed25519) extendiendo la lógica de generación de claves en `main_window.py`.
- La interfaz gráfica usa ttkbootstrap para una fácil personalización de temas.

## Registro y Depuración
- Todas las acciones, advertencias, errores y excepciones no capturadas se registran en `traceback.log`.
- Usa `log_info`, `log_warning`, `log_error` para entradas de registro personalizadas en tu código.
- El Visor de Registros admite filtrado por TODOS, INFORMACIÓN, ADVERTENCIA, ERROR.
- Las excepciones no capturadas se registran automáticamente y se muestran en el Visor de Registros (con rastreo).

## Solución de Problemas
- Si encuentras errores de importación, asegúrate de estar ejecutando desde la raíz del proyecto.
- Para problemas con dependencias, verifica `requirements.txt` o reinstala los paquetes necesarios.

# Guía del Desarrollador

¡Bienvenido, desarrollador! Esta guía proporciona lo esencial para contribuir y extender la Aplicación OpenPGP GUI.

---

## Estructura del Proyecto
- `main.py` — Punto de entrada, inicia la ventana principal.
- `gui/` — Todos los componentes de la interfaz gráfica (ventana principal, widgets, diálogos).
- `struttura/` — Lógica principal, diálogos, utilidades, control de versiones, ayuda/acerca de, etc.
- `docs/` — Documentación.
- `requirements.txt` — Dependencias de Python.

## Tecnologías Clave
- **Python 3.x**
- **Tkinter** — Marco de interfaz gráfica (con ttkbootstrap para temas)
- **pgpy** — Criptografía OpenPGP
- **cryptography** — Generación de certificados SSL
- **Pillow** — (opcional) para iconos

## Cómo Contribuir
1. Haz un fork y clona el repositorio.
2. Crea un entorno virtual e instala las dependencias.
3. Sigue PEP8 y mantén el código modular.
4. Documenta nuevas características y actualiza `CHANGELOG.md`.
5. Añade o actualiza pruebas si es posible.
6. Abre una solicitud de extracción con una descripción clara.

## Añadiendo Características
- Para añadir nuevos algoritmos (ej. ECC), extiende la lógica de generación de claves en `main_window.py`.
- Para nuevos componentes de interfaz gráfica, añade widgets en `gui/` y mantén la lógica separada de la interfaz.
- Usa estilos `ttkbootstrap` para una apariencia consistente.

## Pruebas
- Añade pruebas para nuevas características y correcciones de errores.
- Pruebas manuales: ejecuta `python main.py` y usa todas las funciones de la interfaz gráfica.
- (Opcional) Integra con CI/CD para pruebas automatizadas.

## Estilo de Código
- Sigue PEP8.
- Usa docstrings para funciones/clases públicas.
- Mantén la interfaz de usuario y la lógica lo más separadas posible.

## Registro y Depuración
- Usa `log_info(msg)`, `log_warning(msg)`, `log_error(msg)` en cualquier parte del código para entradas de registro personalizadas.
- Todos los registros se guardan en `traceback.log` y se muestran en el Visor de Registros.
- El Visor de Registros admite filtrado por TODOS, INFORMACIÓN, ADVERTENCIA, ERROR.
- Las excepciones no capturadas se registran automáticamente y se muestran en el Visor de Registros (con rastreo).

## Soporte y Preguntas
- Abre incidencias en GitHub para informar de errores o solicitar características.
- Consulta `README.md` para información de contacto y contribución.

---

## Temas Avanzados

### Referencia de la API

La aplicación es modular: la lógica principal está en `struttura/`, la interfaz gráfica en `gui/`.

**Clases y funciones principales:**
- `MainWindow` (`gui/main_window.py`): Lógica principal de la interfaz gráfica y manejo de eventos.
- `gen_key`, `export_pubkey`, `clear_fields`, etc.: Métodos para operaciones criptográficas.
- `Help`, `About`, `LogViewer`, etc.: Diálogos y utilidades en `struttura/`.
- `get_version()` (`struttura/version.py`): Devuelve la cadena de versión actual.

Para más información, lee los docstrings en el código y consulta `docs/user_guide.md` para el flujo de uso.

### Ejemplos de Extensión

#### Añadir un Nuevo Algoritmo de Clave
1. En `gui/main_window.py`, localiza el menú desplegable de selección de algoritmo.
2. Añade tu nuevo algoritmo (ej. ECC, Ed25519) a las opciones del menú.
3. En la lógica de generación de claves, implementa el manejo para el nuevo algoritmo usando `pgpy`.
4. Prueba exhaustivamente y actualiza la documentación.

#### Añadir un Widget Personalizado
1. Crea tu widget en `gui/widgets.py` o en un archivo nuevo.
2. Impórtalo y úsalo en `main_window.py` donde sea necesario.
3. Sigue las convenciones de estilo de ttkbootstrap para mantener la consistencia.

### Diagrama de Arquitectura

A continuación se muestra una descripción general de la arquitectura en texto simple:

```
Aplicación OpenPGP GUI
│
├── main.py (punto de entrada)
│
├── gui/
│   ├── main_window.py (clase MainWindow, lógica de eventos)
│   ├── widgets.py (widgets personalizados)
│   └── ...
│
├── struttura/
│   ├── help.py, about.py, version.py (diálogos, control de versiones)
│   ├── menu.py (lógica de la barra de menú)
│   └── ...
│
├── docs/ (documentación)
├── requirements.txt
└── ...
```

Para un diagrama visual, consulta [docs/architecture.png](architecture.png) (añade tu propio PNG para más detalle).

# Preguntas Frecuentes

**P: ¿Puedo usar esta aplicación sin conexión a internet?**  
R: ¡Sí! Todas las operaciones criptográficas se realizan localmente para garantizar la privacidad.

**P: ¿Cómo exporto mi clave pública?**  
R: Usa el botón 'Exportar Clave Pública' o la opción en el menú Archivo.

**P: ¿Qué algoritmos son compatibles?**  
R: Actualmente RSA; próximamente se añadirán más (ECC, Ed25519).

**P: ¿Dónde se guardan mis claves?**  
R: Las claves se guardan solo donde tú elijas. No hay subidas automáticas ni almacenamiento en la nube.

**P: ¿Cómo obtengo ayuda?**  
R: Usa el menú Ayuda o lee la documentación en la carpeta docs/.
