---
lang: es
lang-niv: fonto
lang-ref: 022-jbk
layout: doc
order: 13
title: 'Clima'
---

# Documentación de la Aplicación del Tiempo (v1.6.0)

¡Bienvenido a la documentación de la Aplicación del Tiempo! Esta aplicación proporciona información meteorológica en tiempo real y pronósticos de múltiples proveedores de datos meteorológicos.

## Características

- 🌦️ Condiciones climáticas actuales con métricas detalladas
- 📅 Pronóstico del tiempo a 7 días con desglose por horas
- 📖 Visor de documentación Markdown integrado
- 📊 Visor de registros de la aplicación para diagnóstico
- 🌍 Múltiples proveedores de datos meteorológicos
- 🌐 Soporte multilingüe
- ⭐ Ubicaciones favoritas con historial mejorado
- ⚙️ Configuración y temas personalizables

## Actualizaciones Recientes

Para una lista detallada de cambios, consulte el archivo [CHANGELOG.md](CHANGELOG.md).

## Empezando

1. [Guía de Instalación](installation.md) - Cómo instalar y configurar la aplicación
2. [Guía del Usuario](usage.md) - Cómo usar la aplicación
3. [Configuración](configuration.md) - Cómo configurar la aplicación

## Temas Avanzados

- [Proveedores Meteorológicos](providers.md) - Información sobre los proveedores de datos meteorológicos compatibles
- [Traducciones](translations.md) - Cómo agregar o modificar traducciones
- [Guía de Desarrollo](development.md) - Cómo contribuir al proyecto
- [Solución de Problemas](troubleshooting.md) - Problemas comunes y soluciones

## Soporte

Para soporte, por favor abra un problema en nuestro [repositorio de GitHub](https://github.com/Nsfr750/weather).

## Licencia

Este proyecto está licenciado bajo la Licencia GPLv3 - consulte el archivo [LICENCIA](https://github.com/Nsfr750/weather/blob/main/LICENSE) para más detalles.

# Guía del Usuario

## Empezando

1. **Iniciar la Aplicación**
   - Haga doble clic en el icono de la aplicación o ejecútela desde la línea de comandos
   - Se abrirá la ventana principal con el clima de la ubicación predeterminada
   - En el primer inicio, se le guiará a través de la configuración inicial

2. **Buscar una Ubicación**
   - Escriba el nombre de una ciudad en el cuadro de búsqueda
   - Presione Enter o haga clic en el botón de búsqueda (🔍)
   - Para resultados más precisos, incluya el código de país (ej: "París, FR")
   - Haga clic derecho en el mapa para seleccionar una ubicación

## Interfaz Principal

### Visualización del Tiempo

- **Tiempo Actual**: Muestra la temperatura, condiciones y detalles adicionales
  - Toque cualquier métrica para alternar entre unidades (ej: °C/°F, km/h/mph)
  - Pase el cursor sobre los íconos para más información

- **Pronóstico a 7 Días**: Muestra el pronóstico del tiempo para los próximos 7 días
  - Haga clic en un día para ver el pronóstico por horas
  - Probabilidad de precipitación codificada por colores
  - Incluye rangos de temperatura y condiciones climáticas para cada día

- **Detalles del Tiempo**: Incluye:
  - Sensación térmica
  - Humedad y punto de rocío
  - Velocidad y dirección del viento
  - Presión y visibilidad
  - Índice UV y calidad del aire
  - Horarios de salida y puesta del sol

### Navegación

- **Barra de Búsqueda**: Encuentre el clima para cualquier ubicación
  - Las búsquedas recientes se guardan automáticamente
  - Busque por nombre de ciudad, código postal o coordenadas

- **Selector de Tema**: Cambie entre tema claro, oscuro o del sistema

- **Barra de Menú**: Acceda a funciones y configuraciones adicionales
  - Archivo: Nueva ventana, configuración, salir
  - Ver: Alternar elementos de la interfaz, actualizar datos, mapas y radar
  - Favoritos: Administrar ubicaciones guardadas
  - Ayuda: Visor de documentación, visor de registros, acerca de, buscar actualizaciones

## Mapas y Radar Meteorológico

La función de Mapas y Radar Meteorológico proporciona visualizaciones interactivas de patrones y condiciones climáticas.

### Acceso a los Mapas Meteorológicos

1. Haga clic en **Ver** en la barra de menú
2. Seleccione **Mapas y Radar Meteorológico**
3. Se abrirá el diálogo de Mapas Meteorológicos con varias pestañas

### Características

#### Pestaña Radar
- **Tipo de Mapa**: Cambie entre diferentes mapas base (OpenStreetMap, OpenTopoMap, Stamen Terrain)
- **Capa**: Alternar entre superposiciones de radar y satélite
- **Buscar**: Encuentre ubicaciones por nombre o coordenadas

#### Pestaña Temperatura
- Vea las variaciones de temperatura por regiones
- Alternar entre Celsius y Fahrenheit
- Ajuste la opacidad de la superposición de temperatura

#### Pestaña Precipitación
- Vea la precipitación actual y pronosticada
- Alternar entre diferentes capas de precipitación
- Vea lluvia, nieve y otros tipos de precipitación

#### Pestaña Viento
- Visualice la velocidad y dirección del viento
- Alternar entre flechas o líneas de flujo
- Ajuste las unidades de velocidad del viento (km/h, m/s, mph, nudos)

### Uso del Mapa
- **Zoom**: Use la rueda del ratón o los botones +/-
- **Desplazamiento**: Haga clic y arrastre el mapa
- **Búsqueda**: Ingrese una ubicación en el cuadro de búsqueda y presione Enter
- **Capas**: Active diferentes capas meteorológicas usando los controles
- **Pantalla Completa**: Haga clic en el botón de pantalla completa para una vista más grande

### Consejos
- El mapa se centrará automáticamente en su ubicación actual si los servicios de ubicación están habilitados
- Haga clic en el mapa para obtener información meteorológica detallada de esa ubicación
- Use los controles de línea de tiempo para ver datos de pronóstico para diferentes momentos
- Haga clic derecho en el mapa para establecer un marcador u obtener coordenadas

## Características

### Favoritos

- **Agregar a Favoritos**: Haga clic en la estrella (☆) para guardar una ubicación

- **Ver Favoritos**: Acceda a las ubicaciones guardadas desde el menú Favoritos
  - Reordene los favoritos arrastrando y soltando
  - Haga clic derecho para acciones rápidas

- **Sincronizar Favoritos**: Habilite la sincronización en la nube en la configuración

- **Eliminar de Favoritos**: Haga clic en la estrella llena (★) para eliminar

### Configuración

1. Haga clic en el ícono de engranaje (⚙️) o vaya a Menú > Configuración
2. Configure opciones como:
   - **General**: Idioma, tema, unidades
   - **Tiempo**: Configuración del proveedor, frecuencia de actualización
   - **Pantalla**: Diseño, animaciones, tamaño de fuente
   - **Notificaciones**: Alertas meteorológicas, alertas de lluvia
   - **Avanzado**: Caché, registro, opciones de desarrollador
3. Haga clic en "Guardar" para aplicar los cambios

### Interfaz de Línea de Comandos

```bash
# Uso básico
weather-app [ubicación] [opciones]

# Ejemplos
weather-app "Nueva York, US"
weather-app --provider openweathermap --units metric
weather-app --config ~/.config/weather/config.ini

# Opciones
  -h, --help            Mostrar mensaje de ayuda y salir
  -v, --version         Mostrar información de versión
  -c, --config ARCHIVO  Especificar archivo de configuración
  -d, --debug           Habilitar modo depuración
  --provider PROVEEDOR  Establecer proveedor meteorológico
  --units {metric,imperial}
                        Establecer sistema de unidades
  --lang IDIOMA         Establecer código de idioma
  --tema {claro,oscuro,sistema}
                        Establecer tema de color
  --sin-interfaz        Ejecutar en modo consola
```

## Atajos de Teclado

### Atajos Globales

| Atajo | Acción |
|-------|--------|
| `Ctrl + F` | Enfocar barra de búsqueda |
| `Ctrl + ,` | Abrir Configuración |
| `Ctrl + Q` | Salir de la Aplicación |
| `F1` | Mostrar Ayuda |
| `Esc` | Cerrar diálogos o borrar búsqueda |
| `F5` | Actualizar datos meteorológicos |
| `Ctrl + R` | Actualizar todos los datos |
| `Ctrl + W` | Cerrar ventana actual |
| `Ctrl + N` | Nueva ventana |

### Atajos de Navegación

| Atajo | Acción |
|-------|--------|
| `Ctrl + Tab` | Cambiar entre ubicaciones |
| `Ctrl + F` | Alternar favoritos |
| `Ctrl + L` | Alternar lista de ubicaciones |
| `Ctrl + M` | Alternar vista de mapa |

## Consejos y Trucos

- **Clic derecho** en cualquier tarjeta del tiempo para acciones rápidas
- **Doble clic** en la temperatura para alternar entre Celsius y Fahrenheit
- **Clic central** en el mapa para establecer una ubicación personalizada
- Use la **rueda del ratón** en el pronóstico para desplazarse por las horas
- **Arrastre y suelte** para reordenar las ubicaciones favoritas
- **Fije** la ventana para que permanezca sobre otras aplicaciones
- Use el **icono de la bandeja del sistema** para acceso rápido

### Visor de Documentación

- Acceda a la documentación Markdown integrada desde el menú Ayuda
- Navegue por documentación completa
- Funcionalidad de búsqueda para encontrar temas específicos
- Zoom para mejor legibilidad
- Tabla de contenidos para navegación fácil

### Visor de Registros

- Vea los registros de la aplicación desde el menú Ayuda
- Filtre registros por nivel (Depuración, Información, Advertencia, Error)
- Busque en los mensajes de registro
- Copie registros al portapapeles para solución de problemas

### Mapas Meteorológicos
- Acceda a mapas meteorológicos desde el menú Ver
- Mapa interactivo con múltiples capas:
  - Temperatura
  - Precipitación
  - Velocidad del viento
  - Nubosidad
- Desplácese y haga zoom para explorar diferentes regiones
- Haga clic en el mapa para obtener el clima de esa ubicación

## Solución de Problemas

Si encuentra algún problema:
1. Verifique su conexión a Internet
2. Verifique sus claves de API en Configuración
3. Intente cambiar a un proveedor meteorológico diferente
4. Revise los registros de la aplicación en busca de errores
5. Reinicie la aplicación
6. Restablezca la configuración si es necesario

Para obtener ayuda adicional, visite nuestro [repositorio de GitHub](https://github.com/Nsfr750/weather) o consulte la [Guía de Solución de Problemas](troubleshooting.md).

## Comentarios

¡Apreciamos sus comentarios! Por favor, háganos saber:
- Qué características le gustaría ver
- Cualquier error que encuentre
- Su experiencia con la aplicación

Puede enviar comentarios a través de la aplicación (Ayuda > Enviar Comentarios) o en nuestra página de [Problemas de GitHub](https://github.com/Nsfr750/weather/issues).
