---
lang: es
lang-niv: fonto
lang-ref: 010-jbk
layout: doc
order: 1
title: 'Gestor de Filamento 3D'
---

# Gestor de Filamento 3D

![Gestor de Filamento 3D](assets/logo.png)

Una aplicación de escritorio para gestionar tu inventario de filamentos de impresión 3D. Controla materiales, colores, uso, costes y configuraciones de laminado en un solo lugar.

## ✨ Características

* **🌐 Soporte Multilingüe**: Disponible en inglés, español e italiano
* **🎨 Interfaz Moderna**: Diseño limpio con iconos de emoji y soporte de temas (modo claro/oscuro)
* **📊 Gestión Integral de Filamentos**:
  * Almacena información detallada del filamento (marca, material, color, diámetro, etc.)
  * Controla el uso y la cantidad restante de filamento
  * Calcula costes de material
  * Seguimiento de precios e histórico
  * Análisis interactivo de precios con visualizaciones
  * Comparativa de precios entre proveedores
* **⚙️ Integración con Laminadores**:
  * Guarda y gestiona perfiles de laminado (Cura, PrusaSlicer, eQuidiSlicer)
  * Perfiles de impresión personalizados para diferentes impresoras
* **🔍 Búsqueda y Filtrado Avanzado**:
  * Busca por cualquier propiedad del filamento
  * Ordena por cualquier columna
  * Filtra por tipo de material, color o etiquetas personalizadas
* **📂 Importar/Exportar**:
  * Haz copias de seguridad y restaura tu biblioteca de filamentos
  * Comparte perfiles con otros usuarios
  * Soporte para importación/exportación masiva
* **🔒 Seguridad de Datos**:
  * Configuración guardada en el directorio `config/`
  * No se requiere conexión a internet
  * Almacenamiento local de datos

## 🚀 Requisitos

* Python 3.8 o superior
* Paquetes necesarios (se instalan automáticamente):
  * `lxml` - Procesamiento rápido de XML
  * `pillow` - Procesamiento de imágenes para iconos
  * `matplotlib` - Visualización de datos para análisis de precios

## 🛠️ Instalación

### Prerrequisitos

* Python 3.8 o superior
* Git (opcional, para desarrollo)

### Pasos de Instalación

1. **Clona el repositorio** (o descárgalo como ZIP):

   ```bash
   git clone https://github.com/Nsfr750/3D_Filament_Manager.git
   cd 3D_Filament_Manager
   ```

2. **Crea y activa un entorno virtual** (recomendado):

   ```bash
   # En Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # En macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Instala las dependencias**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Ejecuta la aplicación**:

   ```bash
   python main.py
   ```

### Almacenamiento de Datos

* Los perfiles de filamento se guardan en el directorio `fdm/`
* La configuración de la aplicación se guarda en el directorio `config/`
* Los registros se escriben en el directorio `logs/`

## 🤝 Contribuciones

¡Agradecemos las contribuciones! Aquí hay formas en que puedes ayudar:

* Informa de errores abriendo un [issue](https://github.com/Nsfr750/3D_Filament_Manager/issues)
* Sugiere nuevas características o mejoras
* Envía solicitudes de extracción con cambios de código
* Ayuda a mejorar la documentación
* Traduce la aplicación a nuevos idiomas

### Configuración para Desarrollo

1. Haz un fork del repositorio
2. Crea una rama de características (`git checkout -b feature/increible-funcionalidad`)
3. Guarda tus cambios (`git commit -m 'Añade una funcionalidad increíble'`)
4. Sube los cambios a la rama (`git push origin feature/increible-funcionalidad`)
5. Abre una Solicitud de Extracción

### Estilo de Código

* Sigue las pautas de [PEP 8](https://www.python.org/dev/peps/pep-0008/)
* Usa sugerencias de tipos para mayor claridad del código
* Escribe cadenas de documentación para todas las funciones y clases públicas

## 📜 Licencia

Este proyecto está bajo la **Licencia Pública General de GNU v3.0**. Consulta el archivo [LICENCIA](LICENCIA) para más detalles.

## 🙏 Apoyo

Si encuentras útil este proyecto, considera apoyar su desarrollo:

* ⭐ Dale una estrella al repositorio
* 🐛 Informa de problemas
* 💡 Sugiere nuevas características
* 💰 [Patrocina el proyecto en GitHub](https://github.com/sponsors/Nsfr750)

## 📞 Contacto

* GitHub: [@Nsfr750](https://github.com/Nsfr750)
* Correo electrónico: nsfr750@yandex.com

---

### Apoya al Desarrollador

Si esta aplicación te resulta útil, por favor considera apoyar al desarrollador:

* **PayPal**: [https://paypal.me/3dmega](https://paypal.me/3dmega)
* **GitHub**: [https://github.com/Nsfr750](https://github.com/Nsfr750)
