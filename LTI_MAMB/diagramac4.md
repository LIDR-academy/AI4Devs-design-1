graph TB

%% Nivel 1: Diagrama de Contexto
subgraph SistemaATS
    ATS["Sistema ATS\n[Software System]\nGestión de reclutamiento basado en IA"]
end

Recruiter["Reclutador\n[Persona]\nUsa el sistema para gestionar procesos"]
Candidate["Candidato\n[Persona]\nAplica y sigue procesos de selección"]
HRManager["Gerente de RRHH\n[Persona]\nAdministra y configura el sistema"]

JobBoards["Portales de Empleo\n[Software System]\nPlataformas de oferta laboral"]
SocialMedia["Redes Sociales\n[Software System]\nDifusión de ofertas"]

Recruiter -->|"Gestiona procesos de selección"| ATS
Candidate -->|"Aplica a vacantes"| ATS
HRManager -->|"Supervisa y configura el sistema"| ATS
ATS -->|"Publica ofertas"| JobBoards
ATS -->|"Distribuye contenido en redes"| SocialMedia

%% Nivel 2: Diagrama de Contenedores
subgraph SistemaATS ["Sistema ATS [Software System]"]
    WebApp["Aplicación Web\n[Contenedor: React/TypeScript]\nInterfaz principal"]
    MobileApp["Aplicación Móvil\n[Contenedor: React Native]\nInterfaz móvil"]
    
    APIGateway["API Gateway\n[Contenedor: Node.js]\nManejo de solicitudes y autenticación"]
    
    CoreServices["Servicios Core\n[Contenedor: Node.js/Express]\nLógica de negocio principal"]
    
    AIEngine["Motor de IA\n[Contenedor: Python]\nAnálisis avanzado y procesamiento"]
    
    Database["Base de Datos\n[Contenedor: PostgreSQL]\nAlmacenamiento de datos"]
    
    ChatbotService["Servicio de Chatbot\n[Contenedor: Python]\nAtención automatizada"]
end

WebApp -->|"Solicitudes API"| APIGateway
MobileApp -->|"Solicitudes API"| APIGateway
APIGateway -->|"Enrutamiento"| CoreServices
CoreServices -->|"Consultas y actualizaciones"| Database
CoreServices -->|"Solicita análisis de IA"| AIEngine
CoreServices -->|"Envía mensajes"| ChatbotService

%% Nivel 3: Diagrama de Componentes (MVP)
subgraph CoreServices ["Servicios Core [Contenedor]"]
    JobManager["Gestor de Ofertas\n[Componente]\nManejo de publicaciones de empleo"]
    CandidateManager["Gestor de Candidatos\n[Componente]\nAdministración de aplicantes"]
    RecruitmentFlow["Flujo de Reclutamiento\n[Componente]\nControl del proceso de selección"]
    Analytics["Análisis y Reportes\n[Componente]\nGeneración de métricas y KPIs"]
    
    AIIntegration["Integración con IA\n[Componente]\nConexión a servicios de IA"]
    CommunicationManager["Gestor de Comunicaciones\n[Componente]\nNotificaciones y mensajería"]
end

JobManager -->|"Acceso a datos de ofertas"| Database
CandidateManager -->|"Acceso a perfiles y estados"| Database
RecruitmentFlow -->|"Control de estados del proceso"| Database
Analytics -->|"Consultas de datos"| Database

AIIntegration -->|"Solicitudes de procesamiento"| AIEngine
CommunicationManager -->|"Envía mensajes automatizados"| ChatbotService
