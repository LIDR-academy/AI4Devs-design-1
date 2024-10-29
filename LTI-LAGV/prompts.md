# Chatbot: ChatGPT-4.0

## Prompt 1
En este ejercicio tu misión será diseñar y documentar un sistema de software siguiendo las fases de investigación, análisis, casos de uso, modelado de datos y diseño de alto nivel.

 ¿Y qué sistema? El de LTI. LTI es una startup que quiere desarrollar el ATS (Applicant-Tracking System) del futuro. 
 
 Para eso, primero haz análisis de los diferentes ATS que hay en el mercado, y busca las áreas de oportunidad para posteriormente agregarlas en nuestro producto como valor añadido y ventajas competitivas. Puedes ser creaativo y atrevido en la propuesta para darle un diferenciador a nuestro producto. 
 
 No me des nínguna respuesta por el momento.

## Prompt 2

Todavía no hay nada creado, así que adopta el rol de Product Manager con connocimientos sólidos en arquitectura de software y diseño de diagramas UML, define esas funcionalidades clave que harán brillar a LTI por encima de los competidores: aumentar la eficiencia para los departamentos de RH, mejorar la colaboración en tiempo real entre reclutadores y managers, automatizaciones, asistencia de IA en diversas tareas.

Tu misión es diseñar la primera versión del sistema, entregando los siguientes artefactos:

1) Descripción breve del software LTI, valor añadido y ventajas competitivas, toma como base el análisis previo que hiciste de los diferentes competidores. 

2)  Explicación de las funciones principales y en la parte de abajo añade un diagrama Lean Canvas para entender el modelo de negocio.

3) Descripción de los 3 casos de uso principales, con el diagrama asociado a cada caso de uso.

4) Modelo de datos que cubra entidades, atributos (nombre y tipo) y relaciones.

5) Diseño del sistema a alto nivel, pon la explicación y abajo el diagrama correspondiente.

6) Diagramas C4 que llegue en profundidad de los componentes principales del sistema, igual agrega la descripción de este diagrama en la parte inferior.


Puntos a considerar:

- Todos los diagramas deben ser elaborados con Mermaid o en su defecto con alguna herramienta similar de tal manera que puedan ser incluidos dentro de un archivo .MD

- Debes asegurarte que no falte ninguno de los 6 aterfactos definidos.


Hazme las preguntas que necesites antes de iniciar.

## Respuesta ChatGPT

Gracias por los detalles. Antes de comenzar, me gustaría aclarar algunos puntos para alinear bien los requisitos:

1. **Nivel de automatización**: ¿Te interesa incluir funciones de automatización como respuestas automáticas a candidatos, creación de recordatorios automáticos para reclutadores, o procesos de evaluación automatizados? 

2. **Asistencia de IA**: ¿Tienes preferencia en las áreas de IA, como clasificación automática de CVs, recomendaciones de candidatos para ciertas vacantes, o análisis de tono en respuestas de entrevistas?

3. **Colaboración en tiempo real**: Para mejorar la colaboración entre reclutadores y managers, ¿qué tan interactivo deseas que sea el sistema? Ejemplo: comentarios en tiempo real, chat en vivo, o paneles compartidos.

4. **Alcance del modelo de negocio en Lean Canvas**: ¿Te gustaría que cubramos solo esta primera versión (centrándonos en adopción temprana de usuarios) o proyectamos también fases futuras para monetización o expansión?

Avísame si tienes preferencia por algún enfoque específico en estos puntos.


## Prompt 4
1) Sí
2) Incluye todo esos puntos.
3) Puedes incluir los 3 puntos pero enfócate en el chat en vivo.
4) Dame las dos propuestas, es decir un primera versión y también otra proyectando fases futuras.

## Prompt 5
"Que sea la puras etiquetas a partir de table, sin ocupar ningún estilo, básate en esta estructura https://gist.githubusercontent.com/pierrebeaucamp/fa2fec4f859d8d9ce3d0/raw/2e8cb6df840b6d194506d1e6587dea78a55a0c61/LeanCanvas.md"

## Prompt 6
Listo, ahora une toda la documentación y expórtalo en un archivo .MD, pero antes agrega un índice con todos los apartados.

## Prompt 7
Me sale este error: Syntax error: No diagram type detected matching given configuration for text: usecaseDiagram en los diagramas de casos de uso.

## Respuesta ChatGPT 
Para resolver el error en los diagramas de casos de uso, cambia usecaseDiagram por @startuml y @enduml.

## Prompt 8
Los diagramas que empiezan con este tag @startuml no se pueden ver en el archivo .MD, ¿qué alternativas hay?

## Respuesta ChatGPT 
Para visualizar los diagramas en un archivo .MD, puedes reemplazar @startuml con el formato de etiquetas Mermaid que Markdown soporta nativamente en muchas plataformas. Aquí tienes la versión revisada con las etiquetas Mermaid ````mermaidy ``` `:

## Prompt 9
Une todo en un único archivo .MD, no pongas el código, expórtalo.
