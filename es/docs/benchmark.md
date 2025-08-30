---
lang: es
lang-niv: fonto
lang-ref: 023-jbk
layout: doc
order: 14 # Opcional: para ordenar en el menú
title: 'benchmark'
---

[![Licencia: GPL v3](https://img.shields.io/badge/Licencia-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Estilo de código: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Una herramienta moderna de evaluación comparativa en Python desarrollada con PySide6, que proporciona una interfaz de usuario intuitiva para ejecutar y analizar pruebas Pystone y otros benchmarks.

## 📥 Instalación

### Requisitos previos

- Python 3.9 o superior
- Windows o Linux

### Inicio rápido

1. Clona el repositorio:

   ```bash
   git clone https://github.com/Nsfr750/benchmark.git
   cd benchmark
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

## ✨ Características

- **Interfaz de usuario moderna**: Interfaz limpia y receptiva construida con PySide6
- **Evaluación comparativa completa**:
  - Duración personalizable de las pruebas
  - Seguimiento en tiempo real del progreso
  - Resultados detallados con estadísticas
  - Comparación con datos históricos
- **Registro**:
  - Registros detallados de operaciones
  - Filtrado de registros por nivel
  - Rotación de archivos de registro
- **Soporte multilingüe**:
  - Inglés (en)
  - Italiano (it)
- **Accesibilidad**:
  - Atajos de teclado
  - Modo de alto contraste
  - Tamaño de texto ajustable

## ⌨️ Atajos de teclado

- `Ctrl+L`: Ver registros de la aplicación
- `F1`: Mostrar ayuda
- `Esc`: Cerrar diálogos
- `Ctrl+Q`: Salir de la aplicación

## 📊 Uso

1. Establece el número de iteraciones para la evaluación
2. Haz clic en "Iniciar evaluación" para comenzar
3. Supervisa el progreso en tiempo real
4. Consulta los resultados detallados y las estadísticas
5. Accede a los registros para la resolución de problemas

## 📂 Estructura del proyecto

```
benchmark/
├── .github/                            # GitHub Actions
│   ├── workflows/                      # Flujos de trabajo de GitHub Actions
│   │   └── ci-cd.yml                   # Canalización CI/CD
│   ├── issues/                         # Incidencias de GitHub
│   |   └── templates/                  # Plantillas de incidencias
│   └── FUNDING.yml                     # Archivo de financiación
├── assets/                             # Archivos de recursos
├── config/                             # Archivos de configuración
│   ├── config.json                     # Archivo de configuración
│   └── updates.json                    # Caché de actualizaciones
├── docs/                               # Documentación
│   ├── images/                         # Imágenes de documentación
│   ├── pdf/                            # Documentación en PDF
│   └── USER_GUIDE.md                   # Guía del usuario
├── lang/                               # Archivos de idioma
│   ├── en.json                         # Archivo en inglés
│   └── it.json                         # Archivo en italiano
├── logs/                               # Archivos de registro
├── script/                             # Código fuente
│   ├── __init__.py                     # Inicialización del paquete
│   ├── about.py                        # Diálogo "Acerca de"
│   ├── benchmark_history.py            # Historial de evaluaciones
│   ├── benchmark_tests.py              # Pruebas de evaluación
│   ├── CLI_pystone.py                  # Evaluación Pystone desde línea de comandos
│   ├── config_manager.py               # Gestor de configuración
│   ├── export_results.py               # Exportación de resultados
│   ├── hardware_monitor.py             # Monitor de hardware
│   ├── help.py                         # Diálogo de ayuda
│   ├── history_dialog.py               # Diálogo de historial
│   ├── lang_mgr.py                     # Gestor de idiomas
│   ├── logger.py                       # Configuración de registros
│   ├── menu.py                         # Funcionalidad de la barra de menú
│   ├── settings.py                     # Diálogo de configuración
│   ├── sponsor.py                      # Diálogo de patrocinadores
│   ├── system_info.py                  # Información del sistema
│   ├── test_menu.py                    # Menú de pruebas
│   ├── theme_manager.py                # Gestor de temas
│   ├── updates.py                      # Sistema de actualizaciones
│   ├── version.py                      # Sistema de versionado
│   ├── view_log.py                     # Visor de registros
│   └── visualization.py                # Visualización de evaluaciones
├── tests/                              # Archivos de prueba
│   ├── test_benchmark.py               # Prueba de evaluación
│   ├── test_hardware_monitor.py        # Prueba de monitor de hardware
│   ├── test_monitor_manual.py          # Prueba manual de monitor
│   ├── test_monitor.py                 # Prueba de monitor
│   └── TEST_README.md                  # README de pruebas
├── .gitignore                          # Archivo .gitignore
├── CHANGELOG.md                        # Registro de cambios
├── CONTRIBUTING.md                     # Pautas de contribución
├── LICENSE                             # Archivo de licencia GPLv3
├── main.py                             # Aplicación principal
├── README.md                           # Este archivo
├── requirements.txt                    # Archivo de dependencias
└── TO_DO.md                            # Lista de tareas pendientes
```
