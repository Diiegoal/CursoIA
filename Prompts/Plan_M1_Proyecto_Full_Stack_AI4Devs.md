# Plan de ejecución — Proyecto Full Stack con Claude Code
## Fase actual: Módulo 1 — Los 3 pilares del uso efectivo de copilotos IA

**Repositorio fuente:** `https://github.com/Diiegoal/CursoIA.git`  
**Módulo obligatorio inicial:** `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA`  
**Referencia complementaria:** `Proyecto_Final_Master_AI4Devs`  
**Ejemplo analizado:** `LIDR-academy/AI4Devs-finalproject-Example2`  
**Fecha de investigación:** 2026-09-01  
**Corte exigido por el usuario para información vigente:** agosto de 2026

---

# 1. Alcance de esta respuesta

El objetivo de esta respuesta es establecer, antes de ejecutar el Paso 1, el marco completo de trabajo para construir posteriormente un proyecto real, profesional y full stack con Claude Code, usando el contenido del Módulo 1 del repositorio `Diiegoal/CursoIA` como guía obligatoria.

No se ha avanzado todavía a la implementación funcional del producto.

La intención es trabajar por pasos controlados, verificables y acumulativos. Al terminar cada paso se ejecutarán las comprobaciones correspondientes, se documentarán los resultados y se decidirá explícitamente si puede abrirse el siguiente paso.

No se avanzará al Módulo 4 mientras el Módulo 1 no esté completamente ejecutado, auditado y verificado.

---

# 2. Limitaciones operativas reales

## 2.1. Acceso al PC local

No existe acceso directo a la computadora local del usuario desde este entorno. Por lo tanto, no es posible ejecutar físicamente `git clone` dentro del PC del usuario ni abrir Claude Code instalado allí.

Sí fue posible consultar el repositorio público mediante GitHub y analizar su contenido. También se intentó realizar un `git clone` en el entorno de trabajo aislado de esta sesión, pero ese entorno no pudo resolver `github.com`; esto no equivale al PC del usuario y no debe interpretarse como un problema de su configuración local.

La ejecución local deberá hacerse mediante los comandos que se proporcionarán en el Paso 1.

## 2.2. Creación del nuevo repositorio

La conexión GitHub disponible para esta sesión permite consultar repositorios públicos, ramas, commits y contenido, pero no proporciona en este momento una operación autorizada para crear un repositorio nuevo en la cuenta objetivo `DiiegoA`.

Por tanto, no se afirmará que el repositorio nuevo fue creado hasta disponer de una operación real y verificable. Cuando lleguemos a ese punto, se podrá crear mediante GitHub CLI (`gh repo create`) o mediante la interfaz de GitHub y después enlazar el remoto local.

---

# 3. Resultado de la inspección del repositorio fuente

El árbol `main` de `Diiegoal/CursoIA` confirma la existencia de:

- `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA`
- `Módulo_2_Spec_Driven_Development_(SDD)`
- `Módulo_3_Sistema_operativo_Copilotos_IA`
- `Módulo_4_Planificación_efectiva_con_IA`
- `Módulo_5_Documentación_efectiva_con_IA`
- `Módulo_6_Ética_Regulación_y_Privacidad_en_el_uso_de_IA`
- `Módulo_7_Testing_y_calidad_con_IA`
- `Módulo_8_Bases_de_datos`
- `Módulo_9_Programación_asistida_por_IA_backend`
- `Módulo_10_Programación_asistida_por_IA_frontend`
- `Proyecto_Final_Master_AI4Devs`

El árbol se obtuvo del branch `main` y estaba marcado como no truncado.

---

# 4. Contenido íntegro revisado del Módulo 1

El Módulo 1 contiene cinco archivos:

1. `1. El modelo mental de los 3 pilares.md`
2. `2. Pilar 1 — La Herramienta.md`
3. `3. Pilar 2 — El Contexto.md`
4. `4. Pilar 3 — El Prompt + Integración.md`
5. `5. Recursos adicionales.md`

Se revisó el contenido completo disponible de los cinco archivos, no únicamente sus títulos.

## 4.1. Lección 1 — El modelo mental

El módulo presenta tres pilares co-iguales:

- Herramienta
- Contexto
- Prompt

El mensaje principal es que la eficacia del desarrollo asistido por IA no debe reducirse a escoger el modelo "más potente". El entorno de herramientas, el contexto disponible y la formulación de la tarea influyen conjuntamente.

El módulo relaciona este enfoque con:

- Harness Engineering
- Context Engineering
- Prompt Engineering

También insiste en que el agente debe considerarse dentro de un sistema de herramientas, instrucciones, restricciones, contexto y memoria.

## 4.2. Lección 2 — La Herramienta

La taxonomía del módulo distingue:

- IDE-integrated
- Terminal/CLI agentic
- Standalone autonomous agents
- Herramientas especializadas

Además diferencia:

- completion
- agentic

y propone decidir la herramienta según:

1. Tamaño y forma del codebase
2. Lenguaje principal
3. Privacidad/compliance
4. Presupuesto
5. Estilo de trabajo del developer

Para el proyecto se tomará como principio la idea de que la herramienta se escoge a partir de la tarea, no al revés.

## 4.3. Lección 3 — El Contexto

La lección trata el contexto como un recurso que debe gestionarse, no acumularse.

Presenta cuatro estrategias:

1. Write
2. Select
3. Compress
4. Isolate

y recomienda utilizar archivos de contexto persistente y subagentes para evitar inundar la conversación principal.

El módulo menciona `AGENTS.md` como estándar multiagente y `CLAUDE.md` como mecanismo específico de Claude Code.

## 4.4. Lección 4 — El Prompt + Integración

La anatomía de prompt propuesta por el módulo contiene:

1. Contexto/rol corto, únicamente si aporta valor
2. Objetivo orientado al resultado
3. Criterios de éxito explícitos
4. Restricciones / antipatterns
5. Referencias a recursos y archivos
6. Formato de salida cuando sea necesario
7. Solicitud de aclaración ante ambigüedad

También presenta la integración de los tres pilares mediante el flujo:

```text
Caracterizar tarea
        ↓
Elegir herramienta
        ↓
Preparar contexto
        ↓
Escribir prompt
        ↓
Ejecutar y revisar
```

## 4.5. Recursos adicionales

La quinta lección reúne:

- Martin Fowler / Birgitta Böckeler
- METR
- arXiv
- Anthropic Claude Code
- GitHub Copilot
- Cursor
- Windsurf
- vals.ai
- SWE-rebench
- Aider
- Lance Martin / LangChain
- Simon Willison
- Phil Schmid
- AGENTS.md
- OpenAI Codex
- Anthropic / MCP
- Anthropic prompting
- OpenAI prompting
- investigación sobre razonamiento
- GitHub spec-kit
- Karpathy
- Tobi Lütke
- Simon Willison
- Geoffrey Huntley
- comunidades de agentes

Estos recursos forman parte de la fuente de trabajo del Módulo 1 y serán usados como material de contraste, no como autoridad automática.

---

# 5. Contraste con fuentes primarias y oficiales

## 5.1. Hecho verificado: CLAUDE.md

La documentación actual de Claude Code establece que `CLAUDE.md` es el mecanismo principal para instrucciones persistentes de proyecto y que Claude Code carga estos archivos al inicio de una sesión.

También documenta que:

- Claude Code lee `CLAUDE.md`.
- Si el repositorio utiliza `AGENTS.md`, se puede crear un `CLAUDE.md` que lo importe.
- En Windows, la importación `@AGENTS.md` es especialmente apropiada cuando no se desea depender de enlaces simbólicos.
- Los archivos `CLAUDE.md` pueden tener diferentes alcances.
- Los archivos de subdirectorios se vuelven relevantes según el alcance del trabajo.

Fuente oficial:
https://code.claude.com/docs/en/memory

## 5.2. Hecho verificado: AGENTS.md

`AGENTS.md` se presenta como un formato abierto para proporcionar contexto e instrucciones a coding agents.

La documentación pública de AGENTS.md permite:

- un `AGENTS.md` en la raíz;
- archivos `AGENTS.md` anidados para subproyectos;
- instrucciones específicas según proximidad al archivo editado.

Fuente:
https://agents.md/

## 5.3. Hecho verificado: subagentes

Claude Code documenta que los subagentes sirven para:

- aislar contexto;
- delegar tareas específicas;
- realizar exploraciones de gran volumen sin inundar la conversación principal;
- ejecutar investigación paralela cuando resulte útil.

Fuente oficial:
https://code.claude.com/docs/en/subagents

## 5.4. Hecho verificado: Plan Mode

La documentación de Claude Code confirma que el modo de planificación está diseñado para leer y proponer un plan sin hacer ediciones hasta la aprobación correspondiente.

Fuente oficial:
https://code.claude.com/docs/en/common-workflows

## 5.5. Hecho verificado: hooks

Claude Code proporciona hooks para ejecutar comandos antes o después de determinados eventos del ciclo de trabajo.

La documentación diferencia claramente las instrucciones de proyecto de los mecanismos deterministas de enforcement.

Fuente oficial:
https://code.claude.com/docs/en/hooks

## 5.6. Hecho verificado: configuración

La configuración de Claude Code incluye:

- memoria
- settings
- permisos
- skills
- MCP
- hooks

y permite denegar acceso a archivos sensibles.

Fuente oficial:
https://code.claude.com/docs/en/settings

## 5.7. Hecho verificado: context engineering

La investigación de Chroma documentó degradación del rendimiento de distintos modelos conforme aumenta el contexto, incluso antes de llegar al límite físico de la ventana.

Fuente:
https://www.trychroma.com/research/context-rot

La consecuencia que tomaremos es metodológica:

> no se debe llenar artificialmente la ventana de contexto solo porque técnicamente exista capacidad para hacerlo.

## 5.8. Hecho verificado: contexto como disciplina

Simon Willison documentó en junio de 2025 el uso creciente del término `context engineering` para describir la selección cuidadosa de la información necesaria para resolver una tarea.

Fuente:
https://simonwillison.net/2025/jun/27/context-engineering/

## 5.9. Hecho verificado: harness engineering

OpenAI publicó en febrero de 2026 un documento sobre `Harness engineering` basado en la construcción de un producto real con agentes.

El documento describe una práctica que coincide con el espíritu del Módulo 1:

- especificar intención;
- diseñar el entorno de trabajo del agente;
- hacer el sistema legible para los agentes;
- imponer límites arquitectónicos;
- crear bucles de feedback;
- automatizar validación;
- aumentar progresivamente la autonomía.

Fuente oficial:
https://openai.com/index/harness-engineering/

## 5.10. Matiz importante sobre METR

El Módulo 1 resume el estudio inicial de METR de 2025 y menciona el update de febrero de 2026 como una inversión del efecto.

La fuente de METR confirma que el análisis posterior obtuvo una estimación de speedup de -18% para un subconjunto de participantes, pero también afirma expresamente que ese segundo experimento sufría problemas de selección y que sus datos eran una evidencia débil del tamaño real del speedup.

Por tanto, para este proyecto:

- El dato de +19% de tiempo del estudio de 2025 se tratará como resultado específico de aquel estudio y contexto.
- El -18% del update de 2026 NO se tratará como una ley general sobre productividad.
- Las cifras de METR se citarán con su contexto y limitaciones.

Fuentes:
https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/
https://metr.org/blog/2026-02-24-uplift-update/

---

# 6. Correcciones metodológicas que adoptaremos

El Módulo 1 será obligatorio, pero sus afirmaciones fechadas, estadísticas y snapshots de herramientas serán contrastados antes de convertirse en una regla técnica permanente.

Esto es especialmente importante para:

- pricing;
- modelos disponibles;
- límites de contexto;
- nombres de versiones;
- cuotas;
- disponibilidad de funcionalidades;
- cifras de adopción;
- resultados experimentales;
- rankings;
- afirmaciones de "estándar".

Cuando una afirmación sea una recomendación del módulo y no una especificación oficial de una herramienta, se etiquetará como recomendación.

Cuando sea una afirmación factual susceptible de cambiar, se verificará con una fuente actual.

---

# 7. Regla específica para CLAUDE.md y AGENTS.md

No se crearán copias idénticas de ambos archivos en todos los directorios solo para aumentar su número.

La arquitectura inicial propuesta es:

```text
/
├── AGENTS.md
├── CLAUDE.md
├── .claude/
│   ├── settings.json
│   ├── agents/
│   ├── skills/
│   └── rules/
├── backend/
├── frontend/
├── docs/
└── tests/
```

La intención será:

```text
AGENTS.md
    ↑
    └── fuente compartida y portable

CLAUDE.md
    ↑
    └── instrucciones específicas de Claude Code
```

y, cuando exista una razón real de alcance, se podrán añadir archivos más específicos en:

```text
backend/AGENTS.md
backend/CLAUDE.md
frontend/AGENTS.md
frontend/CLAUDE.md
tests/AGENTS.md
tests/CLAUDE.md
docs/AGENTS.md
docs/CLAUDE.md
```

pero únicamente cuando su contenido sea específico de ese ámbito.

Esta decisión evita contradicciones y duplicación innecesaria.

---

# 8. Número máximo total de pasos del Módulo 1

Se establece un máximo de:

# **18 pasos**

No se pretende rellenar artificialmente los 18. Si dos pasos quedan correctamente cubiertos por una misma actividad verificable, se podrán completar conjuntamente, pero nunca se omitirá una comprobación obligatoria.

El Paso 1 será el primero en ejecutarse después de la aprobación del usuario.

---

# 9. Plan secuencial completo del Módulo 1

## Paso 1 — Preparación local y clone verificable

Objetivo:

- comprobar Git;
- comprobar GitHub CLI;
- comprobar Claude Code;
- clonar `Diiegoal/CursoIA`;
- verificar branch;
- verificar commit;
- comprobar que el directorio corresponde al repositorio correcto;
- preparar el workspace local sin modificar el repo fuente.

Comprobaciones:

- `git --version`
- `gh --version`
- `claude --version`
- `git remote -v`
- `git branch --show-current`
- `git status`
- `git rev-parse HEAD`
- existencia del directorio del Módulo 1.

No se modificará el repositorio fuente en este paso.

---

## Paso 2 — Auditoría del entorno de ejecución

Objetivo:

Identificar qué existe realmente en el PC y qué necesita instalarse.

Se comprobará:

- sistema operativo;
- shell;
- Git;
- GitHub CLI;
- Claude Code;
- Node/npm/pnpm si fueran necesarios;
- Docker si fuese necesario;
- autenticación GitHub;
- disponibilidad de terminal;
- configuración de Claude.

Resultado:

Una tabla de "disponible / no disponible / versión / acción requerida".

---

## Paso 3 — Construcción de la fuente de verdad del Módulo 1

Objetivo:

Crear una representación estructurada de todo lo que el módulo exige.

Se clasificarán:

- principios;
- prácticas;
- herramientas;
- configuraciones;
- anti-patrones;
- comprobaciones;
- recursos externos;
- afirmaciones sujetas a verificación.

No se convertirán automáticamente las opiniones del módulo en reglas.

---

## Paso 4 — Definición del contrato operativo del proyecto

Objetivo:

Traducir el Módulo 1 a reglas de trabajo concretas para el proyecto futuro.

Se fijará:

- qué puede hacer el agente;
- qué debe consultar;
- cuándo debe investigar;
- cuándo debe detenerse;
- cuándo debe pedir aclaración;
- qué resultados deben quedar registrados;
- cómo se validará una tarea;
- cómo se controlará el contexto.

---

## Paso 5 — Selección de Claude Code como herramienta principal

Objetivo:

Aplicar el Pilar 1 de manera consciente.

Se definirá:

- por qué Claude Code es la herramienta principal;
- qué tareas serán agentic;
- qué tareas podrán resolverse con operaciones menores;
- qué tareas requieren planificación;
- qué tareas podrán delegarse a subagentes.

No se seleccionarán herramientas adicionales por moda.

---

## Paso 6 — Diseño del harness inicial

Objetivo:

Convertir el repositorio en un entorno legible, predecible y verificable para Claude Code.

Se definirá:

- estructura de instrucciones;
- reglas persistentes;
- permisos;
- hooks;
- skills;
- subagentes;
- herramientas MCP realmente necesarias.

---

## Paso 7 — Creación de `AGENTS.md`

Objetivo:

Crear la fuente portable de contexto del proyecto.

Contenido previsto:

- propósito del proyecto;
- stack una vez definido;
- arquitectura;
- comandos;
- convenciones;
- testing;
- seguridad;
- workflow;
- restricciones;
- gotchas;
- criterios de calidad.

Se evitará incluir documentación extensa que el agente pueda consultar bajo demanda.

---

## Paso 8 — Creación de `CLAUDE.md`

Objetivo:

Configurar el comportamiento específico de Claude Code.

La primera estrategia será evitar duplicación y usar la importación del contexto común:

```md
@AGENTS.md
```

Después podrán añadirse reglas realmente específicas de Claude Code.

---

## Paso 9 — Instrucciones con alcance por directorio

Objetivo:

Separar las reglas por ámbitos cuando el proyecto realmente lo requiera.

Se analizará la necesidad de:

- backend;
- frontend;
- tests;
- documentación;
- scripts;
- infraestructura.

Solo se crearán archivos específicos donde la especialización produzca una mejora real.

---

## Paso 10 — Política de Context Engineering

Objetivo:

Aplicar el Pilar 2.

Se establecerán reglas para:

- Select;
- Write;
- Compress;
- Isolate;
- usar referencias a archivos;
- evitar pegar código innecesariamente;
- usar subagentes para investigación pesada;
- reiniciar sesiones cuando sea más seguro que continuar;
- conservar artefactos de estado.

El modelo de 50/70/90 del Módulo 1 se tratará como heurística, no como límite oficial de Claude Code.

---

## Paso 11 — Arquitectura de subagentes

Objetivo:

Definir cuándo delegar.

Se estudiará la necesidad de subagentes específicos para:

- exploración;
- investigación técnica;
- revisión;
- testing;
- seguridad;
- documentación.

Cada subagente deberá tener:

- propósito;
- alcance;
- herramientas mínimas;
- formato de salida;
- criterio de finalización.

---

## Paso 12 — Contrato de prompting

Objetivo:

Aplicar el Pilar 3.

Toda tarea importante seguirá una estructura equivalente a:

```text
Contexto relevante
Objetivo
Criterios de éxito
Restricciones
Referencias
Formato esperado
Condición de aclaración
```

No se crearán megaprompts permanentes.

---

## Paso 13 — Workflow operativo de sesiones

Objetivo:

Aplicar la integración de los tres pilares.

El flujo base será:

```text
Caracterizar tarea
        ↓
Herramienta
        ↓
Contexto
        ↓
Prompt
        ↓
Ejecución
        ↓
Validación
        ↓
Registro
```

Cuando corresponda:

```text
Explore
   ↓
Plan
   ↓
Gate humano
   ↓
Execute
```

---

## Paso 14 — Protocolo Git y reversibilidad

Objetivo:

Hacer que el trabajo del agente sea reversible y auditable.

Se definirá:

- ramas;
- commits;
- naming;
- checkpoints;
- rollback;
- cuándo hacer commits;
- cuándo no realizar operaciones destructivas;
- cómo revisar diffs.

---

## Paso 15 — Seguridad del agente

Objetivo:

Aplicar los principios de harness y seguridad del Módulo 1 sin esperar al Módulo 6.

Se configurará la separación entre:

- instrucciones;
- permisos;
- hooks;
- acceso a secretos.

Se estudiará la denegación de acceso a:

- `.env`;
- secretos;
- credenciales;
- archivos sensibles.

La documentación oficial de Claude Code confirma que permisos/hook mechanisms son más adecuados que una simple instrucción textual cuando se necesita una garantía.

---

## Paso 16 — Ejercicio controlado con Claude Code

Objetivo:

Realizar una primera tarea real, pequeña, reversible y totalmente verificable.

La tarea será deliberadamente limitada para validar:

- que Claude lee las instrucciones;
- que entiende el contexto;
- que sigue el prompt;
- que utiliza las herramientas correctas;
- que respeta restricciones;
- que reporta sus resultados;
- que no invade otras áreas.

Este será el primer experimento práctico del sistema de trabajo.

---

## Paso 17 — Auditoría del Módulo 1

Objetivo:

Comparar el sistema real construido contra todo el contenido del Módulo 1.

Se comprobará:

- Pilar 1 cubierto;
- Pilar 2 cubierto;
- Pilar 3 cubierto;
- recursos importantes revisados;
- anti-patrones contemplados;
- contexto persistente funcionando;
- subagentes funcionando;
- workflow reproducible;
- verificaciones funcionando.

---

## Paso 18 — Gate formal para abandonar Módulo 1

El Módulo 1 solo se considerará terminado si:

```text
[✓] Herramienta definida y validada
[✓] Contexto persistente funcionando
[✓] AGENTS.md validado
[✓] CLAUDE.md validado
[✓] Alcances por directorio justificados
[✓] Política de contexto definida
[✓] Subagentes definidos
[✓] Contrato de prompting definido
[✓] Workflow de sesiones definido
[✓] Seguridad inicial aplicada
[✓] Git/reversibilidad verificados
[✓] Ejercicio práctico completado
[✓] Salida validada
[✓] Módulo 1 auditado
```

Solo después de este gate se permitirá avanzar al Módulo 4.

---

# 10. Ejemplo 2 — referencia arquitectónica, no plantilla

El repositorio `LIDR-academy/AI4Devs-finalproject-Example2` fue inspeccionado como referencia.

Entre los elementos observables del repositorio aparecen:

- backend FastAPI;
- carpetas `app`, `docs`, `scripts`, `tests`;
- Alembic;
- Dockerfile;
- `cloudbuild.yaml`;
- `prompts.md`;
- infraestructura cloud;
- documentación estructurada;
- pruebas;
- separación entre componentes;
- trazabilidad de las decisiones.

El README del ejemplo organiza, entre otras áreas:

- ficha;
- descripción del producto;
- arquitectura;
- modelo de datos;
- API;
- historias;
- tickets;
- despliegue.

La intención para nuestro proyecto no será copiar su stack ni sus detalles de dominio.

La referencia se utilizará para identificar prácticas maduras que puedan reutilizarse:

- documentación;
- observabilidad del proceso;
- trazabilidad;
- testing;
- separación de responsabilidades;
- despliegue;
- disciplina del repositorio.

---

# 11. Principio de no invención

Durante todo el proyecto:

1. No se inventarán requisitos de negocio.
2. No se inventarán datos del dominio.
3. No se inventarán APIs.
4. No se inventarán capacidades de herramientas.
5. No se inventarán versiones.
6. No se afirmará que una prueba pasó si no fue ejecutada.
7. No se afirmará que un repositorio fue creado si no existe verificación.
8. No se afirmará que Claude Code leyó algo si no existe evidencia de esa ejecución.
9. Las decisiones de arquitectura deberán quedar justificadas.
10. Las afirmaciones externas deberán separar hechos de recomendaciones.

---

# 12. Estructura de verificación para cada paso

Cada paso futuro tendrá exactamente esta estructura:

## A. Objetivo

Qué se pretende conseguir.

## B. Fuente del requisito

Qué parte del Módulo 1 lo exige o qué fuente oficial lo respalda.

## C. Acción

Qué se ejecutará realmente.

## D. Resultado esperado

Qué debería observarse.

## E. Comprobaciones

Comandos, inspecciones o pruebas objetivas.

## F. Hallazgos

Qué ocurrió realmente.

## G. Correcciones

Qué se cambió si apareció un problema.

## H. Checklist

Lista de aceptación del paso.

## I. Gate

Estado:

- PASA
- PASA CON OBSERVACIONES
- NO PASA

No se abrirá el siguiente paso si el paso actual tiene un fallo crítico.

---

# 13. Investigación primaria priorizada

Fuentes principales usadas para establecer las reglas actuales de trabajo:

### Claude Code — documentación oficial

https://code.claude.com/docs/en/memory

https://code.claude.com/docs/en/subagents

https://code.claude.com/docs/en/common-workflows

https://code.claude.com/docs/en/hooks

https://code.claude.com/docs/en/settings

https://code.claude.com/docs/en/claude-directory

### AGENTS.md

https://agents.md/

### OpenAI — Harness Engineering

https://openai.com/index/harness-engineering/

### Anthropic — MCP / Agentic AI Foundation

https://www.anthropic.com/news/donating-the-model-context-protocol-and-establishing-of-the-agentic-ai-foundation

### Context Rot

https://www.trychroma.com/research/context-rot

### Simon Willison — Context Engineering

https://simonwillison.net/2025/jun/27/context-engineering/

### METR — Productivity

https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/

https://metr.org/blog/2026-02-24-uplift-update/

### Repositorio fuente

https://github.com/Diiegoal/CursoIA

### Ejemplo 2

https://github.com/LIDR-academy/AI4Devs-finalproject-Example2

---

# 14. Estado actual

```text
Repositorio fuente inspeccionado:        ✓
Módulo 1 identificado:                   ✓
Lecciones 1–4 revisadas íntegramente:   ✓
Recursos adicionales revisados:         ✓
Ejemplo 2 inspeccionado:                 ✓
Fuentes primarias externas consultadas: ✓
Diferencias hecho/recomendación:        ✓
Limitaciones operativas documentadas:   ✓
Plan máximo definido:                   ✓ — 18 pasos
Paso 1 ejecutado:                       NO
Módulo 1 completado:                    NO
Módulo 4 iniciado:                      NO
```

---

# 15. Decisión requerida antes de ejecutar

## Paso siguiente: Paso 1 — Preparación local y clone verificable

En el siguiente paso se trabajará exclusivamente sobre:

- acceso local;
- `git clone`;
- verificación de identidad del repositorio;
- branch;
- commit;
- estado inicial;
- herramientas necesarias.

No se comenzará todavía a diseñar funcionalidades del producto ni se avanzará al Módulo 4.

**Esperando autorización para iniciar el Paso 1.**