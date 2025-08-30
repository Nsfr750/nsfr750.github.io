---
lang: es
lang-niv: fonto
lang-ref: 017-jbk
layout: page
title: 'Nidec CommanderCDE'
---

# Nidec CommanderCDE

Una aplicación GUI completa en Python para controlar y monitorear variadores Nidec Commander CDE a través de Modbus RTU.

## ✨ Características

- **Soporte Multilingüe**: Interfaz completa en inglés e italiano con cambio de idioma dinámico
- **Soporte Multi-modelo**: Compatible con los modelos de variadores CDE400, CDE550, CDE750 y CDE1100S
- **Control del Variador**:
  - Conexión a variadores Nidec Commander CDE vía RS-485/Modbus RTU
  - Control de velocidad y dirección del motor
  - Arranque/Parada del variador
  - Monitoreo en tiempo real del estado y diagnóstico del variador
  - Detección de fallos y función de reinicio
  - Respaldo y restauración de parámetros
- **Interfaz de Usuario**:
  - Interfaz moderna con pestañas y controles intuitivos
  - Panel integral con métricas en tiempo real
  - Barra de estado con información de conexión y estado del variador
  - Diseño receptivo con soporte para temas Claro/Oscuro
  - Elementos de interfaz personalizables
- **Gestión de Datos**:
  - Monitoreo y registro en tiempo real de parámetros del variador
  - Exportación de datos a CSV/Excel
  - Visualización gráfica de tendencias de parámetros
  - Intervalos de registro de datos configurables
- **Diagnósticos**:
  - Monitoreo integral de parámetros
  - Historial de fallos y registro
  - Indicadores de estado del sistema
  - Métricas de rendimiento en tiempo real

## 🆕 Novedades en la v0.0.4

### Nuevas Características
- Añadido soporte para múltiples modelos de variadores Nidec (CDE400, CDE550, CDE750, CDE1100S)
- Traducciones completas al italiano para todos los elementos de la interfaz
- Sistema de ayuda mejorado con documentación detallada
- Tema azul para mejor legibilidad en secciones de ayuda

### Mejoras
- Interfaz de usuario actualizada para mejor experiencia
- Mensajes de error y registro mejorados
- Rendimiento optimizado para monitoreo en tiempo real
- Resueltos problemas de compatibilidad con PyQt6
- Corregido el cambio de idioma en los diálogos de ayuda

## 🚀 Requisitos

- Python 3.8 o superior
- PyQt6 >= 6.6.1
- pyserial >= 3.5
- pymodbus >= 3.5.4
- PyQt6-QScintilla >= 2.14.1
- python-dotenv >= 1.0.0

## 🛠 Instalación y Configuración

1. Clona el repositorio:

   ```bash
   git clone https://github.com/Nsfr750/nidec-commandercde.git
   cd nidec-commandercde
   ```

2. Crea y activa un entorno virtual (recomendado):

   ```bash
   python -m venv venv
   # En Windows:
   .\venv\Scripts\activate
   # En Unix o MacOS:
   # source venv/bin/activate
   ```

3. Instala los paquetes necesarios:

   ```bash
   pip install -r requirements.txt
   ```

## 🚀 Uso Básico

1. Conecta tu variador Nidec Commander CDE a tu computadora mediante un adaptador RS-485
2. Inicia la aplicación:

   ```bash
   python main.py
   ```

3. Selecciona el puerto COM apropiado y la velocidad en baudios
4. Haz clic en 'Conectar' para establecer la comunicación con el variador
5. Utiliza la interfaz para controlar y monitorear el variador

## Configuración de Conexión

- Velocidad en baudios: 9600
- Bits de datos: 8
- Paridad: Par
- Bits de parada: 1
- Dirección Modbus: 1 (predeterminada, puede cambiarse en los parámetros del variador)

## Notas Importantes

- Este software se proporciona "tal cual" sin garantía alguna
- Siempre asegúrate de realizar las conexiones eléctricas correctamente y seguir las medidas de seguridad al trabajar con variadores de motor
- Las direcciones de registro predeterminadas se basan en configuraciones típicas de variadores Nidec pero pueden necesitar ajustes para tu modelo específico
- Consulta el manual de Nidec CDE 400 Commander para obtener información detallada sobre parámetros y direcciones de registro
