# Metodología

TotisGdB sigue una organización propia de aplicaciones ASP.NET Core MVC, con separación entre interfaz, controladores, modelos, persistencia y utilidades transversales.

## Organización técnica

- **Modelo MVC:** Divide responsabilidades entre presentación, coordinación de flujos y representación de datos.
- **Persistencia administrada:** Entity Framework Core permite mantener el modelo relacional y sus cambios de forma controlada.
- **Vistas por perfil:** La interfaz se organiza según responsabilidades funcionales.
- **Componentes compartidos:** Elementos comunes de navegación y layout reducen duplicación visual.
- **Utilidades transversales:** Tareas comunes, como correo y aprobaciones, se aíslan de los controladores principales.

## Prácticas recomendadas

- Mantener cambios funcionales pequeños y revisables.
- Documentar nuevas reglas de negocio a nivel funcional.
- Agregar validaciones tanto en interfaz como en servidor.
- Probar flujos completos antes de publicar cambios.
- Revisar que reportes y documentos reflejen correctamente los estados de los activos.
- Mantener la documentación pública sincronizada con cambios relevantes del sistema sin exponer implementación privada.

## Puesta en producción del sistema

La aplicación TotisGdB se publica en un servidor Windows mediante IIS. Este despliegue permite operar el sistema en un entorno corporativo e integrarlo con Active Directory para que los usuarios accedan con sus credenciales institucionales.
