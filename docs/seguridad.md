# Seguridad

La seguridad de TotisGdB se apoya en controles de acceso, sesiones de usuario, separación de perfiles, autenticación corporativa y protección de información sensible.

## Autenticación y sesiones

- Inicio de sesión integrado con Active Directory en un entorno Windows.
- Validación automática con las mismas credenciales del perfil corporativo de cada usuario.
- Autenticación basada en cookies HTTP para mantener la sesión de la aplicación.
- Expiración de sesión por inactividad.
- Políticas de cookie orientadas a reducir exposición en navegador.
- Redirección a vistas de acceso denegado cuando el perfil no tiene permisos.

## Control por perfil

El sistema separa funcionalidades por perfil operativo. Esta división reduce accesos innecesarios y permite que cada tipo de usuario interactúe solo con los procesos que le corresponden.

Perfiles funcionales documentados:

- Usuario.
- Jefatura.
- Control.
- Autorización.
- Administración inicial.

## Aprobaciones y trazabilidad

Los procesos sensibles, como asignaciones, bajas, devoluciones y traspasos, se apoyan en revisión por perfiles responsables y registros de historial. Las decisiones relevantes quedan asociadas al proceso para consulta posterior.
