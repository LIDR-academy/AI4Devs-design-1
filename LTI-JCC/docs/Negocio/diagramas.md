# Diagramas del Sistema ATS LTI

## 1. Arquitectura del Sistema

```mermaid
graph TD
    A[Portal Web] --> B[API Gateway]
    B --> C[Servicio de Autenticación]
    B --> D[Gestión de Candidatos]
    B --> E[Motor de IA]
    B --> F[Gestión de Vacantes]
    D --> G[(Base de Datos)]
    E --> G
    F --> G
    H[Aplicación Móvil] --> B
```

## 2. Flujo del Proceso de Reclutamiento

```mermaid
flowchart LR
    A[Crear Vacante] --> B[Publicar Oferta]
    B --> C[Recibir CVs]
    C --> D[Filtrado IA]
    D --> E[Evaluación]
    E --> F[Entrevistas]
    F --> G[Selección]
    G --> H[Contratación]
```

## 3. Modelo de Datos Simplificado

```mermaid
erDiagram
    CANDIDATO ||--o{ APLICACION : realiza
    VACANTE ||--o{ APLICACION : tiene
    EMPRESA ||--o{ VACANTE : publica
    CANDIDATO {
        string id
        string nombre
        string email
        string experiencia
        string habilidades
    }
    VACANTE {
        string id
        string titulo
        string descripcion
        string requisitos
        date fecha_publicacion
    }
    APLICACION {
        string id
        string estado
        date fecha_aplicacion
    }
```

## 4. Casos de Uso

```mermaid
graph TD
    subgraph Reclutador
        A[Crear Vacante]
        B[Revisar Candidatos]
        C[Programar Entrevistas]
        D[Generar Reportes]
    end
    
    subgraph Candidato
        E[Registrar Perfil]
        F[Aplicar a Vacante]
        G[Ver Estado]
        H[Actualizar CV]
    end
    
    subgraph Admin
        I[Gestionar Usuarios]
        J[Configurar Sistema]
        K[Monitorear Métricas]
    end
```

## 5. Proceso de Evaluación de Candidatos

```mermaid
stateDiagram-v2
    [*] --> Registrado
    Registrado --> EnRevisión
    EnRevisión --> Preseleccionado
    EnRevisión --> Rechazado
    Preseleccionado --> Entrevista
    Entrevista --> Seleccionado
    Entrevista --> Rechazado
    Seleccionado --> Contratado
    Rechazado --> [*]
    Contratado --> [*]
```

## 6. Arquitectura de Microservicios

```mermaid
graph LR
    A[Frontend] --> B[API Gateway]
    B --> C[Servicio de Usuarios]
    B --> D[Servicio de Candidatos]
    B --> E[Servicio de Vacantes]
    B --> F[Servicio de IA]
    B --> G[Servicio de Reportes]
    C --> H[(Base de Datos)]
    D --> H
    E --> H
    F --> H
    G --> H
```

## 7. Flujo de Integración con Redes Sociales

```mermaid
sequenceDiagram
    participant U as Usuario
    participant ATS as Sistema ATS
    participant API as API Social
    participant DB as Base de Datos

    U->>ATS: Solicita conexión social
    ATS->>API: Solicita autorización
    API->>U: Solicita permiso
    U->>API: Autoriza
    API->>ATS: Token de acceso
    ATS->>API: Obtiene datos
    ATS->>DB: Almacena información
    ATS->>U: Confirma integración
```

## 8. Dashboard y Métricas

```mermaid
pie title Distribución de Candidatos por Estado
    "En Revisión" : 30
    "Preseleccionados" : 25
    "En Entrevista" : 20
    "Seleccionados" : 15
    "Rechazados" : 10
```

## 9. Integración con Sistemas Externos

```mermaid
graph TB
    subgraph ATS LTI
        A[Core ATS]
        B[API Gateway]
    end
    
    subgraph Integraciones
        C[LinkedIn]
        D[Indeed]
        E[Email]
        F[Calendar]
    end
    
    A <--> B
    B <--> C
    B <--> D
    B <--> E
    B <--> F
```

## 10. Ciclo de Vida del Candidato

```mermaid
graph LR
    A[Registro] --> B[Aplicación]
    B --> C[Evaluación]
    C --> D[Entrevista]
    D --> E[Oferta]
    E --> F[Contratación]
    
    style A fill:#f9f,stroke:#333,stroke-width:2px
    style F fill:#9f9,stroke:#333,stroke-width:2px
```

---

Estos diagramas proporcionan una visión completa de la arquitectura, flujos y procesos del sistema ATS de LTI. Los diagramas están creados usando la sintaxis Mermaid, que se renderiza automáticamente en plataformas como GitHub y GitLab.

Para visualizar estos diagramas correctamente, asegúrate de usar un visor de Markdown que soporte Mermaid, como GitHub, GitLab, o VSCode con la extensión adecuada. 