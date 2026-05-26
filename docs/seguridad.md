# Seguridad

La seguridad de TotisGdB se apoya en controles de acceso, sesiones de usuario, separacion de perfiles y proteccion de informacion sensible.

## Autenticacion y sesiones

- Inicio de sesion mediante credenciales de usuario.
- Autenticacion basada en cookies HTTP.
- Expiracion de sesion por inactividad.
- Politicas de cookie orientadas a reducir exposicion en navegador.
- Redireccion a vistas de acceso denegado cuando el perfil no tiene permisos.

## Control por perfil

El sistema separa funcionalidades por perfil operativo. Esta division reduce accesos innecesarios y permite que cada tipo de usuario interactue solo con los procesos que le corresponden.

Perfiles funcionales documentados:

- Usuario.
- Jefatura.
- Control.
- Autorizacion.
- Administracion inicial.

## Aprobaciones y trazabilidad

Los procesos sensibles, como asignaciones, bajas, devoluciones y traspasos, se apoyan en revision por perfiles responsables y registros de historial. Las decisiones relevantes quedan asociadas al proceso para consulta posterior.

## Proteccion de datos sensibles

No deben publicarse:

- Cadenas de acceso a datos.
- Nombres de servidores o infraestructura interna.
- Correos reales o identificadores de empleados.
- Datos reales de activos.
- Plantillas documentales internas.
- Capturas sin censura.
- Archivos de configuracion del entorno privado.

## Seguridad de esta documentacion publica

Este repositorio solo debe contener informacion descriptiva. Cualquier contribucion debe revisarse para confirmar que no incluya codigo fuente, credenciales, datos reales, configuracion privada ni archivos internos del sistema.
