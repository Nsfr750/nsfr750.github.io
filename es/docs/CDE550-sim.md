---
lang: es
lang-niv: font
lang-ref: 012-jbk
layout: doc
order: 3
title: 'CDE550-Sim'
---

# Simulador Nidec Commander CDE 550

[![Versión de Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Licencia: GPL v3](https://img.shields.io/badge/Licencia-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Versión](https://img.shields.io/badge/versi%C3%B3n-0.0.2-green.svg)](CHANGELOG.md)

Simulador de software para el inversor Nidec Commander CDE 550 con interfaz gráfica, desarrollado en Python con PyQt6.

## Novedades en la Versión 0.0.2

- **Localización completa** de la interfaz de usuario al español
- **Manejo mejorado de alarmas** con menos falsos positivos
- **Optimizaciones de rendimiento** durante el arranque y variaciones de carga
- **Documentación actualizada** con registro de cambios detallado

## Características

- Simulación realista del comportamiento del inversor Nidec Commander CDE 550
- Interfaz gráfica intuitiva con PyQt6 completamente localizada en español
- Comunicación serie a través de pyserial
- Soporte para comandos de control principales
- Simulación de fallos y alarmas con gestión avanzada
- Monitoreo en tiempo real de parámetros
- Registro de eventos y errores

## Requisitos Previos

- Python 3.8 o superior
- Pip (gestor de paquetes de Python)
- Entorno virtual de Python (recomendado)

## Instalación

1. Clona el repositorio:
   ```bash
   git clone https://github.com/Nsfr750/CDE550-sim.git
   cd CDE550-sim
   ```

2. Crea y activa un entorno virtual (opcional pero recomendado):
   ```bash
   # En Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # En macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Instala las dependencias:
   ```bash
   pip install -r requirements.txt
   ```

## Uso

1. Inicia el simulador:
   ```bash
   python main.py
   ```

2. La interfaz gráfica mostrará:
   - Estado del inversor
   - Parámetros de operación
   - Registro de eventos
   - Controles de simulación

3. Para conexión serie:
   - Ve a Conexión -> Conectar
   - Selecciona el puerto COM deseado
   - Configura la velocidad de comunicación (baudios)
   - Haz clic en "Conectar"

## Comandos Serie Soportados

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `RUN` | Inicia el inversor | `RUN` |
| `STOP` | Detiene el inversor | `STOP` |
| `RST` | Reinicia las alarmas | `RST` |
| `FREQ <valor>` | Establece la frecuencia (Hz) | `FREQ 50.0` |
| `DIR <1\|-1>` | Establece la dirección | `DIR 1` (adelante) |
| `STATUS` | Muestra el estado completo | `STATUS` |
| `HELP` | Muestra la lista de comandos | `HELP` |

## Estructura del Proyecto

```
CDE550-sim/
├── main.py              # Punto de entrada de la aplicación
├── inverter_sim.py      # Lógica de simulación del inversor
├── serial_handler.py    # Manejo de comunicación serie
├── script/              # Interfaz de usuario y archivos de ayuda
│   ├── help.py          # Ventana de ayuda
│   ├── serial_dialog.py # Ventana de conexión serie
│   └── version.py       # Gestión de versiones
├── requirements.txt     # Dependencias del proyecto
├── README.md            # Documentación principal
└── CHANGELOG.md         # Registro de cambios
```

## Contribuciones

¡Las contribuciones son bienvenidas! Para proponer mejoras:

1. Haz un fork del proyecto
2. Crea una rama de características (`git checkout -b feature/CaracteristicaIncreible`)
3. Guarda tus cambios (`git commit -m 'Añade una Característica Increíble'`)
4. Sube los cambios a la rama (`git push origin feature/CaracteristicaIncreible`)
5. Abre una Solicitud de Extracción

## Licencia

Distribuido bajo la Licencia GPL-3.0. Consulta el archivo `LICENSE` para más información.

## Contacto

- Autor: Nsfr750
- Correo: [nsfr750@yandex.com]
- Repositorio: https://github.com/Nsfr750/CDE550-sim

---

<div align="center">
  <sub>Desarrollado con ❤️ por Nsfr750</sub>
</div>
