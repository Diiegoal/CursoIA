# Orden óptimo de los 10 módulos de `CursoIA` para construir `Proyecto_Final_Master_AI4Devs`

**Repositorio analizado:** `https://github.com/Diiegoal/CursoIA.git`  
**Rama analizada:** `main`  
**Fecha de contraste:** 2 de septiembre de 2026  
**Proyecto final objetivo:** `Proyecto_Final_Master_AI4Devs`  
**Referencia elegida por el alumno:** **Ejemplo 2** del archivo `Proyecto_Final_Master_AI4Devs/Ejemplo_Proyectos_Finales_Reales.md`.

---

## 1. Respuesta ejecutiva

El orden que considero más sólido para utilizar los **10 módulos como un proceso de construcción real** no es el orden numérico actual del repositorio.

La secuencia recomendada es:

```text
PRE-FASE — Definición inicial del proyecto + estudio del Ejemplo 2
        ↓
1. Módulo 1 — Los 3 pilares del uso efectivo de copilotos IA
        ↓
2. Módulo 3 — Sistema operativo de Copilotos IA
        ↓
3. Módulo 4 — Planificación efectiva con IA
        ↓
4. Módulo 5 — Documentación efectiva con IA
        ↓
5. Módulo 6 — Ética, Regulación y Privacidad en el uso de IA
        ↓
6. Módulo 2 — Spec-Driven Development (SDD)
        ↓
7. Módulo 7 — Testing y calidad con IA
        ↓
8. Módulo 8 — Bases de datos
        ↓
9. Módulo 9 — Programación asistida por IA — Backend
        ↓
10. Módulo 10 — Programación asistida por IA — Frontend
        ↓
CICLO CONTINUO — PR → revisión → pruebas → documentación → merge → siguiente historia
```

### Respuesta concreta a la duda principal

Después de realizar la **definición inicial del proyecto**, no recomiendo saltar directamente a SDD.

La dependencia profesional más coherente es:

```text
Definición del producto
        ↓
Planificación del producto / backlog
        ↓
Arquitectura y documentación inicial
        ↓
Seguridad, privacidad, regulación y riesgos
        ↓
SDD / OpenSpec por historia o cambio concreto
        ↓
Tests derivados de criterios de aceptación / spec
        ↓
Diseño e implementación de datos
        ↓
Backend
        ↓
Frontend
```

La razón fundamental es que **SDD no sustituye la planificación del producto**. El propio Módulo 4 distingue claramente entre la capa de producto y la capa de especificación: el backlog responde qué se entrega y por qué; OpenSpec formaliza cómo se construye un cambio concreto. El flujo que propone el repositorio es `PRD → User Story → OpenSpec change → Código`. [Fuente del repositorio: Módulo 4, “Anatomía de un backlog AI-ready”.]

Además, el propio material de SDD define la especificación como un contrato que debe capturar qué se construye y por qué, mientras que `design.md` captura decisiones sobre cómo construirlo. Por ello una OpenSpec útil necesita que ya exista suficiente contexto funcional, técnico, arquitectónico y de seguridad. [Fuente del repositorio: Módulo 2, “Qué es Spec-Driven Development” y “Anatomía de OpenSpec”.]

**Conclusión importante:** `planificación → documentación → seguridad → SDD` es una mejor secuencia inicial que `planificación → SDD → documentación`, aunque la documentación no termina nunca y parte de ella debe seguir produciéndose durante SDD, desarrollo, revisión y despliegue.

---

# 2. Distinción fundamental: lo que dice el repositorio vs. mi recomendación profesional

Para evitar mezclar hechos con inferencias, este documento utiliza tres categorías.

### A. Evidencia directa del repositorio

Son afirmaciones extraídas de los documentos del repositorio `Diiegoal/CursoIA`, de la estructura real de sus carpetas/archivos y de la lección del proyecto final.

### B. Evidencia externa verificable

Son principios que contrasté con fuentes primarias o de alta autoridad, especialmente:

- documentación oficial de GitHub;
- documentación oficial de OpenSpec;
- documentación oficial de GitHub Spec Kit;
- sitio oficial del modelo C4;
- NIST SSDF / NIST AI RMF;
- documentación OWASP sobre threat modeling;
- principios originales del Manifiesto Ágil;
- referencia de Martin Fowler sobre TDD.

### C. Inferencia/recomendación profesional

Es la secuencia que propongo al combinar las dependencias encontradas en los módulos con prácticas de ingeniería de software. Esta secuencia **no se presenta como “la única manera correcta”** ni como una secuencia oficial impuesta por el curso. Es el orden que considero más coherente para tu objetivo específico: construir una aplicación web full stack real, profesional, con IA y tomando el Ejemplo 2 como referencia.

---

# 3. Qué contiene realmente el repositorio

El árbol de la rama `main` confirma que existen los siguientes 10 módulos, además de documentación específica del proyecto final y material de prompts.

## Módulo 1 — `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA`

Archivos:

1. `1. El modelo mental de los 3 pilares.md`
2. `2. Pilar 1 — La Herramienta.md`
3. `3. Pilar 2 — El Contexto.md`
4. `4. Pilar 3 — El Prompt + Integración.md`
5. `5. Recursos adicionales.md`

## Módulo 2 — `Módulo_2_Spec_Driven_Development_(SDD)`

Archivos:

1. `1. Qué es Spec-Driven Development.md`
2. `2. El ecosistema SDD en 2026.md`
3. `3. Anatomía de OpenSpec.md`
4. `4. Cheat-sheet OpenSpec.md`
5. `5. Practica con codigo.md`
6. `6. Recursos adicionales.md`

## Módulo 3 — `Módulo_3_Sistema_operativo_Copilotos_IA`

Archivos:

1. `1. El copiloto en serio. instalación, planes y primera sesión real.md`
2. `2. Anatomía de un copiloto moderno.md`
3. `3. Cómo se trabaja. Explore-Plan-Execute y copilotos SDD-aware.md`
4. `4. Decisiones de senior. cuándo qué, costes reales, gobernanza.md`
5. `5. Practica con codigo.md`
6. `6. Recursos adicionales.md`

## Módulo 4 — `Módulo_4_Planificación_efectiva_con_IA`

Archivos:

1. `1. La planificación cambia. nuevos paradigmas.md`
2. `2. Anatomía de un backlog AI-ready.md`
3. `3. Estimación asistida por IA.md`
4. `4. PM tools + IA en 2026.md`
5. `5. Planificación ágil continua.md`
6. `6. Recursos adicionales.md`

## Módulo 5 — `Módulo_5_Documentación_efectiva_con_IA`

Archivos:

1. `1. El déficit documental en la era IA.md`
2. `2. Arquitectura documentada. ADRs + diagramas C4 con IA.md`
3. `3. Documentación de API y código.md`
4. `4. Testing de documentación en CI y docs para LLMs.md`
5. `5. Practica con codigo.md`
6. `6. Recursos adicionales.md`

## Módulo 6 — `Módulo_6_Ética_Regulación_y_Privacidad_en_el_uso_de_IA`

Archivos:

1. `1. GDPR, marcos regulatorios de AI y agencias de AI.md`
2. `2. Principales riesgos de seguridad y privacidad.md`
3. `3. Mejores prácticas de seguridad en la interacción con LLMs.md`
4. `4. El auge de los modelos LLM locales.md`
5. `5. Recursos adicionales.md`

## Módulo 7 — `Módulo_7_Testing_y_calidad_con_IA`

Archivos:

1. `1. ntroducción a TDD.md`
2. `2. Fake It ('Til You Make It).md`
3. `3. Buenas prácticas de testing.md`
4. `4. Uso de IA para escribir tests.md`
5. `5. Creación de tu propio asistente de testing con Danilo Alarcón.md`
6. `6. Practica con codigo.md`
7. `7. Recursos adicionales.md`

## Módulo 8 — `Módulo_8_Bases_de_datos`

Archivos:

1. `1. Buenas prácticas en bases de datos.md`
2. `2. Un ejemplo práctico de uso de IA en BBDD.md`
3. `3. Preguntando con IA a mi BBDD.md`
4. `4. Recursos adicionales.md`
5. `5. Practica con codigo.md`

## Módulo 9 — `Módulo_9_Programación_asistida_por_IA_backend`

Archivos:

1. `1. Patrones de Refactorización - Refactorización en la era agéntica.md`
2. `2. Buenas prácticas para el Desarrollo Backend.md`
3. `3. Demo de ticket a pull request.md`
4. `4. Recursos adicionales.md`

## Módulo 10 — `Módulo_10_Programación_asistida_por_IA_frontend`

Archivos:

1. `1. Buenas prácticas para el Desarrollo Frontend .md`
2. `2. De diseño a código con IA.md`
3. `3. Recursos adicionales.md`

### Material adicional relevante fuera de los 10 módulos

El repositorio también contiene:

- `Proyecto_Final_Master_AI4Devs/Leccion_1_Proyecto_Final_AI4Devs.md`
- `Proyecto_Final_Master_AI4Devs/Ejemplo_Proyectos_Finales_Reales.md`
- `Prompts/Plan_M1_Proyecto_Full_Stack_AI4Devs.md`
- `Prompts/Prompts_1_al_6/Paso_1_Preparacion_local_y_clone_verificable.md`

El árbol recursivo de GitHub de `main` reporta que no está truncado y muestra estos elementos del repositorio.

---

# 4. La referencia del proyecto final: por qué el Ejemplo 2 cambia el orden

El archivo `Proyecto_Final_Master_AI4Devs/Ejemplo_Proyectos_Finales_Reales.md` indica expresamente que los dos ejemplos deben usarse como **referencia de estructura y calidad, no como molde para copiar**.

También especifica que conviene estudiar:

- estructura del repositorio;
- `README.md`;
- `prompts.md` o registro del uso de IA;
- `/docs` o `/architecture`;
- `.github/workflows` si existe;
- estructura del backend;
- componentes y estado del frontend;
- tests unitarios y E2E;
- ejecución local;
- URL pública o video;
- decisiones arquitectónicas.

El **Ejemplo 2** se describe en el repositorio como un chatbot RAG avanzado que actúa como representante virtual para un portfolio profesional, con captura natural de leads. El documento describe como referencia tecnológica:

```text
Python 3.11+
FastAPI
React 18
TypeScript
Gemini 2.5 Flash
HuggingFace embeddings
pgvector
GCP
Cloud Run
Cloud SQL
Pytest
Coverage
```

El repositorio señala como elementos destacables del Ejemplo 2:

- arquitectura RAG;
- embeddings locales multilingües;
- pgvector;
- optimización de costes;
- cache;
- monitorización de costes;
- GDPR/consentimientos;
- lead capture;
- lead scoring;
- Cloud Run;
- Cloud SQL con pgvector;
- Artifact Registry;
- CI/CD;
- Secret Manager;
- testing con Pytest y cobertura superior al 80% según la descripción del ejemplo.

**Importante:** estos valores y características son afirmaciones del material del curso sobre ese proyecto de referencia. No deben transformarse automáticamente en requisitos para tu propio proyecto. El mismo archivo advierte que cada proyecto es diferente.

Fuente primaria del repositorio: `Proyecto_Final_Master_AI4Devs/Ejemplo_Proyectos_Finales_Reales.md`.

---

# 5. La definición inicial del proyecto es una pre-fase, no uno de los 10 módulos

Antes de aplicar los 10 módulos, hay una actividad previa que viene directamente de la lección del proyecto final:

## Definir el MVP

La lección del proyecto final establece que el entregable es un **MVP de tema libre** y que debe ser robusto, no simplemente una pantalla con un botón.

La lección señala como mínimo un flujo end-to-end completo con backend, frontend y base de datos, o un equivalente según el perfil y stack.

También recomienda:

- 3–5 historias de usuario `must-have`;
- 1–2 historias `should-have`;
- no intentar implementar todo lo aprendido en el máster.

La Entrega 1 del proyecto final incluye documentación técnica de:

- ficha del proyecto;
- descripción general;
- arquitectura;
- modelo de datos;
- historias de usuario;
- tickets;
- stack tecnológico.

La Entrega 2 pasa a scaffolds del frontend, backend y base de datos, además del flujo principal y primeras funcionalidades.

La Entrega final une documentación y código, exige funcionalidades completas, tests, evidencia del despliegue y registro del uso de IA.

**Implicación profesional:** esta pre-fase determina el “qué” del producto antes de que el trabajo técnico de cada feature se convierta en un cambio SDD.

Fuente: `Proyecto_Final_Master_AI4Devs/Leccion_1_Proyecto_Final_AI4Devs.md`.

---

# 6. ORDEN 1 — Módulo 1: Los 3 pilares del uso efectivo de copilotos IA

## Posición

**1 de 10.**

## Propósito dentro del proyecto

Establecer el modelo mental con el que se utilizará IA durante todo el ciclo de desarrollo.

El módulo define tres pilares:

```text
Herramienta
Contexto
Prompt
```

Y explica que en desarrollo asistido por agentes el resultado depende de cómo se configura el sistema alrededor del modelo, de la calidad del contexto y de la instrucción.

La lección del módulo recalca que el prompt no debe verse como una magia aislada y que el contexto y el harness son parte de la ingeniería.

## Qué aporta al proceso

Este módulo no produce todavía una arquitectura ni código.

Produce algo más fundamental: **el marco operativo para utilizar los módulos posteriores con IA sin tratar al agente como una caja negra**.

En particular prepara para:

- seleccionar una herramienta apropiada;
- preparar contexto persistente;
- definir criterios de éxito;
- reducir prompts ambiguos;
- distinguir exploración, planificación y ejecución;
- evitar megaprompts;
- trabajar con archivos de instrucciones y conocimiento del proyecto.

## Dependencias respecto de otros módulos

Tiene prácticamente ninguna dependencia de los demás porque es el fundamento metodológico.

A su vez, todos los demás módulos se benefician de él:

```text
M1
 ├──► M3: cómo operar el copiloto
 ├──► M4: cómo usar IA para planificar
 ├──► M5: cómo usar IA para documentar
 ├──► M2: cómo trabajar con specs
 ├──► M7: cómo aplicar IA al testing
 ├──► M8: cómo usar IA con bases de datos
 ├──► M9: cómo programar backend con IA
 └──► M10: cómo programar frontend con IA
```

## Por qué debe ir aquí

Porque sería prematuro estudiar una técnica de desarrollo asistido por agentes sin establecer primero cómo se configura el contexto y cómo se define el resultado esperado.

La razón no es “porque sea el módulo 1”, sino porque constituye la capa transversal sobre la que funcionan los otros nueve.

## Evidencia del repositorio

El Módulo 3 declara explícitamente que S1 estableció los tres pilares y que los módulos posteriores no deben re-explicar ese fundamento. El Módulo 2 también conecta SDD con herramienta, contexto y prompt.

---

# 7. ORDEN 2 — Módulo 3: Sistema operativo de Copilotos IA

## Posición

**2 de 10.**

## Propósito dentro del proyecto

Convertir el modelo mental del M1 en un **entorno operativo real** para trabajar con el agente.

El propio Módulo 3 dice que S1 estableció el modelo mental y que S2 estableció el método SDD; M3 baja al “harness real”: configuración, operación, Explore-Plan-Execute, skills, hooks, subagentes y gobierno del agente.

## Qué aporta

Entre sus elementos más importantes aparecen:

- instalación de Claude Code y Cursor;
- `CLAUDE.md`;
- herramientas y MCP;
- subagentes;
- plan mode;
- exploración del repositorio;
- ejecución agéntica;
- hooks;
- manejo de contexto;
- `Explore → Plan → Execute`;
- integración con OpenSpec;
- estrategias para evitar context rot;
- criterios para escoger entre ejecución directa y plan mode.

La lección de EPE describe tres fases:

```text
EXPLORE → PLAN → EXECUTE
```

y coloca el gate humano entre Plan y Execute.

Esto es especialmente importante para tu proyecto porque la construcción será multiarchivo, incluirá frontend/backend/base de datos y tendrá operaciones con efectos secundarios.

## Dependencias

Depende del M1.

Es previo a M4 porque necesitas saber operar el agente antes de delegarle investigación, refinamiento de backlog y planificación.

También es previo a M2 en sentido operativo, aunque conceptualmente M2 explica SDD antes. Para **construir el proyecto**, necesitas llegar al punto de poder ejecutar correctamente el método después de aprenderlo.

## Por qué va antes de planificación

No porque el copiloto deba decidir el producto, sino porque la planificación asistida con IA debe hacerse con un flujo controlado.

La combinación correcta es:

```text
M1 → cómo pensar sobre IA
M3 → cómo operar IA
M4 → cómo aplicar IA al trabajo de producto
```

## Evidencia especialmente fuerte del repositorio

El Módulo 3 describe el patrón Explore-Plan-Execute y advierte contra planificar en frío sin explorar el código cuando se trata de un repositorio existente.

Para un proyecto nuevo, esto se traduce en:

- explorar requisitos, opciones y restricciones;
- generar un plan;
- revisar el plan;
- ejecutar después de la aprobación humana.

---

# 8. ORDEN 3 — Módulo 4: Planificación efectiva con IA

## Posición

**3 de 10.**

## Este es el módulo que debe venir inmediatamente después de preparar al copiloto

Para responder directamente a tu pregunta: **después de la definición inicial del proyecto, el siguiente gran bloque debe ser la planificación del producto.**

## Por qué

El Módulo 4 establece una jerarquía explícita:

```text
PRD
 ↓
EPICS
 ↓
USER STORIES
 ↓
TASKS
 ↓
ACCEPTANCE CRITERIA
```

Y distingue el nivel de producto del nivel técnico.

La idea crucial para este proyecto es:

> El backlog determina qué se debe entregar y por qué.

Mientras que OpenSpec determinará después cómo se materializa un cambio técnico concreto.

## Qué debe producir el proyecto en esta fase

Antes de abrir el primer change SDD, deberías tener como mínimo:

```text
1. Objetivo del producto
2. Usuario objetivo
3. Problema que resuelve
4. Alcance MVP
5. Non-goals
6. User stories must-have
7. User stories should-have
8. Acceptance criteria
9. Prioridades
10. Dependencias
11. Riesgos preliminares
12. Hipótesis técnicas relevantes
13. Criterio de éxito del MVP
```

No significa escribir una documentación burocrática gigantesca.

Significa tener una base suficientemente precisa para que el desarrollo técnico no empiece inventando el producto.

## Dependencias

Depende de:

- definición inicial del proyecto;
- M1 para el uso efectivo de IA;
- M3 para operar el copiloto en modo Explore/Plan.

Alimenta directamente a:

- M5: documentación/arquitectura;
- M6: riesgos de seguridad y privacidad;
- M2: OpenSpec;
- M7: tests y criterios de aceptación.

## Evidencia interna decisiva

El Módulo 4 afirma explícitamente que el backlog/product layer y OpenSpec/spec layer son dos capas diferentes.

La tabla del módulo resume:

| Capa | Pregunta |
|---|---|
| Backlog | ¿Qué se entrega y por qué? |
| OpenSpec | ¿Cómo se construye exactamente? |

Y muestra el flujo:

```text
PRD → User Story → OpenSpec change → Código
```

Esto es la principal evidencia para **no poner SDD antes de la planificación del producto**.

## Relación con el Ejemplo 2

El Ejemplo 2 no debe copiarse como producto. Debe utilizarse para observar qué capacidades hacen que un proyecto RAG full stack sea suficientemente robusto.

Por tanto, esta fase convierte esas observaciones en requisitos propios, no en una copia de funcionalidades.

---

# 9. ORDEN 4 — Módulo 5: Documentación efectiva con IA

## Posición

**4 de 10.**

## Por qué no lo pondría después de programar

Porque una parte importante del Módulo 5 es **documentación arquitectónica**, no solamente documentación del código terminado.

El documento “Arquitectura documentada: ADRs + diagramas C4 con IA” trata los ADRs como memoria institucional y recomienda mantener diagramas como texto en el repositorio.

También se propone generar diagramas desde la estructura real del sistema y registrar decisiones importantes mediante ADRs.

## Qué debe producirse aquí

Antes de pasar a SDD conviene tener una primera versión de:

```text
docs/
├── architecture/
├── adr/
└── diagrams/
```

Y, según el alcance:

- contexto del sistema;
- containers principales;
- componentes importantes;
- flujos principales;
- decisiones arquitectónicas;
- stack elegido;
- integración con proveedores de IA;
- límites del sistema;
- fuentes externas;
- modelo de datos preliminar.

## Importante: este módulo no se “termina” aquí

Esta es una de las principales conclusiones de toda la investigación.

El M5 contiene tres clases de documentación:

### Documentación que debe existir antes de implementar

- arquitectura inicial;
- decisiones relevantes;
- modelo conceptual;
- contexto del sistema.

### Documentación que nace durante la implementación

- ADRs nuevos;
- diagramas actualizados;
- OpenAPI;
- decisiones de integración;
- documentación de código.

### Documentación que se verifica después

- docs en CI;
- snippets ejecutables;
- links internos;
- referencia API.

Por tanto, tratar “M5” como una fase cerrada sería una simplificación incorrecta.

## Relación con SDD

OpenSpec tiene `design.md`, donde se registran decisiones técnicas, riesgos, trade-offs y plan de migración.

Por eso la relación correcta no es:

```text
M5 o M2
```

sino:

```text
M5 aporta el lenguaje y la memoria arquitectónica
              ↓
M2 formaliza cambios concretos en specs
              ↓
M5 continúa actualizando documentación viva
```

## Evidencia externa

El C4 Model oficial define una jerarquía de abstracciones para visualizar arquitectura: software system, container, component y code, además de diagramas de contexto, dinámica y despliegue. Esto coincide con la función arquitectónica que el M5 asigna a C4. [C4 Model oficial](https://c4model.com/)

---

# 10. ORDEN 5 — Módulo 6: Ética, Regulación y Privacidad en el uso de IA

## Posición

**5 de 10.**

## Por qué va antes de SDD y código

Porque seguridad y privacidad no deberían aparecer como un parche posterior.

En un sistema que usa IA y, particularmente, si toma inspiración del Ejemplo 2, debes decidir temprano:

- qué datos procesa el sistema;
- qué datos se envían a proveedores de modelos;
- qué datos pueden almacenarse;
- qué información es sensible;
- qué consentimiento hace falta;
- qué riesgos introduce la integración con LLMs;
- cómo se manejan secretos;
- qué límites tendrá el agente durante el desarrollo;
- qué controles serán necesarios en producción.

## Evidencia interna

El Módulo 6 cubre:

- marcos regulatorios;
- GDPR;
- riesgos de seguridad y privacidad;
- mejores prácticas de seguridad con LLMs;
- modelos locales;
- exposición de código;
- credenciales;
- riesgos de supply chain;
- prompt injection;
- gobernanza.

No todos los ejemplos regulatorios del módulo deben aceptarse automáticamente como hechos actuales: las afirmaciones concretas sobre proveedores, precios, políticas y litigios cambian y deben verificarse externamente cuando sean relevantes.

## Evidencia externa primaria

NIST indica que las prácticas de seguridad deben integrarse en cada implementación del SDLC y que, en general, cuanto antes se aborda la seguridad en el SDLC, menor esfuerzo y coste se necesitan después. Esto respalda poner el M6 antes de cerrar el diseño técnico y no después del backend/frontend. [NIST SP 800-218](https://csrc.nist.gov/pubs/sp/800/218/final)

La documentación de NIST sobre DevSecOps describe explícitamente la fase Plan como el punto donde se definen requisitos funcionales, no funcionales y de seguridad, se evalúan riesgos y se crea una estrategia proactiva de seguridad. [NIST DevSecOps](https://pages.nist.gov/nccoe-devsecops/notational-reference-model.html)

OWASP recomienda realizar threat modeling idealmente temprano, durante diseño, y mantenerlo/refinarlo a lo largo del SDLC. [OWASP Threat Modeling Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html)

## Consecuencia para tu orden

El M6 no significa “hacer seguridad una vez y olvidarla”. Significa:

```text
M6 temprano
   ↓
restricciones y requisitos de seguridad
   ↓
M2 / OpenSpec
   ↓
implementación
   ↓
testing / revisión / CI
   ↓
seguridad continua
```

---

# 11. ORDEN 6 — Módulo 2: Spec-Driven Development (SDD)

## Posición

**6 de 10.**

## Este es el punto que genera más confusión

El Módulo 2 es fundamental, pero **no debe interpretarse como sustituto de la planificación inicial del producto**.

Su lugar óptimo en el flujo de construcción es después de haber establecido:

```text
qué producto queremos
qué funcionalidades entran en el MVP
qué riesgos existen
qué arquitectura preliminar usamos
qué reglas y restricciones aplican
```

Entonces SDD convierte una unidad de trabajo concreta en un contrato ejecutable/versionado.

## Evidencia interna decisiva

El Módulo 2 define SDD como una metodología donde la especificación es el artefacto primario y el código es una expresión de esa especificación.

También distingue:

- `proposal.md`: por qué y qué cambia;
- `specs/`: comportamiento esperado;
- `design.md`: cómo se construye;
- `tasks.md`: checklist accionable.

El workflow de OpenSpec del propio material es:

```text
propose → revisión humana → apply → tests/validación → archive
```

La documentación oficial actual de OpenSpec mantiene el mismo núcleo operativo: inicializar, explorar opcionalmente, proponer un change, aplicar el change y archivar el trabajo terminado. [OpenSpec README](https://github.com/Fission-AI/OpenSpec/blob/main/README.md)

La documentación oficial de OpenSpec también indica actualmente Node.js 20.19.0 o superior como prerrequisito. [OpenSpec installation](https://github.com/Fission-AI/OpenSpec/blob/main/docs/installation.md)

## Flujo recomendado dentro de tu proyecto

No debes crear una única OpenSpec gigantesca para toda la aplicación.

La estructura recomendada es:

```text
Proyecto
├── contexto general
├── PRD / visión
├── backlog
├── arquitectura
├── riesgos / restricciones
│
└── para cada historia/cambio significativo:
    └── OpenSpec change
        ├── proposal.md
        ├── specs/
        ├── design.md
        └── tasks.md
```

## Dependencias

M2 consume:

- M1: modelo mental de IA;
- M3: forma de operar el agente;
- M4: historias/AC/backlog;
- M5: arquitectura y documentación;
- M6: restricciones de seguridad, privacidad y regulación.

M2 alimenta:

- M7: tests;
- M8: cambios de datos;
- M9: backend;
- M10: frontend.

## Qué representa la relación SDD → testing

El Módulo 2 establece scenarios que pueden traducirse directamente en tests.

El Módulo 7 luego convierte ese contrato en una estrategia de verificación más rigurosa.

Así:

```text
User Story
   ↓
Acceptance Criteria
   ↓
OpenSpec scenarios
   ↓
Tests
   ↓
Implementation
```

Esto no significa que todo proyecto deba generar literalmente cada test desde un scenario de OpenSpec, pero sí que existe una cadena de trazabilidad útil.

## Evidencia externa

GitHub presenta Spec Kit como un toolkit de Spec-Driven Development que organiza prompts, templates, scripts y assets de integración para definir un workflow de desarrollo guiado por especificaciones. [GitHub Spec Kit](https://github.com/github/spec-kit)

La documentación de conceptos de Spec Kit define SDD como un proceso donde la especificación define el “qué” antes del “cómo” y donde las specs tienen un papel mucho más central en la generación de implementación. [GitHub Spec Kit — SDD](https://github.com/github/spec-kit/blob/main/docs/concepts/sdd.md)

---

# 12. ORDEN 7 — Módulo 7: Testing y calidad con IA

## Posición

**7 de 10.**

## Por qué el testing debe estar antes de la implementación principal

No recomiendo aprender o adoptar testing como “fase final”. El contenido del Módulo 7 está diseñado para encajar con el desarrollo incremental.

La primera lección describe:

```text
RED → GREEN → REFACTOR
```

Y, de forma todavía más importante para tu proyecto, explica el flujo desde historia de usuario y criterios de aceptación hasta pruebas.

La lección presenta esta cadena:

1. historia;
2. criterios de aceptación;
3. criterio seleccionado;
4. test;
5. código;
6. ejecución de tests;
7. refactor;
8. repetir.

## Relación con SDD

El Módulo 7 afirma explícitamente que SDD, BDD y TDD son complementarios:

- SDD define comportamiento a nivel de sistema/feature;
- BDD expresa escenarios de comportamiento;
- TDD guía la implementación mediante tests.

La separación funcional es:

```text
SDD = contrato amplio
BDD = escenarios observables
TDD = ciclo de implementación/verificación
```

## Evidencia externa

Martin Fowler describe TDD como el ciclo repetitivo de escribir el test, hacer pasar el test con la implementación y refactorizar, además de preparar una lista de casos de prueba y seleccionar el siguiente caso. [Martin Fowler — Test Driven Development](https://martinfowler.com/bliki/TestDrivenDevelopment.html)

## Por qué no va después de M9/M10

Porque entonces perderías una de las ventajas principales del enfoque:

```text
Especificación
    ↓
criterios verificables
    ↓
tests
    ↓
código
```

Además, la lección del proyecto final exige en la entrega final una suite con tests unitarios, integración y al menos un E2E del flujo principal.

## Qué debe ocurrir realmente

M7 se estudia aquí para definir la estrategia y, a partir de ese momento, se aplica continuamente:

```text
Cada OpenSpec change
      ↓
tests
      ↓
implementación
      ↓
refactor
      ↓
CI
      ↓
PR
```

---

# 13. ORDEN 8 — Módulo 8: Bases de datos

## Posición

**8 de 10.**

## Por qué ahora

El proyecto es full stack y, en el caso de un RAG parecido al Ejemplo 2, la persistencia no es un detalle posterior.

El Módulo 8 trata:

- bases SQL;
- NoSQL;
- alternativas cloud/serverless;
- normalización;
- índices;
- consultas;
- joins;
- bases vectoriales;
- pgvector;
- uso de IA para analizar schemas y consultas.

## Por qué no antes de arquitectura/documentación

No deberías elegir una base de datos solo porque el módulo la enseñe.

La elección debe salir de:

```text
requisitos
  ↓
casos de uso
  ↓
modelo de datos
  ↓
requisitos de consistencia / búsqueda / escala
  ↓
arquitectura
  ↓
selección de tecnología
```

Para un RAG, por ejemplo, el vector store depende de necesidades de búsqueda, volumen, latencia, filtros y relación con datos transaccionales.

El Módulo 8 presenta `pgvector` como una opción integrada en PostgreSQL para combinar datos relacionales y embeddings; esa es una recomendación del material del curso, no un requisito universal para tu proyecto.

## Relación con M2

Una vez que una historia concreta requiere cambios en persistencia, el change de OpenSpec debe especificar:

- entidades afectadas;
- constraints;
- migraciones;
- índices;
- cambios de consultas;
- impactos;
- tests.

Entonces M8 deja de ser teoría y pasa a convertirse en una implementación concreta guiada por la spec.

## Dependencia con M9

El backend consume la base de datos.

Por ello, para el orden didáctico de los 10 módulos:

```text
M8 → M9
```

es más natural que

```text
M9 → M8
```

aunque en un equipo profesional los modelos de datos, los contratos y el backend se refinan iterativamente y pueden trabajarse en paralelo.

---

# 14. ORDEN 9 — Módulo 9: Programación asistida por IA — Backend

## Posición

**9 de 10.**

## Por qué aquí

Aquí finalmente se entra de lleno en la implementación de backend.

El Módulo 9 cubre:

- refactorización asistida por IA;
- buenas prácticas backend;
- DDD;
- arquitectura hexagonal;
- SOLID/CUPID/DRY;
- patrones;
- flujo ticket → pull request.

El documento de buenas prácticas backend insiste en que una estructura clara ayuda tanto a humanos como a agentes. También trata bounded contexts, aggregates, value objects, repositories, domain events y puertos/adapters.

## Dependencias

M9 necesita el contexto acumulado:

```text
M4 → qué feature construir
M5 → arquitectura y decisiones
M6 → restricciones de seguridad
M2 → contrato de la feature
M7 → estrategia de verificación
M8 → persistencia
```

Luego implementa.

## El flujo por feature debería ser

```text
Backlog story
   ↓
OpenSpec change
   ↓
Explore
   ↓
Plan
   ↓
Tests
   ↓
Backend implementation
   ↓
Run tests
   ↓
Refactor
   ↓
Update docs
   ↓
PR
   ↓
Review
   ↓
Merge
   ↓
Archive OpenSpec change
```

## Punto importante: no hacer “backend de una sola vez”

El hecho de que M9 vaya antes de M10 en esta secuencia no significa que debas construir todo el backend antes de tocar cualquier frontend.

En una empresa real, una estrategia mejor para una aplicación full stack sería construir por **vertical slices**:

```text
Historia 1
 ├── datos
 ├── backend
 ├── frontend
 ├── tests
 └── PR

Historia 2
 ├── datos
 ├── backend
 ├── frontend
 ├── tests
 └── PR
```

El orden M8 → M9 → M10 es el orden de aprendizaje y dependencia principal de los módulos, no una obligación de hacer todo el backend antes de cualquier interfaz.

---

# 15. ORDEN 10 — Módulo 10: Programación asistida por IA — Frontend

## Posición

**10 de 10.**

## Por qué cierra la secuencia

El Módulo 10 aborda:

- buenas prácticas frontend;
- diseño → código;
- agentes;
- Figma/MCP;
- componentes;
- integración visual;
- revisión y refinamiento de interfaz.

El frontend necesita consumir contratos y capacidades reales del sistema.

Eso hace que el flujo general sea:

```text
producto
 ↓
contratos / specs
 ↓
data + backend
 ↓
UI integrada
```

## Importante: el frontend no debe esperar hasta el final en un proyecto real

Igual que con M9, esta posición indica la **última pieza del orden de módulos**, no una prohibición de trabajar frontend antes.

Una vez exista un contrato de API suficientemente estable, frontend y backend pueden avanzar en paralelo.

El Módulo 10 precisamente muestra que los agentes actuales pueden trabajar con diseño, Figma, código y navegador dentro de un mismo workflow.

## La dependencia técnica

En una aplicación full stack, la interfaz necesita conocer al menos:

- endpoints;
- request/response;
- autenticación;
- estados de error;
- validaciones;
- modelos de datos expuestos;
- reglas de negocio observables.

Eso procede de las capas anteriores.

---

# 16. El flujo completo recomendado para construir `Proyecto_Final_Master_AI4Devs`

La secuencia final que recomiendo es la siguiente.

## Fase 0 — Definición inicial

**Fuente:** lección del Proyecto Final + Ejemplo 2.

### Entregables

```text
Nombre del proyecto
Problema
Usuarios
Objetivo
MVP
Must-have
Should-have
Non-goals
Flujo principal E2E
Criterios de éxito
Idea de arquitectura inicial
Stack candidato
```

No se desarrolla código de producción todavía.

---

## Fase 1 — M1: modelo mental de IA

### Entregable

Un criterio claro sobre:

```text
Herramienta
Contexto
Prompt
```

y cómo interactuarán durante el desarrollo.

---

## Fase 2 — M3: entorno operativo del copiloto

### Entregables

```text
Herramienta principal
CLAUDE.md / instrucciones equivalentes
MCP necesarios
Skills útiles
Hooks necesarios
Política de permisos
Flujo Explore-Plan-Execute
```

Todavía no se desarrolla la aplicación completa.

---

## Fase 3 — M4: producto y planificación

### Entregables

```text
PRD
Epics
User Stories
Acceptance Criteria
Prioridad
Dependencias
Non-goals
Definition of Done
Backlog inicial
```

Este es el **qué**.

---

## Fase 4 — M5: arquitectura/documentación inicial

### Entregables

```text
README inicial
Arquitectura
C4 Context
C4 Containers
Modelo de datos conceptual
ADRs iniciales
Flujos principales
Decisiones de stack
```

Esto documenta y hace explícito el **cómo arquitectónico de alto nivel**.

---

## Fase 5 — M6: seguridad, privacidad y riesgos

### Entregables

```text
Datos sensibles
Threat model inicial
Requisitos de seguridad
Política de secretos
Política de datos enviados a proveedores IA
Privacidad
Consentimiento, si aplica
Riesgos regulatorios
Guardrails del agente
```

Esto introduce restricciones que deben aparecer en los cambios técnicos posteriores.

---

## Fase 6 — M2: SDD/OpenSpec

Ahora sí se empieza a construir **feature por feature**.

Para cada historia:

```text
User Story
 ↓
Explore
 ↓
proposal.md
 ↓
specs/
 ↓
design.md
 ↓
tasks.md
 ↓
revisión humana
```

No ejecutar aún sin revisar.

---

## Fase 7 — M7: testing

Antes de implementar la historia:

```text
Acceptance Criteria
 ↓
Scenarios
 ↓
Tests
 ↓
RED
```

Después:

```text
GREEN
 ↓
REFACTOR
```

---

## Fase 8 — M8: datos

Implementar los cambios de persistencia necesarios para la historia:

```text
schema
 ↓
migration
 ↓
constraints
 ↓
indexes
 ↓
queries
 ↓
tests
```

En un RAG:

```text
documentos
 ↓
chunks
 ↓
embeddings
 ↓
vector search
 ↓
retrieval
```

pero solamente donde realmente lo requiera el producto.

---

## Fase 9 — M9: backend

Implementar los casos de uso y APIs que requiere la historia.

```text
Domain / use case
 ↓
application
 ↓
ports
 ↓
adapters
 ↓
API
 ↓
tests
```

La arquitectura exacta debe seguir lo que realmente justifiquen los requisitos; el propio Módulo 9 advierte que la arquitectura hexagonal no es automáticamente adecuada para cualquier CRUD o prototipo.

---

## Fase 10 — M10: frontend

Construir la interfaz de la misma historia sobre los contratos reales.

```text
API contract
 ↓
UI
 ↓
state
 ↓
components
 ↓
interaction
 ↓
E2E
```

Usar el M10 especialmente para diseño → código, consistencia visual y validación visual.

---

# 17. El ciclo profesional real que debe repetirse después de la primera feature

Aquí está la diferencia fundamental entre “terminar los 10 módulos” y realmente trabajar como un equipo de software.

Los 10 módulos **no deben convertirse en una cascada única e irreversible**.

Después de la primera historia, el flujo debe ser iterativo:

```text
                  ┌──────────────────────────────┐
                  │          PRODUCTO            │
                  │ PRD / Backlog / prioridades  │
                  └──────────────┬───────────────┘
                                 ↓
                         User Story + AC
                                 ↓
                         Explore / Research
                                 ↓
                           OpenSpec
                                 ↓
                        Revisión humana
                                 ↓
                              Tests
                                 ↓
                         Data / Backend
                                 ↓
                            Frontend
                                 ↓
                      Integration / E2E
                                 ↓
                         Documentation
                                 ↓
                           Pull Request
                                 ↓
                         Human review
                                 ↓
                             CI/CD
                                 ↓
                             Merge
                                 ↓
                           Deploy
                                 ↓
                      Observability / feedback
                                 ↓
                         Backlog refinement
                                 ↓
                         siguiente story
```

En otras palabras:

```text
M4 ↔ M5 ↔ M6 ↔ M2 ↔ M7 ↔ M8 ↔ M9 ↔ M10
```

se convierte en un ciclo, no en una línea.

---

# 18. Por qué una empresa real no usaría una secuencia puramente lineal

El Manifiesto Ágil establece que:

- la prioridad es la entrega temprana y continua de valor;
- los requisitos pueden cambiar;
- el software funcional es la medida principal de progreso;
- debe existir atención continua a excelencia técnica y buen diseño;
- el equipo inspecciona y adapta regularmente.

Fuente: [Principios del Manifiesto Ágil](https://agilemanifesto.org/principles)

Por eso el siguiente modelo es más realista:

```text
                 PLANEACIÓN
                     ↓
              PRIMER VERTICAL SLICE
                     ↓
           SOFTWARE FUNCIONANDO
                     ↓
              FEEDBACK / REVIEW
                     ↓
                REPLANIFICAR
                     ↓
              SIGUIENTE SLICE
```

Esto también concuerda con el contenido del Módulo 4 sobre planificación ágil continua: el backlog, el sprint, la estimación y el plan deben actualizarse en función de lo aprendido.

---

# 19. La relación exacta entre Planificación, Documentación y SDD

Esta es la parte más importante de todo el análisis.

## Planificación responde

> **¿Qué producto estamos construyendo y qué valor entregaremos?**

Artefactos:

```text
PRD
Epic
Story
Acceptance Criteria
Prioridad
Non-goals
```

## Documentación arquitectónica responde

> **¿Qué arquitectura estamos proponiendo y por qué?**

Artefactos:

```text
C4
ADRs
modelo conceptual
diagramas
README
flujos
```

## SDD responde

> **¿Qué cambio concreto vamos a construir y qué comportamiento exacto debe cumplir?**

Artefactos:

```text
proposal.md
specs/
design.md
tasks.md
```

## Testing responde

> **¿Cómo demostraremos que el cambio funciona y no rompe lo anterior?**

Artefactos:

```text
tests
coverage
integration tests
E2E
```

## Implementación responde

> **¿Cómo traducimos ese contrato a software ejecutable?**

Artefactos:

```text
database
backend
frontend
```

La relación completa es:

```text
                 PRODUCTO
                    │
                    ▼
              PLANIFICACIÓN
                    │
                    ▼
             ARQUITECTURA
                    │
                    ▼
                RIESGOS
                    │
                    ▼
                  SDD
                    │
          ┌─────────┴─────────┐
          ▼                   ▼
       TESTING            DESIGN
          │                   │
          └─────────┬─────────┘
                    ▼
            IMPLEMENTACIÓN
                    │
          ┌─────────┴─────────┐
          ▼                   ▼
       BACKEND            FRONTEND
          │                   │
          └─────────┬─────────┘
                    ▼
             INTEGRACIÓN
                    │
                    ▼
                  CI/CD
                    │
                    ▼
               DEPLOYMENT
```

---

# 20. Por qué no recomiendo `Definición → SDD → Planificación`

Sería tentador porque SDD parece una metodología de construcción de software completa.

Pero produciría un problema conceptual:

```text
¿qué le estamos pidiendo a la spec que especifique?
```

Si todavía no has decidido:

- alcance;
- usuarios;
- prioridad;
- comportamiento del MVP;
- non-goals;
- aceptación;

entonces la IA puede generar una spec técnicamente detallada pero producto-incorrecta.

El Módulo 4 precisamente presenta el backlog como el nivel que alimenta a OpenSpec.

Por ello:

```text
PLANIFICACIÓN
     ↓
SPEC
```

es mucho más coherente que:

```text
SPEC
  ↓
PLANIFICACIÓN
```

Para cambios posteriores en un proyecto existente puede aparecer otro patrón:

```text
Issue
 ↓
Explore
 ↓
OpenSpec
 ↓
Implementation
```

pero eso ocurre **porque el producto y el sistema ya tienen contexto acumulado**.

---

# 21. Por qué tampoco recomiendo `Definición → Documentación completa → código`

Porque el M5 no debe convertirse en Big Design Up Front.

La documentación arquitectónica útil debe comenzar temprano, pero evolucionar junto al sistema.

Los ADRs existen para decisiones significativas y el propio módulo explica que los diagramas y decisiones deben vivir cerca del código.

Por tanto:

```text
Documentación inicial
       ↓
SDD
       ↓
implementación
       ↓
actualización de docs
       ↓
merge
       ↓
próxima historia
```

es mejor que:

```text
documentar absolutamente todo
       ↓
no tocar documentación nunca más
```

---

# 22. Qué significa “hacerlo como una empresa” en este contexto

La característica empresarial importante no es usar herramientas concretas como Cursor, Claude Code, OpenSpec, Figma o un MCP concreto.

Es tener un sistema de control del trabajo.

Ese sistema debería incluir:

```text
Producto
 ↓
Backlog
 ↓
Historia
 ↓
Criterios de aceptación
 ↓
Spec
 ↓
Tests
 ↓
Implementación
 ↓
PR
 ↓
Review
 ↓
CI
 ↓
Merge
 ↓
Deploy
 ↓
Observabilidad
 ↓
Feedback
```

GitHub documenta los pull requests como propuestas para incorporar cambios y como el mecanismo central para discutir y revisar cambios antes del merge. También permite requerir revisiones antes del merge mediante reglas de protección. [GitHub Pull Requests](https://docs.github.com/en/pull-requests/reference/pull-requests) y [GitHub Pull Request Reviews](https://docs.github.com/en/pull-requests/reference/pull-request-reviews).

Por tanto, la práctica profesional no debe ser:

```text
IA escribe → tú haces merge
```

sino:

```text
IA propone / implementa
        ↓
Humano inspecciona
        ↓
Tests + CI
        ↓
Review
        ↓
Merge
```

---

# 23. Orden final de los 10 módulos, resumido en una tabla

| Posición | Módulo | Papel | Dependencias principales | Por qué aquí |
|---:|---|---|---|---|
| 1 | M1 — 3 pilares | Modelo mental para usar IA | Ninguna | Todos los módulos posteriores dependen del buen uso de herramienta, contexto y prompt |
| 2 | M3 — Sistema operativo de copilotos | Harness, herramientas y EPE | M1 | Convierte el modelo mental en un workflow operativo |
| 3 | M4 — Planificación | PRD, backlog, stories, AC | Definición + M1/M3 | Define el “qué” y alimenta SDD |
| 4 | M5 — Documentación | Arquitectura, ADRs, C4, docs | M4 | Hace explícitas decisiones y contexto técnico antes de cambios de implementación |
| 5 | M6 — Ética/Seguridad/Privacidad | Requisitos de riesgo y seguridad | M4/M5 | Seguridad debe influir en diseño/spec, no ser parche posterior |
| 6 | M2 — SDD/OpenSpec | Contrato implementable por feature | M4/M5/M6 + M1/M3 | Formaliza el cambio concreto antes de código |
| 7 | M7 — Testing | Verificación y TDD | M2 + AC | Convierte criterios/spec en comprobación ejecutable antes/durante implementación |
| 8 | M8 — BBDD | Persistencia y búsqueda | M4/M5/M6/M2/M7 | Implementa el soporte de datos requerido por la feature |
| 9 | M9 — Backend | APIs y lógica de negocio | Todo lo anterior + M8 | Expresa el contrato en software servidor |
| 10 | M10 — Frontend | UI e integración visual | Contratos/backend + todo lo anterior | Consume las capacidades reales del sistema y cierra el flujo E2E |

---

# 24. Mapa de dependencias

```text
                        ┌──────────────────────┐
                        │ DEFINICIÓN PROYECTO  │
                        │ + EJEMPLO 2         │
                        └──────────┬───────────┘
                                   │
                                   ▼
                     ┌─────────────────────────┐
                     │ M1 — 3 PILARES         │
                     └────────────┬────────────┘
                                  │
                                  ▼
                     ┌─────────────────────────┐
                     │ M3 — COPILOTO           │
                     │ EXPLORE/PLAN/EXECUTE    │
                     └────────────┬────────────┘
                                  │
                                  ▼
                     ┌─────────────────────────┐
                     │ M4 — PLANIFICACIÓN      │
                     │ PRD / BACKLOG / STORIES │
                     └────────────┬────────────┘
                                  │
                                  ▼
                     ┌─────────────────────────┐
                     │ M5 — ARQUITECTURA       │
                     │ ADR / C4 / DOCS         │
                     └────────────┬────────────┘
                                  │
                                  ▼
                     ┌─────────────────────────┐
                     │ M6 — SEGURIDAD          │
                     │ PRIVACIDAD / RIESGOS    │
                     └────────────┬────────────┘
                                  │
                                  ▼
                     ┌─────────────────────────┐
                     │ M2 — SDD / OPENSPEC     │
                     │ PROPOSAL / SPEC / DESIGN│
                     │ TASKS                    │
                     └────────────┬────────────┘
                                  │
                                  ▼
                     ┌─────────────────────────┐
                     │ M7 — TESTING / TDD      │
                     └────────────┬────────────┘
                                  │
                                  ▼
                     ┌─────────────────────────┐
                     │ M8 — BASE DE DATOS      │
                     └────────────┬────────────┘
                                  │
                                  ▼
                     ┌─────────────────────────┐
                     │ M9 — BACKEND            │
                     └────────────┬────────────┘
                                  │
                                  ▼
                     ┌─────────────────────────┐
                     │ M10 — FRONTEND          │
                     └────────────┬────────────┘
                                  │
                                  ▼
                     ┌─────────────────────────┐
                     │ E2E / CI / REVIEW / PR  │
                     └────────────┬────────────┘
                                  │
                                  ▼
                             DEPLOYMENT
```

---

# 25. Pero el orden real de trabajo por historia es un grafo, no una lista

Cuando llegues a la primera historia, la secuencia se vuelve más precisa:

```text
M4
 │
 │ User Story + AC
 ▼
M5 ──────► arquitectura / ADR si hace falta
 │
 ▼
M6 ──────► seguridad / riesgos / privacidad
 │
 ▼
M2
 │
 │ proposal + specs + design + tasks
 ▼
M7
 │
 │ tests / AC verification
 ▼
 ├──────────────► M8 si necesita datos
 │
 ├──────────────► M9 backend
 │
 └──────────────► M10 frontend
                    │
                    ▼
                   E2E
                    │
                    ▼
             PR / review / CI
                    │
                    ▼
                  merge
                    │
                    ▼
               archive SDD
```

Esto es más parecido a cómo trabajaría un equipo profesional que una ejecución escolar de diez capítulos lineales.

---

# 26. Qué partes del M1–M10 son transversales y no deben “esperar su turno”

Esta distinción es crítica.

## M1 — transversal

Se aplica en todo prompt y sesión.

## M3 — transversal

Explore/Plan/Execute, contexto, skills, hooks y permisos se usan durante todo el desarrollo.

## M4 — transversal

El backlog se refina continuamente.

## M5 — transversal

La documentación se actualiza conforme cambian decisiones y código.

## M6 — transversal

La seguridad se reevalúa conforme cambian capacidades y amenazas.

## M7 — transversal

Los tests acompañan cada cambio.

## M8 — principalmente técnico, pero iterativo

Cada nueva feature que toca datos vuelve a pasar por diseño de datos, migraciones, queries y tests.

## M9 — implementación iterativa

No se hace una sola vez; se repite por story.

## M10 — implementación iterativa

Tampoco debe esperar a que esté terminado todo el backend; puede avanzar detrás de contratos estables.

---

# 27. Lo que cambiaría respecto al orden numérico actual

Orden actual de carpetas:

```text
M1 → M2 → M3 → M4 → M5 → M6 → M7 → M8 → M9 → M10
```

Orden profesional recomendado:

```text
M1 → M3 → M4 → M5 → M6 → M2 → M7 → M8 → M9 → M10
```

Los cambios decisivos son:

```text
M2 baja de posición 2 → 6
M3 sube de posición 3 → 2
M4 sube de posición 4 → 3
M5 → 4
M6 → 5
M7 → 7
M8 → 8
M9 → 9
M10 → 10
```

### ¿Por qué M2 no queda segundo?

Porque para **aprender** SDD puede perfectamente estudiarse temprano — de hecho el orden pedagógico original lo coloca ahí.

Pero para **aplicarlo a la construcción del proyecto**, primero necesitas la información que alimentará sus specs:

```text
producto
backlog
arquitectura
riesgos / restricciones
```

### ¿Por qué M3 sube?

Porque su contenido es operativo: prepara el agente que vas a usar para planificar, documentar, especificar e implementar.

### ¿Por qué M4 sube antes de M5?

Porque la arquitectura debe responder a necesidades del producto. No conviene diseñar la arquitectura sin saber qué capacidades del MVP realmente tienes que entregar.

### ¿Por qué M5 queda antes de M6?

Porque para analizar amenazas y riesgos de seguridad necesitas comprender qué sistema estás construyendo y cómo se comunica. OWASP también recomienda el threat modeling durante diseño.

### ¿Por qué M6 queda antes de M2?

Porque seguridad, privacidad y regulación generan restricciones que deben aparecer en requisitos/specs/diseño, y NIST recomienda integrar la seguridad durante el SDLC en lugar de añadirla únicamente después.

### ¿Por qué M7 queda antes de M8/M9/M10?

Porque los tests no deben ser el residuo de la implementación. El Módulo 7 muestra explícitamente el ciclo historia → criterio → test → código → refactor.

---

# 28. Cómo utilizar el Ejemplo 2 sin convertirlo en una arquitectura predeterminada

El uso correcto sería:

```text
Ejemplo 2
   ↓
observación
   ↓
comparación con tu problema
   ↓
decisión
   ↓
ADR
   ↓
requisito/spec si aplica
   ↓
implementación
```

No:

```text
Ejemplo 2
   ↓
“voy a copiar FastAPI + React + pgvector + GCP porque el ejemplo lo usa”
```

El propio archivo del repositorio advierte que los ejemplos deben utilizarse para aprender decisiones, estructura, pruebas, documentación y despliegue, pero no como molde idéntico.

Esto es importante también arquitectónicamente: una decisión del Ejemplo 2 solo debe convertirse en una decisión de tu sistema después de verificar requisitos y trade-offs.

---

# 29. Qué artefactos debería tener el nuevo proyecto

Sin imponer exactamente una estructura del Ejemplo 2, una organización coherente podría ser:

```text
Proyecto_Final_Master_AI4Devs/
│
├── README.md
├── prompts.md
├── docs/
│   ├── product/
│   │   ├── product.md
│   │   ├── backlog.md
│   │   └── mvp.md
│   │
│   ├── architecture/
│   │   ├── context.md
│   │   ├── containers.md
│   │   ├── flows/
│   │   └── workspace.dsl      # si realmente aporta valor
│   │
│   └── adr/
│
├── openspec/
│   ├── project.md
│   ├── specs/
│   └── changes/
│
├── backend/
├── frontend/
├── tests/
└── .github/
    └── workflows/
```

Esto es una **propuesta profesional**, no una copia del repositorio del curso.

---

# 30. Qué debería contener `prompts.md`

La lección del Proyecto Final aclara que el registro de IA evolucionó más allá de guardar únicamente prompts.

Debería documentar:

```text
Herramientas utilizadas
Modelos utilizados
Para qué se utilizó cada modelo
Skills
Subagentes
Rules
Comandos personalizados
Prompts/workflows importantes
Cambios humanos aplicados a outputs de IA
```

Esto es particularmente importante para tu objetivo porque el proyecto final evalúa también cómo se utilizó IA a lo largo del proceso.

---

# 31. Gobierno humano: dónde debe intervenir la persona

La IA puede acelerar:

- exploración;
- generación de documentación inicial;
- propuestas de arquitectura;
- expansión de criterios de aceptación;
- generación de tests;
- implementación;
- documentación de código;
- review asistido.

Pero los puntos de decisión humana deberían permanecer en:

```text
Producto
   ↓
Alcance
   ↓
Arquitectura
   ↓
Riesgo
   ↓
Aprobación de spec
   ↓
Review de implementación
   ↓
Merge
   ↓
Decisión de release
```

Esto encaja con la filosofía del Módulo 3: el gate humano se coloca especialmente antes de ejecutar un plan que pueda modificar estado real.

También encaja con GitHub: un PR reúne cambios, contexto y revisión antes del merge. [GitHub Docs](https://docs.github.com/en/pull-requests/reference/pull-requests)

---

# 32. Fuentes externas consultadas y qué respaldan

## 32.1 OpenSpec — fuente primaria

**OpenSpec, repositorio oficial de Fission-AI.**

Respalda:

- concepto de SDD;
- necesidad de acuerdo/spec antes del código;
- workflow `propose → apply → archive`;
- inicialización del proyecto;
- perfil core/expanded;
- requisitos de instalación actuales.

https://github.com/Fission-AI/OpenSpec  
https://github.com/Fission-AI/OpenSpec/blob/main/README.md  
https://github.com/Fission-AI/OpenSpec/blob/main/docs/installation.md

## 32.2 GitHub Spec Kit — fuente primaria

Respalda el uso de specifications como artefacto central del workflow SDD y la idea de que el “qué” debe definirse antes del “cómo”.

https://github.com/github/spec-kit  
https://github.com/github/spec-kit/blob/main/docs/concepts/sdd.md

## 32.3 NIST SSDF — fuente primaria

Respalda que la seguridad debe integrarse en cada SDLC y que desplazar la seguridad hacia etapas tempranas reduce esfuerzo y coste de corrección.

https://csrc.nist.gov/pubs/sp/800/218/final

## 32.4 NIST DevSecOps reference model

Respalda que Plan es una fase donde se definen requisitos funcionales, no funcionales y de seguridad y se evalúan riesgos, siguiendo una estrategia shift-left.

https://pages.nist.gov/nccoe-devsecops/notational-reference-model.html

## 32.5 OWASP Threat Modeling

Respalda que threat modeling debería realizarse preferentemente temprano, durante diseño, y mantenerse a medida que evoluciona el sistema.

https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html  
https://owasp.org/www-project-threat-modeling/

## 32.6 C4 Model — fuente oficial de su creador

Respalda el uso de niveles jerárquicos para documentar arquitectura: system, container, component y code, además de vistas de contexto, dinámica y despliegue.

https://c4model.com/

## 32.7 Agile Manifesto — principios originales

Respalda entrega incremental, adaptación al cambio, software funcionando como medida de progreso, excelencia técnica continua y reflexión periódica.

https://agilemanifesto.org/principles

## 32.8 GitHub Pull Requests / Reviews — documentación oficial

Respalda PRs como mecanismo de propuesta, discusión, revisión y aprobación de cambios antes de merge.

https://docs.github.com/en/pull-requests/reference/pull-requests  
https://docs.github.com/en/pull-requests/reference/pull-request-reviews

## 32.9 Martin Fowler — TDD

Respalda el ciclo Red-Green-Refactor y la preparación de casos de prueba antes de implementar.

https://martinfowler.com/bliki/TestDrivenDevelopment.html

## 32.10 NIST AI RMF

Para un sistema con componentes de IA, el AI RMF proporciona un marco de gestión de riesgos aplicable durante diseño, desarrollo, despliegue y evaluación de sistemas de IA.

https://www.nist.gov/itl/ai-risk-management-framework

El perfil de GenAI se encuentra en:

https://www.nist.gov/publications/artificial-intelligence-risk-management-framework-generative-artificial-intelligence

---

# 33. Precauciones sobre afirmaciones del propio repositorio

El contenido del repositorio contiene numerosas afirmaciones fechadas en 2025/2026 acerca de:

- modelos concretos;
- precios;
- adopción;
- productos;
- políticas de privacidad;
- versiones de herramientas;
- incidentes de seguridad;
- estadísticas;
- benchmarks;
- legislación;
- litigios;
- fechas de lanzamiento.

No es correcto convertir automáticamente todas esas afirmaciones en hechos independientes de la investigación.

Para este análisis he usado el repositorio como **fuente primaria de lo que el curso enseña y recomienda**, y fuentes externas primarias para contrastar los principios que afectan al orden de trabajo.

En particular, los precios, políticas de productos, versiones y estados regulatorios son datos susceptibles de cambiar y deben verificarse contra la fuente oficial correspondiente justo antes de ejecutar el proyecto.

Esta distinción es importante para cumplir el criterio de “sin inventar datos”.

---

# 34. Conclusión definitiva

Para construir `Proyecto_Final_Master_AI4Devs` como una aplicación web full stack profesional, utilizando el Ejemplo 2 como referencia y aprovechando realmente los 10 módulos, el orden que recomiendo es:

```text
PRE-FASE
Definir proyecto + estudiar Ejemplo 2

1. M1 — 3 pilares
   ↓
2. M3 — Sistema operativo de copilotos
   ↓
3. M4 — Planificación
   ↓
4. M5 — Documentación y arquitectura
   ↓
5. M6 — Ética / privacidad / seguridad
   ↓
6. M2 — SDD / OpenSpec
   ↓
7. M7 — Testing / TDD
   ↓
8. M8 — Bases de datos
   ↓
9. M9 — Backend
   ↓
10. M10 — Frontend
```

La respuesta específica a “¿después de la definición inicial del proyecto va planificación, documentación o SDD?” es:

```text
DEFINICIÓN INICIAL
        ↓
PLANIFICACIÓN DEL PRODUCTO
        ↓
ARQUITECTURA / DOCUMENTACIÓN INICIAL
        ↓
SEGURIDAD / PRIVACIDAD / RIESGOS
        ↓
SDD / OPENSPEC
        ↓
TESTING
        ↓
DATOS
        ↓
BACKEND
        ↓
FRONTEND
```

Y hay una precisión todavía más importante:

> **No debes interpretar este orden como un waterfall de diez etapas cerradas.**

El orden sirve para resolver las **dependencias iniciales y pedagógicas**. Una vez empieza la construcción, el proyecto debe convertirse en un ciclo iterativo por historias y vertical slices:

```text
Story
 → Explore
 → Plan
 → Spec
 → Test
 → Data/Backend/Frontend
 → E2E
 → Docs
 → PR
 → Review
 → CI
 → Merge
 → Archive
 → Feedback
 → siguiente story
```

Así se obtiene lo que realmente interesa: no solo completar los 10 módulos, sino utilizar sus conocimientos como un **sistema integrado de ingeniería de software asistida por IA**, donde planificación, especificación, arquitectura, seguridad, pruebas, datos, backend, frontend y revisión forman una cadena de trazabilidad.

---

# 35. Resumen en una sola frase

**Define primero el producto; planifícalo después; documenta y decide la arquitectura; identifica seguridad y privacidad temprano; convierte cada historia priorizada en una OpenSpec; deriva su verificación; implementa datos, backend y frontend en vertical slices; revisa mediante PR/CI; y repite el ciclo.**

---

# Referencias directas al repositorio analizado

- https://github.com/Diiegoal/CursoIA
- https://github.com/Diiegoal/CursoIA/tree/main/Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA
- https://github.com/Diiegoal/CursoIA/tree/main/Módulo_2_Spec_Driven_Development_(SDD)
- https://github.com/Diiegoal/CursoIA/tree/main/Módulo_3_Sistema_operativo_Copilotos_IA
- https://github.com/Diiegoal/CursoIA/tree/main/Módulo_4_Planificación_efectiva_con_IA
- https://github.com/Diiegoal/CursoIA/tree/main/Módulo_5_Documentación_efectiva_con_IA
- https://github.com/Diiegoal/CursoIA/tree/main/Módulo_6_Ética_Regulación_y_Privacidad_en_el_uso_de_IA
- https://github.com/Diiegoal/CursoIA/tree/main/Módulo_7_Testing_y_calidad_con_IA
- https://github.com/Diiegoal/CursoIA/tree/main/Módulo_8_Bases_de_datos
- https://github.com/Diiegoal/CursoIA/tree/main/Módulo_9_Programación_asistida_por_IA_backend
- https://github.com/Diiegoal/CursoIA/tree/main/Módulo_10_Programación_asistida_por_IA_frontend
- https://github.com/Diiegoal/CursoIA/blob/main/Proyecto_Final_Master_AI4Devs/Ejemplo_Proyectos_Finales_Reales.md
- https://github.com/Diiegoal/CursoIA/blob/main/Proyecto_Final_Master_AI4Devs/Leccion_1_Proyecto_Final_AI4Devs.md

---

## Nota de alcance de la investigación

La estructura recursiva de `main` fue verificada mediante GitHub y reporta el árbol como no truncado. Se revisaron los materiales clave que determinan directamente las dependencias del orden —proyecto final, ejemplos, fundamentos de IA, SDD/OpenSpec, Explore-Plan-Execute, planificación, arquitectura/documentación, seguridad, TDD, bases de datos, backend y frontend— y se contrastó la conclusión con fuentes primarias externas. Para afirmaciones concretas y cambiantes de proveedores, precios, versiones o regulación, se priorizaron las fuentes oficiales externas y no se asumieron como hechos únicamente por aparecer en las lecciones.
