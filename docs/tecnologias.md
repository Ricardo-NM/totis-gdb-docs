# Tecnologías

TotisGdB utiliza un conjunto de tecnologías orientadas a aplicaciones web empresariales, persistencia relacional, autenticación corporativa y generación de documentos administrativos.

## Plataforma

- **.NET 8:** Plataforma principal de ejecución.
- **ASP.NET Core MVC:** Patrón de aplicación web basado en controladores, modelos y vistas.
- **Entity Framework Core:** Acceso a datos y administración del modelo relacional.
- **SQL Server:** Motor relacional usado para almacenar información operativa del sistema.
- **Active Directory:** Integración con perfiles corporativos para validar el acceso con las mismas credenciales del usuario en el entorno Windows.
- **IIS sobre Windows Server:** Hospedaje de la aplicación en producción mediante Internet Information Services.

## Interfaz web

- **Bootstrap:** Estilos base, estructura visual y componentes responsivos.
- **jQuery:** Apoyo para interacciones en cliente.
- **jQuery Validation:** Validación de formularios en interfaz.
- **jQuery Validation Unobtrusive:** Integración de reglas de validación con vistas MVC.

## Documentos, reportes y archivos

- **DinkToPdf:** Soporte para conversión de contenido a PDF.
- **QuestPDF:** Generación programática de documentos PDF.
- **DocumentFormat.OpenXml:** Manipulación de documentos de oficina.
- **DocX:** Creación y edición de documentos Word.
- **NPOI:** Lectura y escritura de archivos de hoja de cálculo.
- **X.PagedList.Mvc.Core:** Paginación de listados en vistas MVC.
- **Newtonsoft.Json:** Serialización y manejo de estructuras JSON dentro de la aplicación.

## Seguridad de plataforma

- Inicio de sesión integrado con Active Directory.
- Autenticación basada en cookies.
- Sesiones de usuario con expiración.
- Acceso diferenciado por perfil funcional.
- Uso de HTTPS en ambientes no locales.

## Principio de documentación pública

Las tecnologías se documentan por su propósito dentro del sistema, no por configuraciones privadas ni implementaciones específicas.
