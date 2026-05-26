# Flujos Principales

Esta seccion resume los procesos principales cubiertos por TotisGdB. Los diagramas muestran el comportamiento general sin exponer reglas internas ni detalles sensibles.

## Inicio de sesion

```mermaid
flowchart TD
    A[Usuario ingresa credenciales] --> B[Validacion de identidad]
    B --> C{Acceso valido}
    C -->|Si| D[Creacion de sesion]
    C -->|No| E[Mensaje de acceso no autorizado]
    D --> F[Redireccion a modulo segun perfil]
```

El sistema utiliza autenticacion por cookies y sesiones con expiracion. Cada perfil accede a funciones acordes con sus responsabilidades.

## Carga de activos desde hoja de calculo

```mermaid
flowchart TD
    A[Usuario autorizado selecciona archivo] --> B[Validacion de estructura]
    B --> C{Archivo aceptado}
    C -->|Si| D[Procesamiento de registros]
    C -->|No| E[Notificacion de errores]
    D --> F[Actualizacion de informacion]
    F --> G[Consulta o reporte]
```

Este flujo permite alimentar informacion operativa de activos desde archivos tabulares, manteniendo validaciones previas antes de actualizar datos.

## Asignacion de activos

```mermaid
flowchart TD
    A[Seleccion de activos] --> B[Definicion de responsable]
    B --> C[Solicitud de asignacion]
    C --> D[Revision correspondiente]
    D --> E{Decision}
    E -->|Aprobada| F[Registro de asignacion]
    E -->|Rechazada| G[Registro de observacion]
    F --> H[Documento responsivo]
```

La asignacion vincula activos con responsables y puede generar documentos de respaldo para control administrativo.

## Traspaso, baja y devolucion

```mermaid
flowchart LR
    A[Solicitud] --> B[Revision]
    B --> C{Resultado}
    C -->|Aprobacion| D[Actualizacion de estatus]
    C -->|Rechazo| E[Observacion registrada]
    D --> F[Historial de movimiento]
```

Estos procesos comparten una estructura general: solicitud, revision, decision, actualizacion del estado del activo y registro en historial.

## Reportes y documentos

Los reportes permiten consultar informacion filtrada y exportar resultados para seguimiento administrativo. Los documentos generados respaldan procesos como cartas responsivas y evidencias de movimiento.
