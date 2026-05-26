# Metodologia

TotisGdB sigue una organizacion propia de aplicaciones ASP.NET Core MVC, con separacion entre interfaz, controladores, modelos, persistencia y utilidades transversales.

## Organizacion tecnica

- **Modelo MVC:** divide responsabilidades entre presentacion, coordinacion de flujos y representacion de datos.
- **Persistencia administrada:** Entity Framework Core permite mantener el modelo relacional y sus cambios de forma controlada.
- **Vistas por perfil:** la interfaz se organiza segun responsabilidades funcionales.
- **Componentes compartidos:** elementos comunes de navegacion y layout reducen duplicacion visual.
- **Utilidades transversales:** tareas comunes, como correo y aprobaciones, se aislan de los controladores principales.

## Practicas recomendadas

- Mantener cambios funcionales pequenos y revisables.
- Documentar nuevas reglas de negocio a nivel funcional.
- Agregar validaciones tanto en interfaz como en servidor.
- Probar flujos completos antes de publicar cambios.
- Revisar que reportes y documentos reflejen correctamente los estados de los activos.
- Mantener la documentacion publica sincronizada con cambios relevantes del sistema sin exponer implementacion privada.

## Revision antes de publicar documentacion

Antes de publicar cambios en este repo publico, se recomienda revisar:

- Que no existan archivos privados adjuntos.
- Que no se hayan pegado fragmentos de codigo fuente.
- Que no aparezcan datos reales de usuarios, activos o infraestructura.
- Que los diagramas sean generales y no revelen nombres internos.
- Que la terminologia sea comprensible para revisores externos.

## Despliegue documental

La documentacion se despliega como sitio estatico mediante GitHub Pages. El flujo de publicacion compila el sitio y publica el resultado cuando hay cambios en la rama principal.
