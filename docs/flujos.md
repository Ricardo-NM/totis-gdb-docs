# Flujos Principales

Esta sección resume los procesos principales cubiertos por TotisGdB. Los diagramas muestran el comportamiento general sin exponer reglas internas ni detalles sensibles.

## Inicio de sesión

```mermaid
flowchart TD
    A[Usuario abre el sistema] --> B[Validación con Active Directory]
    B --> C{Perfil corporativo válido}
    C -->|Sí| D[Creación de sesión en la aplicación]
    C -->|No| E[Mensaje de acceso no autorizado]
    D --> F[Redirección a módulo según perfil]
```

El sistema utiliza Active Directory para validar automáticamente al usuario con las credenciales de su perfil corporativo en Windows. Después de esa validación, la aplicación mantiene su sesión web y aplica los permisos funcionales correspondientes.

## Carga de activos desde hoja de cálculo

```mermaid
flowchart TD
    A[Usuario autorizado selecciona archivo] --> B[Validación de estructura]
    B --> C{Archivo aceptado}
    C -->|Sí| D[Procesamiento de registros]
    C -->|No| E[Notificación de errores]
    D --> F[Actualización de información]
    F --> G[Consulta o reporte]
```

Este flujo permite alimentar información operativa de activos desde archivos tabulares, manteniendo validaciones previas antes de actualizar datos.

## Asignación de activos

```mermaid
flowchart TD
    A[Selección de activos] --> B[Definición de responsable]
    B --> C[Solicitud de asignación]
    C --> D[Revisión correspondiente]
    D --> E{Decisión}
    E -->|Aprobada| F[Registro de asignación]
    E -->|Rechazada| G[Registro de observación]
    F --> H[Documento responsivo]
```

La asignación vincula activos con responsables y puede generar documentos de respaldo para control administrativo.

## Traspaso, baja y devolución

```mermaid
flowchart LR
    A[Solicitud] --> B[Revisión]
    B --> C{Resultado}
    C -->|Aprobación| D[Actualización de estatus]
    C -->|Rechazo| E[Observación registrada]
    D --> F[Historial de movimiento]
```

Estos procesos comparten una estructura general: solicitud, revisión, decisión, actualización del estado del activo y registro en historial.

## Reportes y documentos

Los reportes permiten consultar información filtrada y exportar resultados para seguimiento administrativo. Los documentos generados respaldan procesos como cartas responsivas y evidencias de movimiento.
