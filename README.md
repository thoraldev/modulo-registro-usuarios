# Formulario de Práctica - Registro de Usuarios

Un proyecto de escritorio C# WinForms diseñado como una práctica avanzada para la captura, validación y registro de datos de usuarios, con generación de reportes en PDF y un sistema de auto-actualización automatizado.


---

## 🚀 Características Principales

Este proyecto no es solo un formulario, sino una demostración de varias tecnologías modernas de .NET:

* **Captura de Datos Completa:** Formulario multi-pestaña para datos generales, identificación, dirección y contacto.
* **Validación en Tiempo Real:** Campos obligatorios marcados y validaciones de entrada.
* **Integración de APIs Externas:**
    * Conexión con la **API de SEPOME** para auto-rellenar la dirección (colonia, municipio, estado) a partir del Código Postal.
    * Carga de catálogos dinámicos (Nacionalidades, Actividades Económicas) desde archivos JSON en GitHub.
* **Generación de Reportes:** Utiliza **QuestPDF** para generar un informe profesional en `.pdf` con todos los datos capturados del usuario.
* **Auto-Actualización:** Integrado con **AutoUpdater.NET**. La aplicación comprueba si hay una nueva versión en este repositorio de GitHub cada vez que se inicia.
* **Despliegue Automatizado (CI/CD):** Configurado con **GitHub Actions** para que cada vez que se cree un nuevo *tag* (ej. `v1.0.0.9`):
    1.  Se compile el proyecto en `Release`.
    2.  Se comprima en un `.zip`.
    3.  Se cree una nueva "Release" en GitHub con el `.zip` adjunto.

---

## 🛠️ Tecnologías Utilizadas

* **Lenguaje:** C#
* **Framework:** .NET 6 (o superior)
* **Plataforma:** Windows Forms (WinForms)
* **Librerías (NuGet):**
    * `AutoUpdater.NET.Official`: Para el sistema de actualizaciones.
    * `QuestPDF`: Para la generación de reportes en PDF.
    * `Newtonsoft.Json`: Para procesar las respuestas de las APIs.
* **Automatización:** GitHub Actions

---

### Sistema de Actualización
La aplicación **buscará actualizaciones automáticamente** al iniciar. Si se encuentra una nueva versión, te notificará y te permitirá descargarla e instalarla con un solo clic.

La versión actual de tu programa se muestra en la barra de título de la ventana.
