# Arquitectura

TotisGdB está construido como una aplicación web ASP.NET Core MVC. La solución separa responsabilidades entre controladores, modelos, vistas, utilidades y capa de datos, manteniendo una estructura familiar para aplicaciones empresariales basadas en .NET.

## Vista general

```mermaid
flowchart LR
    U[Usuario web] --> B[Navegador]
    B --> IIS[IIS en Windows Server]
    IIS --> M[Aplicación MVC]
    AD[Active Directory] --> IIS
    M --> C[Controladores]
    C --> D[Capa de datos]
    D --> DB[(Base de datos relacional)]
    C --> V[Vistas]
    C --> DOC[Documentos y reportes]
```

## Capas principales

- **Interfaz web:** Vistas MVC, componentes compartidos de navegación y recursos estáticos.
- **Hospedaje:** La publicación en producción se realiza sobre IIS en un servidor Windows.
- **Identidad corporativa:** El inicio de sesión se integra con Active Directory para aprovechar las credenciales del perfil corporativo de cada usuario.
- **Controladores:** Coordinan flujos de usuario, validan solicitudes, aplican reglas de acceso y preparan respuestas.
- **Modelos:** Representan usuarios, activos, solicitudes y registros de movimiento.
- **Capa de datos:** Usa Entity Framework Core para interactuar con la base de datos relacional.
- **Utilidades:** Concentran apoyo transversal, como envío de correos y generación de identificadores seguros de aprobación.
- **Documentos y reportes:** Integran librerías para exportación, generación de PDF, archivos de oficina y reportes paginados.

## Flujo técnico general

```mermaid
sequenceDiagram
    participant Usuario
    participant Web
    participant IIS
    participant MVC
    participant Datos
    participant Documentos

    Usuario->>Web: Realiza una operación
    Web->>IIS: Solicita acceso al sistema
    IIS->>MVC: Enruta la solicitud validada
    MVC->>Datos: Consulta o registra información
    Datos-->>MVC: Devuelve el resultado
    MVC->>Documentos: Genera archivo cuando aplica
    MVC-->>Web: Responde con vista, archivo o resultado
    Web-->>Usuario: Presenta la información
```

## Persistencia

La persistencia se apoya en una base de datos relacional administrada mediante Entity Framework Core. Las entidades principales cubren usuarios, activos fijos contables, solicitudes y trazabilidad de operaciones.

## Criterio de separación

La documentación pública evita publicar nombres internos de infraestructura, configuraciones reales, cadenas de acceso, migraciones o cualquier detalle que permita reconstruir el entorno privado.
