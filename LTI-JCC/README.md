# LTI - Sistema ATS

Sistema de Seguimiento de Candidatos (ATS) desarrollado por LTI, diseñado para optimizar y automatizar el proceso de reclutamiento y selección de personal.

## Documentación

### Arquitectura
- [Diagrama de Contexto](./docs/arquitectura/contexto.md)
- [Diagrama de Contenedores](./docs/arquitectura/contenedores.md)
- [Diagrama de Componentes](./docs/arquitectura/componentes.md)
- [Diagrama de Código](./docs/arquitectura/codigo.md)

### Negocio
- [Beneficios del Sistema](./docs/Negocio/beneficios.md)
- [Ventajas Competitivas](./docs/Negocio/ventajas_competitivas.md)
- [Lean Canvas](./docs/Negocio/lean_canvas.md)
- [Casos de Uso](./docs/Negocio/casos_uso.md)
- [Diagramas Técnicos](./docs/Negocio/diagramas.md)

## Tecnologías Principales

- **Frontend**:
  - React 18.x (Web Interface)
  - React Native 0.72+ (Mobile App)
  - TypeScript 5.x
  - Material-UI 5.x
  - Redux Toolkit

- **Backend**:
  - Node.js 20.x LTS
  - Express.js 4.x
  - TypeScript 5.x
  - Jest para testing
  - Swagger/OpenAPI para documentación

- **Base de Datos**:
  - PostgreSQL 15+
  - Redis para caché
  - Prisma como ORM

- **DevOps & Infraestructura**:
  - Docker & Kubernetes
  - GitHub Actions para CI/CD
  - ELK Stack (Elasticsearch, Logstash, Kibana)
  - Prometheus & Grafana para monitoreo

- **Seguridad**:
  - JWT para autenticación
  - OAuth2 para autorización
  - Helmet.js para seguridad HTTP
  - Rate limiting y protección DDOS

- **Integración**:
  - RabbitMQ para mensajería
  - RESTful APIs
  - WebSockets para comunicación en tiempo real

## Principios de Arquitectura

1. **Diseño Basado en Dominio (DDD)**
   - Separación clara de dominios de negocio
   - Bounded contexts definidos
   - Ubicuidad del lenguaje

2. **Arquitectura Limpia**
   - Separación de responsabilidades
   - Independencia de frameworks
   - Inversión de dependencias

3. **Microservicios**
   - Servicios autónomos
   - Escalabilidad independiente
   - Resiliencia

4. **DevSecOps**
   - Seguridad integrada
   - Automatización
   - Monitoreo continuo

## Calidad y Pruebas

- Tests unitarios
- Tests de integración
- Tests E2E
- Análisis de código estático
- Pruebas de seguridad
- Pruebas de rendimiento

## Despliegue

- Contenedores Docker
- Orquestación con Kubernetes
- Infraestructura como código
- Despliegue continuo

## Contacto

LTI - Transformando el reclutamiento con tecnología
- Email: contacto@lti.com
- Web: www.lti.com
- LinkedIn: /company/lti

## Licencia

Propietario - LTI © 2025