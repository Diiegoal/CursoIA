# Proyecto Final Master AI4Devs — Preparación y plan de ejecución del Módulo 1

**Fecha:** 2026-09-02  
**Repositorio fuente:** `https://github.com/Diiegoal/CursoIA.git`  
**Repositorio objetivo:** `DiiegoA/Proyecto_Final_Master_AI4Devs`  
**Módulo inicial obligatorio:** `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA`  
**Referencia principal del proyecto:** `Proyecto_Final_Master_AI4Devs/Ejemplo_Proyectos_Finales_Reales.md` → Ejemplo 2  
**Herramienta principal prevista:** Claude Code  
**Estado:** fase de preparación terminada; Paso 1 todavía NO iniciado.

---

## 1. Qué se hizo antes de pedir autorización para empezar

Se accedió al repositorio público `Diiegoal/CursoIA` mediante la integración de GitHub y se inspeccionó su árbol `main`. El árbol disponible confirma la presencia del Módulo 1, los módulos posteriores, la carpeta `Prompts` y la carpeta `Proyecto_Final_Master_AI4Devs`. El árbol consultado estaba marcado como no truncado. fileciteturn1file0L2-L2

También se intentó hacer un `git clone` real de `https://github.com/Diiegoal/CursoIA.git` en el entorno aislado de esta sesión. La operación falló porque este entorno no pudo resolver `github.com`. Esto no es una ejecución sobre el PC local del usuario y, por tanto, no demuestra ningún problema en la máquina del usuario.

**Limitación real:** este entorno no tiene acceso directo al PC del usuario, por lo que no puede ejecutar físicamente el `git clone` ni abrir Claude Code instalado en su máquina. El Paso 1 queda diseñado para ejecutarse en el PC del usuario. No se debe afirmar que el clone local fue realizado hasta que exista una comprobación local real.

Se comprobó además que `DiiegoA/Proyecto_Final_Master_AI4Devs` no existe actualmente en GitHub: la consulta directa del repositorio devuelve `404 Not Found`. Por tanto, no se afirmará que ese repositorio ha sido creado hasta que exista evidencia real.

---

# 2. Material del repositorio que se revisó

## 2.1. Módulo 1

El Módulo 1 contiene cinco archivos:

1. `1. El modelo mental de los 3 pilares.md`
2. `2. Pilar 1 — La Herramienta.md`
3. `3. Pilar 2 — El Contexto.md`
4. `4. Pilar 3 — El Prompt + Integración.md`
5. `5. Recursos adicionales.md`

Se revisó el contenido completo disponible de estos cinco archivos, no solo los títulos.

La estructura del módulo y sus cinco archivos están confirmados en el repositorio. El árbol del proyecto contiene precisamente estas cinco piezas dentro de `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA`. fileciteturn1file0L2-L2

### Lección 1 — El modelo mental de los tres pilares

El módulo establece tres pilares co-iguales:

- **Herramienta**: modelo + harness/scaffolding + herramientas + permisos + workflows.
- **Contexto**: la información que el agente necesita realmente en cada momento.
- **Prompt**: objetivo, criterios de éxito, restricciones, referencias y formato de salida.

El módulo conecta este modelo con `Harness Engineering`, `Context Engineering` y `Prompt Engineering` y sostiene que la calidad del resultado depende de la combinación de los tres, no de seleccionar simplemente el modelo “más potente”. fileciteturn20file0L2-L6

La lección también introduce como idea operativa que un agente debe considerarse dentro de un sistema de herramientas, contexto, instrucciones, restricciones y memoria, no como una caja negra que recibe una frase y produce código.

### Lección 2 — Pilar 1: La Herramienta

El módulo propone escoger herramientas según la tarea y el nivel de control requerido, no por popularidad.

Clasifica las herramientas en:

- IDE-integrated.
- Terminal/CLI agentic.
- Agentes autónomos en cloud.
- Herramientas especializadas.

Distingue además `completion` de `agentic` y propone cinco criterios para seleccionar herramienta:

1. Tamaño y forma del codebase.
2. Lenguaje principal.
3. Privacidad y compliance.
4. Presupuesto.
5. Estilo de trabajo del developer.

Para el proyecto actual, el principio que se conserva es: **primero se caracteriza la tarea y después se decide el modo y la herramienta apropiados**. fileciteturn21file0L2-L5

### Lección 3 — Pilar 2: El Contexto

El módulo presenta el contexto como recurso que debe curarse, no acumularse.

Sus cuatro estrategias centrales son:

1. **Write** — persistir fuera de la ventana aquello que no se necesita en el turno.
2. **Select** — elegir solo el contexto relevante.
3. **Compress** — resumir/compactar antes de seguir acumulando.
4. **Isolate** — aislar tareas mediante subagentes o sesiones separadas.

También explica el papel de los archivos persistentes `AGENTS.md` y `CLAUDE.md`, la conveniencia de mantener instrucciones de alta señal y el uso de subagentes para que resultados voluminosos no contaminen la conversación principal. fileciteturn22file0L2-L6

El módulo propone la heurística 50/70/90 para manejo práctico de contexto; esta se usará como **heurística del curso**, no como un límite oficial de Claude Code.

### Lección 4 — Pilar 3: El Prompt + Integración

La anatomía de prompt que aparece en el módulo es:

1. Contexto/rol corto cuando realmente aporta valor.
2. Objetivo orientado al resultado.
3. Criterios de éxito explícitos.
4. Restricciones y antipatterns.
5. Referencias a archivos y documentación.
6. Formato de salida cuando sea necesario.
7. Condición para pedir aclaración antes de actuar.

El módulo integra los tres pilares en este flujo:

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

Para tareas grandes propone además:

```text
Explore
   ↓
Plan
   ↓
Gate humano
   ↓
Execute
```

Los anti-patrones principales son la vaguedad, los megaprompts, la sobre-especificación innecesaria, la ausencia de criterios de éxito, mezclar muchas tareas en un mismo turno y volver a pegar inline instrucciones persistentes que ya están disponibles. fileciteturn25file0L2-L6

### Recursos adicionales

La lección 5 reúne recursos externos agrupados por pilar. Entre ellos están Martin Fowler/Birgitta Böckeler, METR, arXiv, documentación de Anthropic, GitHub, Cursor, vals.ai, SWE-rebench, Aider, LangChain/Lance Martin, Simon Willison, Phil Schmid, AGENTS.md, OpenAI Codex, MCP, prompting de Anthropic/OpenAI, investigación sobre razonamiento, GitHub spec-kit, Karpathy, Tobi Lütke y comunidades de agentes. fileciteturn24file0L2-L6

**Observación importante sobre videos:** el árbol de GitHub del Módulo 1 contiene documentos Markdown, no archivos de video. Por tanto, no existe un corpus de vídeos binarios dentro de esa carpeta que pueda “leerse” desde GitHub. Los materiales de vídeo son referencias externas cuando las notas proporcionan un enlace.

---

# 3. Material transversal del repositorio que también es relevante

El repositorio contiene `Prompts/Plan_M1_Proyecto_Full_Stack_AI4Devs.md`, un documento explícitamente dedicado a planificar la ejecución de un proyecto full stack con Claude Code bajo el Módulo 1. Su contenido es relevante porque no es simplemente una lección teórica: especifica un workflow operativo por pasos, criterios de verificación, limitaciones y gates. fileciteturn28file0L2-L6

Ese documento establece un **máximo de 18 pasos** para el Módulo 1 y define como condición de salida que la herramienta, el contexto persistente, la política de prompting, el workflow y la verificación estén funcionando. fileciteturn30file0L2-L6 fileciteturn31file0L2-L6

El mismo documento separa explícitamente:

- preparación local;
- auditoría del entorno;
- creación de una fuente de verdad del módulo;
- contrato operativo del agente;
- selección de herramienta;
- diseño del harness;
- `AGENTS.md`;
- `CLAUDE.md`;
- reglas por directorio;
- política de context engineering;
- subagentes;
- prompting;
- workflow de sesiones;
- Git/reversibilidad;
- seguridad;
- ejercicio controlado;
- auditoría final;
- gate de cierre. fileciteturn30file0L2-L6 fileciteturn31file0L2-L6

Se respetará esta estructura, corrigiendo únicamente lo necesario para alinearla con la documentación oficial vigente y con la instrucción actual del usuario de continuar después con el Módulo 3, no con el Módulo 4.

---

# 4. Referencia del Proyecto Final: Ejemplo 2

También se inspeccionó el `Ejemplo_Proyectos_Finales_Reales.md` incluido en `Diiegoal/CursoIA/Proyecto_Final_Master_AI4Devs`.

El propio documento dice que los ejemplos deben utilizarse como referencia de estructura y calidad, no como molde para copiar. fileciteturn2file0L2-L10

## Lo que documenta el Ejemplo 2

El ejemplo es un chatbot RAG orientado a portfolio profesional, con backend FastAPI, frontend React, embeddings, pgvector, un LLM, analytics, captura gradual de leads, GDPR, rate limiting, documentación, tests e infraestructura cloud. fileciteturn2file0L2-L10

El README del ejemplo organiza explícitamente:

- Ficha del proyecto.
- Descripción del producto.
- Arquitectura.
- Modelo de datos.
- Especificación de API.
- Historias de usuario.
- Tickets.
- Pull requests.
- Documentación adicional.

La estructura técnica observada incluye `app`, `docs`, `scripts`, `tests`, Alembic, Dockerfile, `cloudbuild.yaml`, `prompts.md` y documentación separada por temas. fileciteturn857341view1L473-L550

El ejemplo también incorpora elementos de seguridad, observabilidad y performance, incluidos rate limiting, validación, gestión de secretos, métricas y health checks. fileciteturn587052view2L662-L700

Sus pruebas comprenden testing unitario, integración, sistema/E2E, performance y seguridad. El README presenta, entre otras, comprobaciones para respuestas HTTP, tiempos de respuesta, rate limiting y seguridad. fileciteturn857341view2L801-L879

### Importante: qué NO se copiará

No se copiarán automáticamente:

- el stack exacto;
- la estructura interna exacta;
- nombres de dominio;
- decisiones de infraestructura;
- valores de rendimiento;
- cifras de coste;
- afirmaciones de cumplimiento;
- ni ninguna capacidad que no se justifique para nuestro caso.

El ejemplo funciona como **fuente de patrones y criterios de calidad**, no como lista de requisitos preaprobados.

---

# 5. Investigación actualizada hasta septiembre de 2026

La investigación externa se contrastó con fuentes primarias o de alta autoridad, dando prioridad a documentación oficial.

## 5.1. Claude Code: memoria persistente

La documentación oficial actual de Claude Code establece que:

- cada sesión comienza con una ventana de contexto nueva;
- `CLAUDE.md` es el mecanismo de instrucciones persistentes del proyecto;
- `CLAUDE.md` se carga al inicio de la sesión;
- las instrucciones deben ser específicas, concisas y estables;
- la documentación recomienda mantener cada `CLAUDE.md` por debajo de aproximadamente 200 líneas;
- reglas que solo aplican a una parte del repositorio se pueden mover a reglas con alcance por ruta;
- Claude Code puede importar `AGENTS.md` desde `CLAUDE.md` mediante `@AGENTS.md`;
- los archivos `AGENTS.md` y `CLAUDE.md` pueden convivir sin duplicar todo su contenido. citeturn176439view0

Esto confirma una de las decisiones fundamentales del proyecto: **no debemos construir un sistema de instrucciones gigantesco**. La calidad del harness depende también de mantener el contexto persistente pequeño y de alta señal.

## 5.2. Claude Code: Explore → Plan → Implement → Commit

La guía oficial actual de mejores prácticas de Claude Code recomienda separar exploración, planificación e implementación. El flujo documentado es:

1. Explore en modo de planificación/read-only.
2. Elaborar un plan.
3. Revisar el plan antes de ejecutar.
4. Implementar y verificar.
5. Hacer commit y abrir PR cuando corresponda.

La misma guía establece que planificar es especialmente útil cuando el cambio afecta varios archivos, cuando el enfoque no es obvio o cuando el área del codebase es desconocida; para cambios minúsculos puede introducir overhead innecesario. citeturn662484view0L88-L139

Esto coincide directamente con el Módulo 1: no se debe convertir “Plan Mode” en una ceremonia para absolutamente todo; se aplica cuando reduce riesgo.

## 5.3. Verificación como parte de la tarea

Las mejores prácticas oficiales actuales de Claude Code recomiendan definir criterios de verificación y hacer que el agente muestre evidencia de ejecución —salida de tests, comandos, resultados o capturas— en vez de declarar simplemente “funciona”. La documentación distingue entre una comprobación pedida en el prompt, un goal, un Stop hook determinista y una segunda opinión independiente. citeturn662484view0L72-L82

Adoptaremos esta regla como parte central del proyecto:

> **Ningún paso se considerará completado únicamente porque Claude Code diga que terminó. Debe existir evidencia verificable.**

## 5.4. Subagentes

La documentación oficial de Claude Code explica que los subagentes tienen contexto propio, herramientas y permisos configurables, y que son especialmente útiles para tareas de investigación o búsqueda que producirían demasiado contenido para la conversación principal. citeturn662484view1L116-L132

También documenta agentes integrados como `Explore` y `Plan`, precisamente para aislar exploración y planificación del hilo principal cuando conviene. citeturn662484view1L135-L148

Esto respalda la aplicación práctica de `Isolate` del Módulo 1.

## 5.5. Hooks

La documentación oficial de Claude Code define hooks como mecanismos automáticos que se ejecutan en puntos concretos del ciclo de vida, incluyendo `PreToolUse`, `PostToolUse`, `Stop`, `SessionStart`, `SessionEnd`, eventos de subagentes y otros. citeturn662484view2L164-L182

La implicación profesional es importante:

- una instrucción textual expresa una intención al agente;
- un hook puede actuar como mecanismo determinista de control;
- los permisos son otra capa diferente;
- por tanto, las garantías críticas no deben depender únicamente de lenguaje natural.

## 5.6. AGENTS.md como formato abierto

La especificación pública de AGENTS.md lo presenta como un formato abierto para proporcionar contexto a coding agents. Permite un archivo raíz y archivos anidados en subproyectos. También promueve mantener allí setup, comandos, estilo, testing y seguridad que un agente necesita. citeturn886043search1

GitHub documenta además que su ecosistema de agentes puede consumir `AGENTS.md`, `CLAUDE.md` y otros mecanismos de instrucciones según la superficie utilizada. citeturn973857search0turn973857search3

## 5.7. Claude Code y AGENTS.md: decisión concreta

La documentación oficial de Claude Code dice explícitamente que Claude Code lee `CLAUDE.md`, no `AGENTS.md` directamente; si el repositorio ya usa `AGENTS.md`, recomienda que `CLAUDE.md` lo importe. Para Windows, la propia documentación señala la importación `@AGENTS.md` como alternativa práctica a enlaces simbólicos. citeturn176439view0L161-L180

Por eso, la arquitectura prevista para el proyecto es:

```text
AGENTS.md
    ↑
    │ fuente común y portable
    │
CLAUDE.md
    └── @AGENTS.md
        + reglas específicas de Claude Code solo cuando sean realmente necesarias
```

## 5.8. Reglas por subdirectorio

Claude Code documenta actualmente reglas modulares bajo `.claude/rules/` y reglas condicionadas por rutas. También explica que los archivos `CLAUDE.md` de subdirectorios se incorporan cuando el trabajo entra en esos directorios. citeturn176439view0L203-L244

Por tanto, no vamos a crear automáticamente ocho pares de archivos por “buenas prácticas” genéricas. Se crearán archivos por ámbito únicamente cuando existan reglas específicas y repetibles que aporten señal real.

## 5.9. Context engineering

La investigación de Chroma sobre `Context Rot` evaluó 18 modelos y observó que el rendimiento se vuelve menos fiable conforme crece el contexto, incluso antes de llenar la ventana. citeturn453435search2

Simon Willison también documentó en junio de 2025 la consolidación del término `context engineering` para describir la disciplina de aportar al modelo el contexto suficiente y correcto para que una tarea sea resoluble. citeturn453435search3

Por eso se conserva el principio del módulo:

> **más contexto disponible no implica mejor contexto.**

## 5.10. Harness engineering

OpenAI publicó en febrero de 2026 un análisis de `Harness engineering` basado en el desarrollo de un producto desde un repositorio vacío y en la creación de mecanismos que hacen que el agente pueda comprender, modificar y verificar el sistema con más fiabilidad. citeturn453435search6

Esta fuente refuerza la parte del Módulo 1 que trata herramienta + reglas + verificación + legibilidad del repositorio como un sistema único.

## 5.11. Productividad: matiz a METR

La lección del curso menciona resultados de METR de 2025 y el update de 2026. La propia organización METR explica que el estudio de 2025 encontró que las tareas tardaban aproximadamente un 19% más con IA en aquel contexto, mientras que el estudio posterior estimó un speedup de -18% para un subconjunto de participantes, pero señaló problemas importantes de selección y medición que vuelven débil la inferencia sobre el tamaño real del speedup. citeturn453435search0

Por eso no se utilizará “la IA acelera/desacelera X%” como regla universal del proyecto. Se usará como evidencia de que **el contexto del trabajo y la forma de uso importan**.

---

# 6. Decisiones profesionales que se adoptarán para este proyecto

A continuación se separan claramente las decisiones propias de este proyecto respecto de los hechos anteriores.

## Decisión 1 — Claude Code será el agente principal

**Motivo profesional:** el proyecto se va a desarrollar con un flujo agentic de tareas multiarchivo, revisión de diffs, ejecución de comandos, tests y trabajo sobre un repositorio real. Claude Code es adecuado para este tipo de flujo porque ofrece memoria de proyecto, plan mode, subagentes y hooks.

Esto no significa que sea “la mejor herramienta para todo”. Significa que se adapta al trabajo que se ha decidido hacer.

## Decisión 2 — No cambiaremos de herramienta por benchmark

El proyecto no se convertirá en una comparativa permanente de agentes. La herramienta principal se mantendrá estable mientras el flujo sea adecuado.

Los recursos del Módulo 1 se usarán para decidir cuándo un modo o herramienta deja de ser apropiado, no para generar un ciclo infinito de evaluación.

## Decisión 3 — `AGENTS.md` será la capa portátil y `CLAUDE.md` la capa específica de Claude Code

Se implementará con importación, no con duplicación total.

## Decisión 4 — Las instrucciones críticas serán de alta señal

No se llenarán los archivos persistentes con:

- explicaciones académicas;
- documentación completa de librerías;
- texto redundante;
- reglas que solo aplican a una tarea.

La documentación persistente tendrá solo aquello que debe recordarse en múltiples sesiones.

## Decisión 5 — Las garantías críticas no dependerán de prompts

Cuando una regla pueda convertirse en una comprobación determinista, se evaluará la posibilidad de utilizar permisos, validadores, hooks o CI en lugar de una instrucción verbal.

## Decisión 6 — Cada unidad importante tendrá criterio de éxito verificable

Ejemplo conceptual:

```text
Objetivo:
Añadir X.

Éxito:
- test A pasa;
- test B pasa;
- lint pasa;
- no cambia Y;
- diff limitado a Z.
```

## Decisión 7 — No habrá un “megaprompt maestro” para todo el proyecto

Se usarán instrucciones persistentes para contexto estable y prompts cortos por tarea para el objetivo concreto.

## Decisión 8 — Explore y Plan se usarán selectivamente

Para tareas grandes:

```text
Explore → Plan → Gate humano → Execute → Verify
```

Para cambios obvios y pequeños, se podrá trabajar directamente.

## Decisión 9 — Se mantendrá reversibilidad

Se utilizarán Git, ramas y commits como puntos de control. Las operaciones destructivas requerirán especial cuidado.

## Decisión 10 — Ejemplo 2 se usará como benchmark cualitativo

La pregunta será:

> “¿Qué prácticas de documentación, arquitectura, testing, trazabilidad, seguridad y despliegue vale la pena mejorar o reutilizar?”

No será:

> “¿Cómo copiamos este repositorio?”

---

# 7. Arquitectura inicial prevista para el contexto del proyecto

La estructura base, a refinar durante el Paso 1 y siguientes, es:

```text
Proyecto_Final_Master_AI4Devs/
├── AGENTS.md
├── CLAUDE.md
├── .claude/
│   ├── settings.json
│   ├── agents/
│   ├── skills/
│   └── rules/
├── backend/
├── frontend/
├── tests/
├── docs/
└── scripts/
```

Esta es una **estructura de trabajo prevista**, no una afirmación de que ya exista en el repositorio objetivo.

Los archivos por ámbito solo aparecerán cuando sus reglas sean reales y específicas. La documentación actual de Claude Code aconseja mantener instrucciones principales concisas y trasladar reglas específicas a mecanismos con alcance apropiado. citeturn176439view0turn662484view1

---

# 8. Regla de trabajo para `CLAUDE.md` y `AGENTS.md`

## `AGENTS.md`

Será la fuente común del proyecto para:

- visión del sistema;
- arquitectura aprobada;
- comandos esenciales;
- convenciones compartidas;
- testing;
- seguridad;
- workflow Git;
- restricciones estables;
- “gotchas”;
- definición mínima de calidad.

## `CLAUDE.md`

Inicialmente contendrá:

```md
@AGENTS.md
```

y añadirá únicamente comportamiento específico de Claude Code que no tenga sentido poner en la capa portable.

## Archivos por ámbito

La creación dependerá del contenido real del proyecto. Una posibilidad futura es:

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

Pero **no se crearán todos automáticamente**. Primero debe existir una necesidad específica.

---

# 9. Máximo total de pasos para completar el Módulo 1

Se establece un máximo de:

# 18 pasos

Este número coincide con el plan `Prompts/Plan_M1_Proyecto_Full_Stack_AI4Devs.md` ya presente en el repositorio. fileciteturn31file0L2-L6

El número es un **máximo**, no una obligación de fabricar 18 actividades si alguna puede resolverse en una sola unidad verificable.

No obstante, ningún requisito o comprobación se omitirá solo para reducir el número de pasos.

---

# 10. Flujo secuencial completo de los 18 pasos

## Paso 1 — Preparación local y clone verificable

### Propósito
Preparar el PC del usuario y obtener una copia local verificable de `Diiegoal/CursoIA` sin modificar el repositorio fuente.

### Alcance
- Git.
- GitHub CLI.
- Claude Code.
- clone.
- remote.
- branch.
- commit.
- estado inicial.

### Comprobaciones previstas

```bash
git --version
gh --version
claude --version
mkdir -p ~/proyectos
cd ~/proyectos
git clone https://github.com/Diiegoal/CursoIA.git
cd CursoIA
git remote -v
git branch --show-current
git status --short
git rev-parse HEAD
```

Después se comprobará que existe:

```text
Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/
```

**No se modificará todavía el repositorio fuente.**

### Gate
PASAR solo con evidencia de clone, remoto, branch, commit y directorio correctos.

---

## Paso 2 — Auditoría del entorno local

### Propósito
Determinar qué está disponible realmente antes de instalar o modificar nada.

### Comprobaciones

- sistema operativo;
- shell;
- Git;
- GitHub CLI;
- Claude Code;
- Node/npm cuando aplique al tooling;
- Docker cuando aplique;
- autenticación disponible;
- acceso al repositorio.

### Resultado esperado
Una tabla:

| Elemento | Estado | Versión | Acción |
|---|---|---:|---|
| Git | disponible/no | ... | ... |
| GitHub CLI | disponible/no | ... | ... |
| Claude Code | disponible/no | ... | ... |
| Node | disponible/no | ... | ... |
| Docker | disponible/no | ... | ... |

### Gate
No instalar nada innecesario antes de conocer el estado real.

---

## Paso 3 — Fuente de verdad estructurada del Módulo 1

### Propósito
Convertir el contenido del Módulo 1 en una matriz de trabajo que distinga:

- principio;
- práctica;
- herramienta;
- configuración;
- antipatrón;
- comprobación;
- recurso externo;
- afirmación que requiere verificación.

### Resultado
Un artefacto local de trabajo, pequeño y auditable, que permitirá comprobar al final que nada relevante del módulo quedó fuera.

---

## Paso 4 — Contrato operativo del proyecto

### Propósito
Transformar el contenido del Módulo 1 en reglas concretas para nuestro modo de trabajar.

### Debe responder

- ¿Qué puede hacer Claude Code?
- ¿Qué debe investigar antes de actuar?
- ¿Cuándo debe usar plan mode?
- ¿Cuándo debe pedir aclaración?
- ¿Cuándo debe detenerse?
- ¿Qué pruebas debe ejecutar?
- ¿Qué evidencia debe devolver?
- ¿Qué acciones están restringidas?

---

## Paso 5 — Decisión formal del harness principal

### Propósito
Aplicar Pilar 1 conscientemente.

### Resultado
Una decisión documentada de por qué Claude Code es el agente principal y qué categorías de tarea usarán:

- directo;
- agentic;
- plan mode;
- subagent.

No se decidirá por “me gusta más”, sino por las propiedades de la tarea.

---

## Paso 6 — Diseño inicial del harness

### Propósito
Configurar el entorno donde Claude Code trabajará:

- settings;
- permisos;
- memoria;
- reglas;
- hooks que realmente aporten valor;
- skills si ya existe un patrón repetible;
- subagentes que tengan una función clara.

### Regla
No se instalarán piezas por moda. Cada pieza debe tener un problema que resuelve.

---

## Paso 7 — Crear y validar `AGENTS.md`

### Propósito
Crear la fuente portable de verdad para agentes.

### Contenido inicial

- visión;
- objetivos;
- comandos;
- layout;
- convenciones;
- testing;
- seguridad;
- Git;
- gotchas;
- reglas de trabajo del agente.

### Validación

- tamaño razonable;
- no duplicar documentación;
- no contener datos secretos;
- reglas verificables;
- ausencia de contradicciones.

---

## Paso 8 — Crear y validar `CLAUDE.md`

### Propósito
Integrar la capa específica de Claude Code.

### Primera forma prevista

```md
@AGENTS.md
```

### Validación
Desde una sesión real de Claude Code se verificará que aparece como memoria cargada mediante `/context`, de acuerdo con la documentación oficial. citeturn176439view0L120-L124

---

## Paso 9 — Reglas por ámbito

### Propósito
Añadir contexto específico solo donde sea necesario.

### Posibles ámbitos

- backend;
- frontend;
- tests;
- docs;
- scripts;
- infraestructura.

### Criterio
Un archivo adicional solo se justifica si contiene reglas específicas de ese ámbito que serían ruido en la raíz.

Esto es coherente con el mecanismo actual de reglas por rutas y archivos `CLAUDE.md` anidados. citeturn176439view0L203-L244

---

## Paso 10 — Política de Context Engineering

### Propósito
Formalizar las cuatro operaciones del módulo:

```text
WRITE
SELECT
COMPRESS
ISOLATE
```

### Reglas prácticas

- no pegar el repositorio completo porque “cabe”;
- usar referencias a archivos;
- usar búsqueda dirigida;
- delegar investigación pesada a subagentes;
- persistir decisiones importantes fuera del chat;
- iniciar sesión nueva cuando arrastrar contexto sea peor que recargarlo.

La heurística 50/70/90 seguirá documentada como heurística del curso, no como especificación oficial del producto.

---

## Paso 11 — Arquitectura de subagentes

### Propósito
Definir cuándo un subagente aporta valor real.

### Candidatos

- exploración de codebase;
- research técnico;
- revisión independiente;
- testing;
- seguridad;
- documentación.

### Cada subagente deberá tener

- propósito;
- descripción clara;
- herramientas mínimas;
- permisos adecuados;
- formato de salida;
- criterio de finalización.

La documentación actual de Claude Code respalda el uso de subagentes para aislar contexto y especializar tareas. citeturn662484view1L121-L132

---

## Paso 12 — Contrato de prompting

### Propósito
Crear un patrón reusable para tareas importantes.

### Plantilla conceptual

```text
<contexto>
  solo información necesaria
</contexto>

<objetivo>
  outcome concreto
</objetivo>

<éxito>
  criterios observables
</éxito>

<restricciones>
  límites y no-gos
</restricciones>

<referencias>
  archivos y fuentes
</referencias>

<formato>
  salida esperada
</formato>

<aclaración>
  detenerse si existe ambigüedad crítica
</aclaración>
```

El módulo insiste en outcome + criterios de éxito + restricciones y la documentación actual de Anthropic recomienda prompts claros, directos, con contexto relevante, criterios específicos y uso de herramientas cuando corresponda. fileciteturn23file0L2-L6 citeturn847371search0

---

## Paso 13 — Workflow operativo de sesión

### Propósito
Integrar los tres pilares.

### Flujo base

```text
Caracterizar tarea
       ↓
Elegir modo/herramienta
       ↓
Curar contexto
       ↓
Prompt
       ↓
Ejecutar
       ↓
Verificar
       ↓
Registrar
```

### Para cambios complejos

```text
Explore
  ↓
Plan
  ↓
Gate humano
  ↓
Execute
  ↓
Verify
```

Este flujo está alineado tanto con el Módulo 1 como con las mejores prácticas actuales de Claude Code. citeturn662484view0L88-L139

---

## Paso 14 — Git y reversibilidad

### Propósito
Hacer auditable el trabajo del agente.

### Se definirá

- estrategia de ramas;
- naming;
- cuándo hacer commits;
- checkpoints;
- rollback;
- revisión de diffs;
- prohibición de acciones destructivas no autorizadas.

La referencia de OpenAI sobre harness engineering y las prácticas del Módulo 1 refuerzan la idea de que el agente debe trabajar sobre un entorno legible y controlable, no sobre un espacio sin límites. citeturn453435search6

---

## Paso 15 — Seguridad inicial del agente

### Propósito
No esperar al Módulo 6 para aplicar higiene básica.

### Se revisará

- `.env`;
- credenciales;
- tokens;
- directorios sensibles;
- permisos de herramientas;
- hooks;
- acciones destructivas.

Las garantías críticas se tratarán mediante mecanismos apropiados —permisos, hooks, CI— en lugar de depender solo de una frase en el prompt. Claude Code documenta explícitamente esta diferencia entre memoria de instrucciones y mecanismos deterministas de control. citeturn176439view0L70-L80

---

## Paso 16 — Primer ejercicio controlado con Claude Code

### Propósito
Validar el sistema completo con una tarea real pequeña y reversible.

### Debe demostrar

- Claude carga `CLAUDE.md`;
- `AGENTS.md` se incorpora;
- el agente entiende el contexto;
- usa la herramienta adecuada;
- no invade otras carpetas;
- cumple el prompt;
- ejecuta verificaciones;
- devuelve evidencia.

### Restricción
No será todavía una gran funcionalidad del producto. El objetivo de este paso es validar el **sistema de trabajo**, no avanzar artificialmente el producto.

---

## Paso 17 — Auditoría completa del Módulo 1

### Propósito
Comparar el estado real contra todo el contenido relevante del módulo.

### Checklist

- [ ] Pilar 1 comprendido y aplicado.
- [ ] Pilar 2 comprendido y aplicado.
- [ ] Pilar 3 comprendido y aplicado.
- [ ] AGENTS.md validado.
- [ ] CLAUDE.md validado.
- [ ] reglas por ámbito justificadas.
- [ ] política de contexto aplicada.
- [ ] subagentes definidos.
- [ ] workflow Explore/Plan/Execute establecido.
- [ ] verificación basada en evidencia.
- [ ] Git/reversibilidad establecida.
- [ ] seguridad inicial aplicada.
- [ ] ejercicio práctico validado.
- [ ] recursos relevantes contrastados.

---

## Paso 18 — Gate formal de salida del Módulo 1

El módulo solo se marcará como completado si:

```text
[✓] Preparación local verificada
[✓] Herramienta principal definida
[✓] Harness inicial configurado
[✓] AGENTS.md validado
[✓] CLAUDE.md validado
[✓] Alcances por directorio justificados
[✓] Context engineering operativo
[✓] Subagentes definidos donde aportan valor
[✓] Contrato de prompting definido
[✓] Explore → Plan → Execute → Verify operativo
[✓] Git y reversibilidad verificados
[✓] Seguridad inicial aplicada
[✓] Ejercicio práctico completado
[✓] Evidencia de resultados conservada
[✓] Auditoría del Módulo 1 superada
```

Solo después de este gate podrá iniciarse el **Módulo 3** que el usuario proporcionará posteriormente.

**No se avanzará al Módulo 3 antes de completar y verificar los 18 pasos del Módulo 1.**

---

# 11. Estructura exacta de cada paso futuro

Para mantener la consistencia solicitada, cada paso se presentará con esta estructura fija:

## A. Objetivo

Qué se debe conseguir.

## B. Fundamento

Qué concepto del Módulo 1 se está aplicando.

## C. Evidencia de la fuente

Qué dice el repositorio y qué fuente externa lo respalda cuando corresponda.

## D. Acción

Qué se hará realmente en el PC/proyecto.

## E. Resultado esperado

Qué debe quedar visible al terminar.

## F. Comprobaciones

Comandos, inspecciones o pruebas objetivas.

## G. Hallazgos

Qué ocurrió realmente.

## H. Correcciones

Qué se cambió para resolver problemas encontrados.

## I. Checklist

Criterios de aceptación del paso.

## J. Gate

Uno de:

- `PASA`
- `PASA CON OBSERVACIONES`
- `NO PASA`

No se abrirá el siguiente paso con un fallo crítico sin resolver.

---

# 12. Qué no se hará todavía

Antes de autorizar el Paso 1 no se hará ninguna de estas actividades:

- definir funcionalidades concretas del producto;
- diseñar la arquitectura funcional final;
- crear una base de datos del producto;
- implementar backend;
- implementar frontend;
- crear OpenSpec/SDD;
- comenzar el Módulo 3;
- copiar código del Ejemplo 2;
- crear falsos tests de “éxito”.

La razón es metodológica: el usuario ha pedido completar primero el Módulo 1 y aplicar sus principios de herramienta, contexto y prompting antes de seguir con las siguientes capas del proceso.

---

# 13. Respuesta específica a la preparación del proyecto

## ¿Podemos hacer `git clone` en tu PC desde aquí?

No. Este entorno no tiene acceso directo a tu PC. Sí se accedió al repositorio mediante GitHub y se intentó un clone en el entorno aislado, pero falló por resolución de red. El comando de clone real queda preparado para el Paso 1.

## ¿El repositorio nuevo ya existe?

No. `DiiegoA/Proyecto_Final_Master_AI4Devs` devuelve `404 Not Found` en la consulta actual. No se afirmará lo contrario hasta verificarlo.

## ¿Vamos a utilizar Claude Code como herramienta principal?

Sí. Es una decisión del proyecto basada en el tipo de flujo solicitado: desarrollo agentic, tareas multiarchivo, shell, planificación, verificación y trabajo sobre Git.

## ¿Vamos a crear `AGENTS.md` y `CLAUDE.md`?

Sí, pero siguiendo la arquitectura correcta: `AGENTS.md` como contexto portable y `CLAUDE.md` importándolo, con contenido específico de Claude Code solo donde realmente sea necesario. Esto está respaldado directamente por la documentación actual de Claude Code. citeturn176439view0L161-L180

## ¿Crearemos muchos `CLAUDE.md` y `AGENTS.md` en todas las carpetas?

No por defecto. Solo se crearán donde exista una necesidad específica de alcance. Esto reduce contexto redundante y contradicciones.

## ¿El Módulo 1 terminará antes del Módulo 3?

Sí. El gate de salida del Paso 18 es obligatorio.

---

# 14. Fuentes principales consultadas

## Repositorio del curso

- `https://github.com/Diiegoal/CursoIA`
- Módulo 1 y sus cinco documentos. fileciteturn1file0L2-L2
- `Prompts/Plan_M1_Proyecto_Full_Stack_AI4Devs.md`. fileciteturn28file0L2-L6
- `Proyecto_Final_Master_AI4Devs/Ejemplo_Proyectos_Finales_Reales.md`. fileciteturn2file0L2-L10

## Claude Code — fuentes oficiales

- Memory / `CLAUDE.md`: `https://code.claude.com/docs/en/memory` citeturn176439view0
- Best practices: `https://code.claude.com/docs/en/best-practices` citeturn662484view0
- Subagents: `https://code.claude.com/docs/en/sub-agents` citeturn662484view1
- Hooks: `https://code.claude.com/docs/en/hooks` citeturn662484view2
- Prompting: documentación oficial de Anthropic, `https://docs.anthropic.com/` citeturn847371search0

## AGENTS.md

- `https://agents.md/` citeturn886043search1
- GitHub custom instructions: `https://docs.github.com/en/copilot/reference/custom-instructions-support` citeturn973857search0

## Harness y contexto

- OpenAI Harness Engineering: `https://openai.com/index/harness-engineering/` citeturn453435search6
- Chroma Context Rot: `https://www.trychroma.com/research/context-rot` citeturn453435search2
- Simon Willison Context Engineering: `https://simonwillison.net/2025/jun/27/context-engineering/` citeturn453435search3
- Martin Fowler / Birgitta Böckeler Harness Engineering: `https://martinfowler.com/articles/exploring-gen-ai/harness-engineering-memo.html` citeturn453435search5

## Productividad

- METR update 2026: `https://metr.org/blog/2026-02-24-uplift-update/` citeturn453435search0

---

# 15. Estado de cierre de esta fase

```text
Repositorio fuente localizado:                 ✓
Árbol del repositorio inspeccionado:            ✓
Módulo 1 localizado:                            ✓
Cinco archivos del Módulo 1 revisados:          ✓
Recursos adicionales revisados:                ✓
Material transversal de Plan_M1 revisado:      ✓
Ejemplo 2 inspeccionado:                        ✓
Fuentes primarias actuales contrastadas:       ✓
Limitaciones operativas documentadas:          ✓
Repositorio objetivo comprobado:               ✓ no existe actualmente
Máximo de pasos definido:                      ✓ 18
Paso 1 ejecutado:                              NO
Proyecto funcional iniciado:                   NO
Módulo 1 completado:                           NO
Módulo 3 iniciado:                             NO
```

---

# 16. Decisión requerida

## Siguiente paso: Paso 1 — Preparación local y clone verificable

El siguiente turno debe trabajar **exclusivamente** en:

1. comprobar las herramientas locales;
2. realizar el `git clone` real de `Diiegoal/CursoIA` en el PC;
3. verificar remoto, branch, commit y estado inicial;
4. comprobar la presencia del Módulo 1;
5. detenerse y reportar evidencia antes de continuar.

No se diseñará todavía una funcionalidad del producto y no se avanzará al Módulo 3.

**¿Deseas comenzar con el Paso 1?**
