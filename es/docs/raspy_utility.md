---
lang: es
lang-niv: font
lang-ref: 021-jbk
layout: page
title: 'Utilidad RasPY'
---

# Utilidad RasPY

<div align="center">
  <img src="../images/logo.png" alt="Logo de Utilidad RasPY" width="50%">
</div>

## Bienvenido a la documentación de Utilidad RasPY

Utilidad RasPY es una aplicación completa para controlar y monitorear pines GPIO de Raspberry Pi a través de una interfaz gráfica intuitiva o API REST.

## Tabla de Contenidos

### Introducción
- [Instalación](installazione.md)
- [Guía](guida.md)

### Desarrollo
- [Desarrollo](sviluppo.md)
- [API](api.md)
- [Interfaz Gráfica](gui.md)
- [Ejemplos](esempi.md)

### Recursos Adicionales
- [Registro de Cambios](changelog.md)
- [Preguntas Frecuentes](faq.md)

### Comunidad
- [Contribuir](contribuire.md)
- [Agradecimientos](ringraziamenti.md)

## Características Principales

### ✅ **Interfaz Gráfica Moderna**
- Tema claro/oscuro
- Soporte multilingüe
- Visualización en tiempo real del estado de los pines
- Integración con bandeja del sistema

### 🔌 **Soporte Completo para GPIO**
- Control de pines digitales de entrada/salida
- Simulador integrado para desarrollo
- Detección automática de hardware
- Soporte para GPIO remoto

### 🌐 **Interfaz Web**
- Servidor web integrado
- Diseño adaptable para móvil/escritorio
- Actualizaciones en tiempo real
- Documentación de API integrada

## Inicio Rápido

1. [Instalación](installazione.md) - Cómo instalar y configurar Utilidad RasPY
2. [Guía](guida.md) - Guía de uso de la aplicación
3. [API](api.md) - Documentación de la API para desarrolladores
4. [Desarrollo](sviluppo.md) - Guía de desarrollo y contribución

## Guía del Usuario

### Interfaz Gráfica

La interfaz gráfica de Utilidad RasPY 4 está diseñada para ser intuitiva y fácil de usar.

#### Menú Principal

- **Archivo**: Controles generales de la aplicación
- **GPIO**: Gestión de pines GPIO y simulador
- **Vista**: Personalización de la interfaz
- **Ayuda**: Documentación e información

#### Control de GPIO

1. Abra la ventana de control de GPIO desde el menú
2. Seleccione el pin a controlar
3. Use los botones para cambiar el estado de los pines
4. Monitoree el estado en tiempo real

#### Simulador de GPIO
El simulador permite probar código sin hardware físico:

1. Inicie el simulador desde el menú GPIO
2. Use la interfaz para simular entradas/salidas
3. Los cambios se reflejan en tiempo real

### Registro y Depuración
La aplicación registra eventos importantes en el archivo `logs/app.log`. Use el Visor de Registros integrado para:

- Filtrar mensajes por nivel (INFO, ADVERTENCIA, ERROR)
- Buscar mensajes específicos
- Exportar registros para análisis

### Atajos de Teclado

- **Ctrl+Q**: Salir de la aplicación
- **F1**: Mostrar ayuda
- **Ctrl+L**: Abrir visor de registros
- **F5**: Actualizar interfaz

## Referencia de la API

### Visión General

La API REST de Utilidad RasPY 4 permite controlar pines GPIO mediante peticiones HTTP.
Todas las respuestas están en formato JSON.

### Puntos Finales Disponibles

#### `GET /api/gpio`

Devuelve el estado de todos los pines GPIO configurados.

**Ejemplo de respuesta:**

```json
{
  "17": {"state": 0, "mode": "out", "description": "LED Rojo"},
  "18": {"state": 1, "mode": "in", "description": "Botón"}
}
```

#### `GET /api/gpio/<int:pin>`

Devuelve el estado de un pin específico.

**Parámetros:**
- `pin`: Número del pin GPIO

**Códigos de estado:**
- 200: Operación exitosa
- 404: Pin no encontrado

**Ejemplo de respuesta:**

```json
{
  "state": 0,
  "mode": "out",
  "description": "LED Rojo"
}
```

#### `POST /api/gpio/<int:pin>/on`

Enciende el pin especificado.

**Parámetros:**
- `pin`: Número del pin GPIO

**Códigos de estado:**
- 200: Operación exitosa
- 400: Pin inválido o no escribible

#### `POST /api/gpio/<int:pin>/off`

Apaga el pin especificado.

**Parámetros:**
- `pin`: Número del pin GPIO

**Códigos de estado:**
- 200: Operación exitosa
- 400: Pin inválido o no escribible

## Ejemplos de Uso

### Control de GPIO con Python

```python
import requests

BASE_URL = "http://localhost:5000/api/gpio"

# Obtener estado de todos los pines
response = requests.get(f"{BASE_URL}")
print("Estado actual:", response.json())

# Encender el pin 17
response = requests.post(f"{BASE_URL}/17/on")
print("Respuesta de encendido:", response.status_code)
```

## Recursos Útiles

- [Sitio web oficial de Raspberry Pi](https://www.raspberrypi.org/)
- [Documentación de Python](https://www.python.org/)
