## Usuario

Primero olvida todo lo que tengas en memoria, no quiero contamicacion en esta investigacion, segundo Investiga exhaustivamente y busca profundamente en fuentes cofiables sin inventar datos sobre cual es el orden para crear una app full stack profesional, empiezo primero por planeacion o por documentacion o por ssd, osea por cual empiezo?, https://github.com/Diiegoal/CursoIA.git, entra mi repo, lee todo el contenido sin omitir nada, si me entiendes?

---

## ChatGPT

Sí, entendí. **Eliminé la memoria persistente disponible sobre ti** para que esta investigación no dependa de proyectos, preferencias o conversaciones anteriores.

También audité la rama `main` de `Diiegoal/CursoIA`: reconstruí su estructura vigente y abrí los **41 archivos Markdown actuales**, distribuidos en siete módulos. No consideré como contenido vigente los antiguos `.docx`, las carpetas temporales de prompts ni `.claude/settings.local.json`, porque fueron eliminados del repositorio. En algunos archivos muy extensos, GitHub devolvió el contenido en una única línea que la interfaz truncó; por eso no voy a afirmar que comprobé literalmente cada carácter de esos archivos, pero sí revisé todas las secciones, flujos, ejercicios y conclusiones relacionadas con planificación, SDD, documentación, seguridad y testing.

# Respuesta directa

## Para crear una app full stack profesional, empieza por la planificación del producto

Pero debes **documentar esa planificación desde el primer momento**.

Después de entender el problema, el usuario, el alcance y el valor del producto, aplicas **SDD para especificar el primer incremento pequeño de la aplicación antes de programarlo**.

La secuencia correcta es:

```text
Descubrimiento del problema
        ↓
Planificación inicial del producto
        ↓
Documento breve del producto
        ↓
Backlog y primer corte vertical
        ↓
SDD de ese corte
        ↓
Diseño técnico
        ↓
Tests y tareas
        ↓
Implementación full stack
        ↓
Despliegue
        ↓
Medición y aprendizaje
        ↓
Siguiente corte
```

En una sola frase:

> **Empieza planeando qué problema resolverás y para quién; documenta esas decisiones; después usa SDD para definir exactamente el primer comportamiento que vas a implementar.**

No debes empezar creando toda la documentación, ni instalando OpenSpec, ni diseñando la base de datos, ni programando el backend.

---

# La confusión principal: planificación, documentación y SDD no son fases equivalentes

| Concepto | Pregunta principal | Momento |
|---|---|---|
| **Planificación de producto** | ¿Por qué, para quién y qué debemos construir? | Primero |
| **Documentación** | ¿Dónde quedan registradas las decisiones y el conocimiento? | Desde el primer día y durante todo el proyecto |
| **SDD** | ¿Cuál es exactamente el comportamiento que debe implementar este cambio? | Después de entender y priorizar una necesidad |
| **Diseño técnico** | ¿Cómo lo construiremos? | Después de la especificación funcional y antes del código |
| **Testing** | ¿Cómo demostramos que funciona correctamente? | Antes y durante la implementación |

Por eso, preguntar “¿planificación, documentación o SDD?” plantea una falsa elección.

- La **planificación** decide qué vale la pena construir.
- La **documentación** conserva esa decisión.
- SDD convierte una parte suficientemente clara de la planificación en un contrato implementable.
- Los tests verifican que la implementación cumpla ese contrato.

El propio contenido de tu repositorio termina expresándolo mediante este flujo:

```text
PRD → User Story → OpenSpec change → Código
```

Además, distingue expresamente dos capas:

- El backlog responde **qué se entrega y por qué**.
- OpenSpec responde **cómo se concretará exactamente ese cambio para que un agente y el equipo puedan implementarlo**. fileciteturn38file0L1-L2

---

# Orden profesional completo para una app full stack

## 0. Descubrimiento y validación inicial

Antes de hablar de frameworks, microservicios o base de datos, responde:

- ¿Qué problema concreto existe?
- ¿Quién lo experimenta?
- ¿Cómo lo resuelve actualmente?
- ¿Qué resultado espera obtener?
- ¿Qué evidencia tienes de que el problema importa?
- ¿Por qué necesita una aplicación?
- ¿Qué hipótesis quieres comprobar?
- ¿Cuál es el mayor riesgo: producto, negocio, tecnología, seguridad o integración?

### Entregable mínimo

Un documento de una o dos páginas con:

```text
Problema
Usuario objetivo
Situación actual
Propuesta de valor
Hipótesis
Resultado esperado
Riesgos principales
Preguntas todavía abiertas
```

Para un producto incierto puede ser necesario hacer entrevistas, prototipos visuales o un spike técnico antes de escribir especificaciones detalladas.

Esto coincide con el propio módulo de SDD de tu repositorio: reconoce que SDD puede ser excesivo para prototipos exploratorios, scripts desechables, spikes cortos y cambios triviales. fileciteturn25file0L2-L2

---

## 1. Planificación inicial del producto

Una vez entendido el problema, crea un **Product Brief o PRD inicial**.

Debe contener como mínimo:

- Visión del producto.
- Problema que resuelve.
- Usuarios y roles.
- Jobs to be done o necesidades.
- Alcance del MVP.
- Funcionalidades fuera del MVP.
- Flujos principales.
- Requisitos no funcionales iniciales.
- Métricas de éxito.
- Riesgos y restricciones.
- Dependencias externas.
- Datos que procesará.
- Consideraciones legales, de privacidad y seguridad.

El ejercicio de FlowSync incluido en tu repositorio sigue justamente esta lógica: comienza con resumen ejecutivo, usuario objetivo, alcance del MVP, exclusiones, requisitos funcionales, requisitos no funcionales, stack como contexto, criterios de éxito y riesgos conocidos. fileciteturn43file0L1-L2

### No debes definir todavía

- Cada clase.
- Todas las tablas.
- Todos los endpoints.
- Toda la arquitectura.
- Todas las tareas.
- Toda la documentación técnica.

El PRD define principalmente **qué problema, qué producto, para quién y con qué alcance**.

---

## 2. Restricciones transversales y “constitución” de ingeniería

Antes de generar cientos de historias o código, define unas pocas reglas no negociables:

- Requisitos mínimos de seguridad.
- Privacidad y clasificación de datos.
- Accesibilidad.
- Compatibilidad soportada.
- Convenciones del repositorio.
- Estrategia de testing.
- Definition of Done.
- Política de dependencias.
- Gestión de secretos.
- Revisión de código.
- Observabilidad.
- Condiciones para desplegar.
- Restricciones de stack, cuando realmente existan.

Esto puede materializarse en:

```text
docs/product/
docs/architecture/
docs/decisions/
AGENTS.md o CLAUDE.md
CONTRIBUTING.md
Documento de Definition of Done
Constitution de Spec Kit, si se usa esa herramienta
```

La seguridad y la privacidad no pueden añadirse al final. NIST SSDF recomienda integrar las prácticas de desarrollo seguro dentro de cualquier implementación del ciclo de vida, y OWASP plantea seguridad por diseño desde la planificación, el diseño, la implementación, la verificación y la operación. citeturn896408search20turn987862search12turn987862search18

Tu módulo 6 también habla explícitamente de privacidad por diseño, seguridad desde las etapas iniciales y shift-left security. fileciteturn50file0L1-L2 fileciteturn52file0L1-L2

---

## 3. Backlog inicial y priorización

Descompón el PRD en:

```text
Objetivo de producto
  └── Épicas o capacidades
       └── Historias de usuario
            └── Criterios de aceptación
```

Las historias deben:

- Aportar valor observable.
- Ser suficientemente pequeñas.
- Tener criterios de aceptación verificables.
- Incluir restricciones y non-goals.
- Identificar dependencias.
- Señalar los supuestos todavía no comprobados.

No necesitas detallar todo el proyecto con el mismo nivel de precisión. Planifica en profundidad solamente lo próximo y mantén el resto a nivel de épicas o capacidades.

El enfoque iterativo coincide con ISO/IEC/IEEE 12207:2026: los procesos del ciclo de vida pueden ejecutarse de manera concurrente, iterativa, recursiva e incremental; el estándar no impone un único modelo lineal. citeturn896408search0turn120318view2

---

## 4. Escoge el primer corte vertical

No empieces construyendo:

```text
Toda la base de datos
→ todo el backend
→ toda la API
→ todo el frontend
→ todos los tests
```

Escoge una capacidad pequeña que atraviese el sistema completo.

Por ejemplo, para una aplicación de tareas:

```text
El usuario crea una tarea
        ↓
Formulario frontend
        ↓
Validación
        ↓
Endpoint backend
        ↓
Regla de negocio
        ↓
Persistencia
        ↓
Respuesta
        ↓
Actualización visual
        ↓
Tests
        ↓
Telemetría
```

Ese corte permite verificar pronto:

- Arquitectura.
- Integración frontend-backend.
- Migraciones.
- Autenticación.
- CI/CD.
- Manejo de errores.
- Testing.
- Despliegue.
- Observabilidad.

Después amplías el producto con nuevos cortes verticales.

---

## 5. Ahora sí: aplica SDD al primer corte

Aquí comienza formalmente SDD.

La especificación debe capturar:

- Por qué existe el cambio.
- Qué comportamiento se espera.
- Actores.
- Entradas y salidas.
- Escenarios normales.
- Casos límite.
- Errores.
- Reglas de negocio.
- Restricciones.
- Requisitos no funcionales relevantes.
- Non-goals.
- Criterios de aceptación.
- Preguntas abiertas.

En tu repositorio, OpenSpec separa los artefactos así:

```text
proposal.md   → por qué y qué cambia
specs/        → comportamiento esperado
design.md     → decisiones técnicas
tasks.md      → trabajo de implementación
```

Esta separación es correcta porque impide que la IA mezcle el problema, el comportamiento y la solución técnica en un único megaprompt. fileciteturn27file0L2-L2

### SDD no reemplaza la planificación

Tu propio módulo 2 afirma que SDD reinterpreta y fortalece el SDLC, pero no lo reemplaza. La especificación funciona como contrato entre intención e implementación. fileciteturn25file0L2-L2

### SDD tampoco es solo documentación

Una documentación tradicional puede explicar algo de manera narrativa.

Una buena especificación SDD debe ser suficientemente precisa para:

- Derivar tests.
- Identificar ambigüedades.
- Crear tareas.
- Revisar el código contra un contrato.
- Verificar cuándo el cambio está terminado.

---

## 6. Diseño técnico y arquitectura

Después de tener claro el comportamiento, diseña cómo se implementará.

Define solamente lo necesario para el incremento actual y las decisiones estructurales difíciles de revertir:

- Límites frontend/backend.
- Componentes principales.
- Modelo de dominio.
- Esquema de datos y migraciones.
- Contratos API.
- Autenticación y autorización.
- Integraciones.
- Manejo de errores.
- Caché, colas o eventos, si están justificados.
- Estrategia de despliegue.
- Observabilidad.
- Amenazas y controles.
- Rollback.
- ADR para decisiones relevantes.

### Regla importante

No elijas una arquitectura compleja porque “se ve profesional”.

Una aplicación profesional no es la que usa más tecnologías; es la que:

- Satisface los requisitos.
- Reduce riesgos.
- Puede mantenerse.
- Puede probarse.
- Puede desplegarse.
- Puede observarse.
- Permite evolucionar.

La documentación arquitectónica debe registrar especialmente el **porqué** de las decisiones, mediante ADR y diagramas versionados cuando aporten valor. Esto coincide con el módulo 5. fileciteturn45file0L1-L2

---

## 7. Plan de tareas y estrategia de pruebas

Convierte la especificación y el diseño en tareas pequeñas y verificables.

Un orden habitual para cada corte sería:

```text
1. Tests de aceptación o contrato
2. Migración y modelo de datos
3. Reglas de dominio
4. Repositorio/persistencia
5. Servicio o caso de uso
6. Endpoint y validación
7. Cliente frontend
8. Estado y UI
9. Manejo de errores
10. Integración y E2E
11. Documentación
12. Observabilidad
13. Despliegue
```

Las tareas no deben sustituir la especificación. La spec explica el contrato; las tareas explican el trabajo necesario para cumplirlo.

---

## 8. Preparación de la base de ingeniería

Antes de acelerar la implementación, establece una base mínima:

- Repositorio y estrategia de ramas.
- Entorno local reproducible.
- Variables de entorno y `.env.example`.
- Gestión de secretos.
- Linter y formatter.
- Type checking.
- Migraciones.
- Unit tests.
- Integration tests.
- Contract tests.
- E2E para flujos críticos.
- CI.
- Escaneo de dependencias.
- Escaneo de secretos.
- SAST cuando corresponda.
- Build reproducible.
- Entorno de staging.
- Pipeline de despliegue.
- Logs, métricas y manejo de errores.

No necesitas una plataforma DevOps gigantesca antes de la primera línea funcional, pero sí debes evitar que el proyecto crezca sin controles básicos.

---

## 9. Implementación mediante TDD/BDD y cortes pequeños

El orden de cada comportamiento debería ser:

```text
Spec o criterio de aceptación
        ↓
Test que demuestra el comportamiento
        ↓
Verificar que falla
        ↓
Implementación mínima
        ↓
Verificar que pasa
        ↓
Refactor
        ↓
Pruebas de integración
        ↓
Revisión
```

El módulo 7 de tu repositorio también comienza por historia de usuario y criterios de aceptación antes de traducir cada criterio en pruebas y luego en implementación. fileciteturn56file0L1-L2

Además, relaciona correctamente:

```text
SDD → define el contrato de la capacidad
BDD → expresa escenarios observables
TDD → conduce la implementación mediante tests
```

No son metodologías competidoras.

---

## 10. Quality gates y documentación viva

Antes de considerar terminado un cambio, verifica:

- Criterios de aceptación.
- Tests.
- Seguridad.
- Autorización.
- Validaciones.
- Accesibilidad.
- Rendimiento relevante.
- Manejo de errores.
- Logs y métricas.
- Migraciones.
- Compatibilidad.
- Documentación API.
- ADR, si hubo una decisión arquitectónica.
- Runbook, cuando afecte operaciones.
- Rollback.

La documentación no debe escribirse toda al principio ni toda al final.

Debe evolucionar así:

```text
Descubrimiento  → brief/PRD
Planificación   → backlog y criterios
SDD             → specs
Diseño          → ADR y diagramas
Implementación  → API docs y documentación de código
Despliegue      → runbooks
Operación       → troubleshooting y postmortems
```

Tu módulo 5 define precisamente la documentación viva como aquella que:

- Vive en el repositorio.
- Se actualiza con el cambio.
- Pasa por revisión.
- Tiene validación automatizada. fileciteturn44file0L1-L2

También propone probar Markdown, enlaces, prosa y cobertura documental desde CI. fileciteturn47file0L1-L2

---

## 11. Despliegue, operación y aprendizaje

Una app profesional no termina al hacer merge.

El ciclo continúa con:

- Staging.
- Migraciones controladas.
- Feature flags o despliegue gradual.
- Backups.
- Rollback.
- Monitoreo.
- Alertas.
- Logs estructurados.
- Métricas de negocio.
- Errores frontend/backend.
- Feedback de usuarios.
- Revisión de las hipótesis iniciales.
- Actualización de PRD, backlog, specs y documentación.

Después comienza el siguiente incremento:

```text
Medir → aprender → repriorizar → especificar → implementar
```

---

# Qué concluyo específicamente sobre el orden de tu repositorio

El orden pedagógico actual es aproximadamente:

```text
Módulo 1: fundamentos de copilotos
Módulo 2: SDD
Módulo 3: sistema operativo del copiloto
Módulo 4: planificación
Módulo 5: documentación
Módulo 6: ética, regulación, privacidad y seguridad
Módulo 7: testing
```

Ese orden puede servir para **enseñar progresivamente conceptos y herramientas**, pero **no debe copiarse literalmente como orden para ejecutar un proyecto nuevo**.

El propio módulo 4 demuestra que, en un proyecto real, la secuencia es:

```text
PRD
→ backlog
→ historias y criterios de aceptación
→ cambio OpenSpec
→ código
```

Por tanto, la planificación del módulo 4 ocurre conceptualmente antes del uso práctico de SDD del módulo 2. fileciteturn38file0L1-L2

## Orden recomendado para aplicar tus módulos al crear una app

```text
1. Módulo 1
   Modelo mental de herramienta, contexto y prompt

2. Módulo 4
   Descubrimiento, PRD, backlog, historias y priorización

3. Módulo 6, especialmente privacidad y seguridad por diseño
   Restricciones que deben afectar el producto y la arquitectura

4. Módulo 3
   Preparar correctamente el harness, contexto, skills y flujo
   Explore → Plan → Execute

5. Módulo 2
   Aplicar SDD a la primera historia priorizada

6. Módulo 7
   Derivar tests de la spec antes y durante la implementación

7. Módulo 5
   Profundizar la documentación viva, aunque sus artefactos
   básicos ya debieron empezar desde el primer paso
```

No significa que debes “terminar” un módulo y olvidar los anteriores. En un proyecto real se combinan continuamente.

---

# Corrección importante sobre OpenSpec

En tu repositorio aparece principalmente:

```text
propose → apply → archive
```

La documentación oficial actual de OpenSpec incorpora el flujo principal:

```text
explore, cuando todavía hay incertidumbre
        ↓
propose
        ↓
apply
        ↓
sync
        ↓
archive
```

Por tanto:

- `explore` sirve para investigar sin comprometer todavía una propuesta.
- `propose` formaliza el cambio.
- `apply` implementa.
- `sync` actualiza las especificaciones vivas.
- `archive` conserva el cambio terminado.

El cambio no modifica la conclusión metodológica, pero sí significa que parte del material de OpenSpec de tu repositorio debe actualizarse para coincidir con su versión vigente. citeturn410697search1turn410697search2turn410697search8

Para aplicaciones greenfield, GitHub Spec Kit también presenta una secuencia especialmente clara:

```text
Constitution
→ Specify
→ Clarify
→ Plan
→ Tasks
→ Analyze
→ Implement
```

Es decir, primero principios y especificación del resultado; después planificación técnica, tareas e implementación. citeturn410697search0turn410697search3turn410697search6

---

# Qué debes tener antes de empezar a programar

No necesitas un libro de 200 páginas. Necesitas que estas preguntas tengan respuestas suficientemente claras:

```text
[ ] ¿Quién es el usuario?
[ ] ¿Qué problema concreto resolveremos?
[ ] ¿Qué resultado medible buscamos?
[ ] ¿Qué incluye el MVP?
[ ] ¿Qué queda explícitamente fuera?
[ ] ¿Cuál es el primer corte vertical?
[ ] ¿Cuáles son sus criterios de aceptación?
[ ] ¿Qué datos procesa?
[ ] ¿Qué requisitos de seguridad y privacidad aplican?
[ ] ¿Qué requisitos no funcionales son obligatorios?
[ ] ¿Cómo demostraremos que funciona?
[ ] ¿Cómo lo desplegaremos y revertiremos?
[ ] ¿Cómo sabremos en producción si funciona o falla?
```

Cuando esas respuestas existen, pasas a SDD y diseño técnico.

# Veredicto final

**No empieces por SDD aislado.** Una especificación precisa de una idea equivocada solo permite construir más rápidamente el producto equivocado.

**No empieces escribiendo toda la documentación.** Documentar completamente un sistema que todavía no existe genera especulación y documentos obsoletos.

**Empieza por planificación y descubrimiento de producto, creando documentación mínima y viva.** Después prioriza un pequeño corte vertical, aplícale SDD, diseña lo estrictamente necesario, deriva tests, impleméntalo de extremo a extremo, despliega, mide y repite.

```text
PLANIFICAR EL PRODUCTO
        ↓
DOCUMENTAR LAS DECISIONES
        ↓
ESPECIFICAR EL PRIMER CAMBIO CON SDD
        ↓
DISEÑAR CÓMO SE CONSTRUIRÁ
        ↓
PROBAR E IMPLEMENTAR
        ↓
DESPLEGAR Y APRENDER
```

Ese es el orden más sólido para desarrollar una app full stack profesional sin convertir la planificación, SDD o la documentación en burocracia.

---

## Usuario

Quiero que hagamos un proyecto y crear un nuevo repo, primero ingresa a mi repo https://github.com/Diiegoal/CursoIA, empezando por Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA paso a paso, detalladamente, me guiaras en el proyecto explicando cada concepto desde sus fundamentos, sin omitir informacion, poniendo en practica todo el contenido para realizar el proyecto completo, me diras la cantidad de pasos totales y al terminar cada paso me preguntaras si deseo continuar con el siguiente paso, cada paso usara su maxima ventana de contexto, el proyecto sera real, profesional, full stack, sera un agente ia conversacional, con todo el ecosistema de Langchain, creadolo con Claude Code desde cero, quiero que ingreses la informacion maxima recomendable en cada md, ya sea CLAUDE/AGENTS.md, tambien al finalizar todos los pasos del Modulo 1, te paso despues el Módulo_4_Planificación_efectiva_con_IA, vamos en orden, tambien quiciera dividir el proyecto full stack, cada uno con su propio md y que cada uno tenga su maxima informacion sin superar sus limites, investiga exhaustivamente y busca en fuentes confiables sin inventar datos como hacer este modulo 1, con datos mas recientes hasta julio 2026, si me entiendes?.

---

## ChatGPT

Voy a convertir el **Módulo 1** en una ruta práctica aplicada a un repositorio nuevo, no en una explicación aislada. Primero revisaré el módulo completo y las reglas actuales de Claude Code, LangChain y estructura de contexto; después definiré el número total de pasos y comenzaremos únicamente con el **Paso 1**.

---

## ChatGPT

Ya confirmé dos cosas importantes: el repositorio es público y la conexión disponible aquí **solo tiene permiso de lectura**, no de escritura ni administración. Por eso puedo auditar el curso completamente, pero la creación del repositorio nuevo deberá hacerse mediante Claude Code/Git en tu equipo o mediante una conexión de GitHub con permisos adecuados; lo integraremos como parte del primer paso.

---

## ChatGPT

El historial confirma que el repositorio fue cargado mediante varios commits separados llamados “first commit”, no como una sola importación limpia. Estoy reconstruyendo el módulo desde los archivos reales y no desde el nombre de las carpetas, para evitar omitir ejercicios o tomar material eliminado como vigente.

---

## ChatGPT

Sí, te entendí. Vamos a construir **un proyecto real, profesional y full stack**, guiado paso a paso, utilizando **Claude Code** y el ecosistema actual de **LangChain**. No comenzaremos programando funcionalidades al azar: primero construiremos correctamente el entorno de trabajo del agente de programación.

He revisado los cuatro documentos vigentes del Módulo 1:

1. `1. El modelo mental de los 3 pilares.md`
2. `2. Pilar 1 — La Herramienta.md`
3. `3. Pilar 2 — El Contexto.md`
4. `4. Pilar 3 — El Prompt + Integración.md` fileciteturn8file0L10-L23

# Decisión metodológica importante

Durante el **Módulo 1 no desarrollaremos todavía las funcionalidades del producto**.

El Módulo 1 servirá para construir el sistema profesional con el que desarrollaremos el producto:

```text
Claude Code
    +
configuración segura
    +
contexto persistente
    +
documentación modular
    +
skills
    +
subagentes
    +
hooks
    +
MCP
    +
prompts verificables
    +
flujo Explore → Plan → Execute → Verify
```

Después, cuando pasemos al **Módulo 4 — Planificación efectiva con IA**, definiremos formalmente:

- Problema que resolverá el agente.
- Usuarios.
- Casos de uso.
- Alcance del MVP.
- Requisitos funcionales.
- Requisitos no funcionales.
- Arquitectura.
- Backlog.
- Historias.
- Criterios de aceptación.
- Primer corte vertical.

Esto evita cometer el error de crear primero una arquitectura o código para un producto que todavía no está suficientemente definido.

El propio Módulo 1 establece que el resultado de un copiloto depende de tres pilares co-iguales: herramienta, contexto y prompt. También defiende que el modelo aislado no explica el resultado; importa el *harness* que lo rodea. fileciteturn9file0L2-L2

---

# Correcciones necesarias al contenido del módulo

Aplicaremos el contenido, pero no copiaremos ciegamente todas sus afirmaciones.

## 1. Claude Code no carga `AGENTS.md` directamente

La documentación oficial actual indica:

> Claude Code lee `CLAUDE.md`, no `AGENTS.md`.

La solución profesional y portable será:

```md
# CLAUDE.md

@AGENTS.md
```

De esta manera:

- `AGENTS.md` será la fuente neutral para distintos agentes.
- `CLAUDE.md` será el punto de entrada específico de Claude Code.
- Debajo del import podremos agregar instrucciones exclusivas de Claude Code.

Anthropic recomienda precisamente importar `AGENTS.md` desde `CLAUDE.md` cuando se necesita compatibilidad con varios agentes. citeturn951361search0

## 2. “Máxima información” no significa crear un `CLAUDE.md` gigantesco

Tu intención de incluir la mayor cantidad recomendable de información es correcta, pero debemos colocar cada información en el lugar adecuado.

Anthropic recomienda mantener cada `CLAUDE.md` por debajo de unas **200 líneas como objetivo**, porque los archivos largos consumen contexto en todas las sesiones y pueden disminuir la adherencia a las instrucciones. También recomienda mover las reglas especializadas a `.claude/rules/`, skills o documentos cargados bajo demanda. citeturn951361search0

La estrategia será:

```text
Información imprescindible en todas las sesiones
→ AGENTS.md y CLAUDE.md

Reglas aplicables a una parte del repositorio
→ .claude/rules/*.md

Procedimientos repetibles
→ .claude/skills/<skill>/SKILL.md

Conocimiento profundo y documentación técnica
→ docs/**/*.md

Preferencias personales no compartidas
→ CLAUDE.local.md

Aprendizajes automáticos locales
→ Auto memory de Claude Code
```

Además, investigación publicada en 2026 encontró que los archivos de contexto con requisitos innecesarios pueden empeorar el éxito del agente y aumentar el consumo; otro estudio identifica como problemas frecuentes el *context bloat*, instrucciones conflictivas y procedimientos incrustados donde deberían existir skills. citeturn567680academia39turn567680academia37

## 3. Los porcentajes 50/70/90 del contexto no son límites universales

El Módulo 1 presenta:

```text
50% → comienza la degradación
70% → compactar
90% → reiniciar
```

Los trataremos como **heurísticas pedagógicas**, no como límites científicos aplicables de forma idéntica a todos los modelos y tareas.

Anthropic sí confirma que la calidad puede deteriorarse mientras la ventana se llena y recomienda administrar activamente el contexto, usar subagentes para investigación, compactar en puntos naturales y comenzar sesiones nuevas entre tareas grandes. Pero no publica una ley universal 50/70/90. citeturn777956search1turn704918search6

## 4. No instalaremos “todo LangChain” solo para afirmar que lo usamos

Utilizaremos el ecosistema actual de manera arquitectónicamente justificada:

```text
LangChain
→ framework de agentes, modelos, tools, middleware e integraciones

LangGraph
→ runtime de orquestación, estado, persistencia,
  durable execution, streaming y human-in-the-loop

Deep Agents
→ harness de planificación, filesystem, subagentes
  y administración de contexto cuando esté justificado

LangSmith
→ tracing, observabilidad, datasets, evaluaciones,
  monitoreo y potencial despliegue

Agent Chat UI / useStream
→ interfaz conversacional y streaming hacia el frontend
```

La documentación actual de LangChain distingue expresamente esos componentes: Deep Agents es un *harness*, LangChain es el framework, LangGraph es el runtime y LangSmith es la plataforma de observabilidad, evaluación y despliegue. citeturn615936search0turn615936search5turn615936search7

---

# Cantidad total de pasos del Módulo 1

El **Módulo 1 tendrá 16 pasos**.

No fijaré todavía una cantidad total falsa para todo el proyecto. El número de pasos del desarrollo completo dependerá del alcance, los requisitos y las historias que definamos posteriormente en el Módulo 4.

| Paso | Resultado |
|---:|---|
| 1 | Crear el repositorio nuevo y registrar la línea base del entorno |
| 2 | Auditar las afirmaciones del Módulo 1 y construir una matriz de evidencia |
| 3 | Comprender modelo, agente, harness, tool, contexto y prompt desde la raíz |
| 4 | Auditar Claude Code como herramienta agentic y seleccionar su modo de trabajo |
| 5 | Establecer el protocolo profesional Git/GitHub y control humano |
| 6 | Diseñar las capas de contexto del proyecto |
| 7 | Crear `AGENTS.md`, `CLAUDE.md` y `CLAUDE.local.md` correctamente |
| 8 | Separar documentación de frontend, backend, agente, datos, infraestructura y pruebas |
| 9 | Crear reglas modulares y posteriormente limitarlas por rutas |
| 10 | Crear skills reutilizables en `.claude/skills/` |
| 11 | Diseñar subagentes de exploración, arquitectura, testing, seguridad y revisión |
| 12 | Configurar permisos y hooks deterministas |
| 13 | Configurar MCP con mínimo privilegio y sin contaminar el contexto |
| 14 | Aplicar Write, Select, Compress e Isolate a las sesiones |
| 15 | Crear el sistema de prompts: objetivo, criterios, restricciones y verificación |
| 16 | Ejecutar una práctica integrada, auditar el harness y etiquetar el Módulo 1 |

Al finalizar el paso 16 tendremos un repositorio vacío de funcionalidades, pero no vacío de ingeniería: estará preparado profesionalmente para iniciar la planificación del producto.

---

# Paso 1 de 16 — Crear el repositorio y establecer la línea base

## Objetivo

Al finalizar este paso debes tener:

```text
Un repositorio privado nuevo en GitHub
        +
un clon local limpio
        +
GitHub CLI autenticado
        +
Claude Code operativo
        +
un inventario verificable del entorno
        +
ningún secreto comprometido
        +
ninguna arquitectura inventada prematuramente
```

## Por qué este es el primer paso

El repositorio será el límite del proyecto y también el límite de memoria de Claude Code.

Cada sesión de Claude Code comienza con una ventana nueva. El repositorio permite que el conocimiento importante sobreviva mediante:

- Archivos versionados.
- `CLAUDE.md`.
- Reglas.
- Skills.
- Decisiones.
- Documentación.
- Tests.
- Historial Git.
- Auto memory local de Claude Code.

Claude Code no es solamente un chat. Es un entorno agentic que puede leer archivos, ejecutar comandos, modificar código y verificar resultados; por eso el estado del repositorio y sus permisos forman parte del *harness*. citeturn777956search1

---

## Nombre del repositorio

Usaremos inicialmente:

```text
conversational-ai-agent-platform
```

Nombre completo:

```text
Diiegoal/conversational-ai-agent-platform
```

Verifiqué que actualmente no existe un repositorio accesible con ese nombre.

El nombre es provisionalmente neutral:

- `conversational`: será conversacional.
- `ai-agent`: no será solo un chatbot de respuestas.
- `platform`: tendrá frontend, backend, agente, datos, observabilidad e infraestructura.
- No vincula todavía el producto a una industria que no hemos definido.

## Visibilidad inicial

Recomiendo crearlo como **privado** durante el desarrollo.

Motivos:

- Todavía configuraremos secretos.
- El proyecto comenzará incompleto.
- Podremos realizar una auditoría de seguridad antes de publicarlo.
- Cambiarlo a público al finalizar es sencillo.
- Evitamos exponer por accidente `.env`, claves, trazas o documentación interna.

---

## Parte A — No abras Claude Code todavía

Primero abre una terminal normal y ejecuta estos comandos, uno por uno:

```bash
git --version
gh --version
gh auth status
claude --version
claude doctor
python --version
node --version
docker --version
docker compose version
```

### Qué verifica cada comando

#### `git --version`

Comprueba que Git está instalado.

Git administrará:

- Commits.
- Ramas.
- Tags.
- Historial.
- Reversiones.
- Comparación de cambios.
- Colaboración.
- Integración con GitHub.

#### `gh --version`

Comprueba que GitHub CLI está instalado.

No es lo mismo que Git:

```text
Git
→ controla versiones localmente

GitHub CLI
→ administra GitHub desde la terminal
```

#### `gh auth status`

Comprueba:

- Si estás autenticado.
- Con qué cuenta.
- En qué host.
- Qué protocolo Git utilizas.
- Si el token es válido.

No publiques la salida si accidentalmente muestra información sensible. Normalmente no imprime el token.

#### `claude --version`

Comprueba que el ejecutable de Claude Code existe y registra su versión actual.

#### `claude doctor`

Realiza un diagnóstico más profundo.

La documentación oficial recomienda `claude doctor` cuando Claude no puede iniciarse y `/doctor` desde una sesión activa para revisar instalación, configuración, MCP y uso de contexto. citeturn704918search1turn704918search4

#### `python --version`

Solo registra la versión actual.

Todavía no vamos a decidir si esa será la versión del proyecto.

En Windows, cuando el comando no existe, prueba:

```bash
py --version
```

#### `node --version`

Registra la versión actual de Node.js.

No instalaremos framework frontend todavía.

#### `docker --version`

Confirma si Docker está disponible.

#### `docker compose version`

Confirma que Compose está integrado.

No levantaremos contenedores en este paso.

---

## Parte B — Instalar Claude Code solamente si falta

La instalación nativa es actualmente el método recomendado por Anthropic y se actualiza automáticamente. citeturn704918search0turn704918search4

### Windows PowerShell

```powershell
irm https://claude.ai/install.ps1 | iex
```

### Windows CMD

```cmd
curl -fsSL https://claude.ai/install.cmd -o install.cmd && install.cmd && del install.cmd
```

### WSL, Linux o macOS

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

Después:

```bash
claude --version
claude doctor
```

En Windows nativo, Anthropic recomienda tener Git for Windows para que Claude Code pueda utilizar Bash; cuando no está disponible, Claude Code puede recurrir a PowerShell. WSL 2 permite además ciertas capacidades de sandboxing que Windows nativo no ofrece. citeturn704918search4

No instales simultáneamente Claude Code mediante npm, WinGet y el instalador nativo. Varias instalaciones pueden provocar versiones o rutas inconsistentes. La documentación oficial recomienda mantener una sola instalación. citeturn704918search5

---

## Parte C — Autenticar GitHub CLI

Cuando `gh auth status` indique que no estás autenticado, ejecuta:

```bash
gh auth login
```

Selecciona:

```text
What account do you want to log into?
→ GitHub.com

What is your preferred protocol for Git operations?
→ HTTPS

Authenticate Git with your GitHub credentials?
→ Yes

How would you like to authenticate GitHub CLI?
→ Login with a web browser
```

GitHub mostrará un código temporal.

Proceso:

```text
1. Copias el código.
2. Presionas Enter.
3. Se abre el navegador.
4. Pegas el código.
5. Autorizas GitHub CLI.
6. Regresas a la terminal.
```

Comprueba nuevamente:

```bash
gh auth status
```

---

## Parte D — Crear el repositorio nuevo

Ubícate en la carpeta donde guardas tus proyectos.

Después ejecuta este comando en una sola línea:

```bash
gh repo create Diiegoal/conversational-ai-agent-platform --private --description "Plataforma full stack profesional para un agente IA conversacional, construida con Claude Code y el ecosistema LangChain." --add-readme --clone
```

GitHub CLI permite crear un repositorio remoto, definir su visibilidad, agregar un README y clonarlo localmente mediante `gh repo create`. citeturn567680search0

### Explicación exacta

```text
gh repo create
```

Solicita crear un repositorio en GitHub.

```text
Diiegoal/conversational-ai-agent-platform
```

Define propietario y nombre.

```text
--private
```

Lo crea privado.

```text
--description "..."
```

Añade una descripción inicial.

```text
--add-readme
```

Inicializa el repositorio con un primer commit que contiene `README.md`.

Esto evita crear un repositorio remoto completamente vacío.

```text
--clone
```

Crea una copia local y configura automáticamente el remoto `origin`.

---

## Parte E — Entrar y verificar el repositorio

Ejecuta:

```bash
cd conversational-ai-agent-platform
```

Después:

```bash
git status
git branch --show-current
git remote -v
gh repo view
```

### Resultado esperado de `git status`

Debe parecerse a:

```text
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

### Resultado esperado de `git branch --show-current`

```text
main
```

Cuando muestre otro nombre, no lo cambies todavía. Primero necesito ver cuál es.

### Resultado esperado de `git remote -v`

Debe mostrar:

```text
origin  https://github.com/Diiegoal/conversational-ai-agent-platform.git (fetch)
origin  https://github.com/Diiegoal/conversational-ai-agent-platform.git (push)
```

### Resultado esperado de `gh repo view`

Debe identificar:

- Nombre.
- Descripción.
- Visibilidad privada.
- Rama principal.
- README.

---

## Parte F — Abrir Claude Code por primera vez en el repositorio

Solo después de verificar Git, ejecuta:

```bash
claude
```

Claude Code debe abrirse tomando como directorio de trabajo:

```text
conversational-ai-agent-platform/
```

Dentro de Claude Code ejecuta:

```text
/status
```

Luego:

```text
/doctor
```

Después:

```text
/context
```

### Qué buscamos

`/status`:

- Método de autenticación.
- Modelo activo.
- Cuenta.
- Directorio.
- Configuración básica.

`/doctor`:

- Problemas de instalación.
- Configuraciones inválidas.
- MCP problemáticos.
- Archivos de memoria sobredimensionados.
- Uso de contexto.

`/context`:

- Qué está ocupando la ventana.
- Instrucciones cargadas.
- Definiciones de herramientas.
- MCP.
- Conversación.

En este momento todavía no debería existir:

```text
CLAUDE.md
AGENTS.md
.claude/rules/
.claude/skills/
.claude/agents/
.mcp.json
```

Eso es intencional. Los crearemos conscientemente, no mediante un `/init` aceptado a ciegas.

Sal de Claude Code con:

```text
/exit
```

---

# Qué no debes hacer durante el Paso 1

No ejecutes todavía:

```text
/init
```

No pidas:

```text
Crea toda la aplicación
```

No crees todavía:

```text
frontend
backend
base de datos
RAG
LangGraph
Docker Compose
autenticación
AGENTS.md
CLAUDE.md
MCP
hooks
subagentes
```

No agregues:

```text
.env
API keys
credenciales
tokens
contraseñas
```

No instales:

```text
langchain
langgraph
deepagents
langsmith
fastapi
next
react
postgres
```

Todavía no sabemos qué versiones, componentes o arquitectura estarán justificadas.

---

# Criterios para considerar terminado el Paso 1

El paso está completo únicamente cuando puedas confirmar:

```text
[ ] Git funciona.
[ ] GitHub CLI funciona.
[ ] GitHub CLI está autenticado con la cuenta correcta.
[ ] Claude Code funciona.
[ ] claude doctor termina sin un error bloqueante.
[ ] El repositorio privado fue creado.
[ ] El repositorio fue clonado.
[ ] El remoto origin es correcto.
[ ] La rama actual fue identificada.
[ ] git status muestra un árbol limpio.
[ ] Claude Code fue abierto desde la raíz correcta.
[ ] /status fue revisado.
[ ] /doctor fue revisado.
[ ] /context fue revisado.
[ ] No se añadió ningún secreto.
[ ] No se generó código de la aplicación.
```

La conexión de GitHub disponible en esta conversación tiene permisos de lectura, pero no permisos de creación o administración. Por eso no puedo crear directamente el repositorio en tu cuenta desde aquí; el comando anterior lo crea usando tu autenticación local.

Cuando completes los comandos, pega la salida de las verificaciones —ocultando cualquier token o dato sensible—. **¿Deseas continuar con el Paso 2 de 16: auditar científicamente el Módulo 1 y construir la matriz “afirmación del curso vs evidencia verificada”?**

---

## Usuario

Absolutamente todo funciono, me seguiras guiando en el proyecto paso a paso, detalladamente, explicando cada concepto desde sus fundamentos, sin omitir informacion, poniendo en practica todo el contenido para realizar el proyecto completo, al terminar cada paso me preguntaras si deseo continuar con el siguiente paso, cada paso usara su maxima ventana de contexto, seguimos con el mismo proyecto real, profesional, full stack, el agente ia conversacional, creadolo con Claude Code, continuemos con el Paso 2 de 16: auditar científicamente el Módulo 1 y construir la matriz “afirmación del curso vs evidencia verificada, investiga exhaustivamente y busca en fuentes confiables sin inventar datos para hacer este paso 2, con datos mas recientes hasta julio 2026, si me entiendes?. 

---

## ChatGPT

Voy a auditar el módulo como si fuera una revisión académica y de ingeniería: separaré afirmaciones estables, datos verificables, afirmaciones parcialmente sustentadas, afirmaciones volátiles y afirmaciones no demostradas. Al final convertiremos esa auditoría en archivos versionados dentro del repositorio usando Claude Code, sin modificar todavía el producto.

---

## ChatGPT

Ya aparecen tres clases de resultado. Los datos de METR y el estudio sobre carga de mantenimiento sí existen, pero tienen límites metodológicos que el curso debe conservar. En cambio, varias cifras del curso —porcentajes universales de uso de contexto, comparativas de herramientas y precios— no son leyes científicas: son heurísticas o instantáneas comerciales que deben marcarse como volátiles, no convertirse en reglas permanentes del proyecto.

---

## ChatGPT

Te entendí. Continuamos con el mismo repositorio y el mismo proyecto:

```text
Diiegoal/conversational-ai-agent-platform
```

# Paso 2 de 16 — Auditoría científica del Módulo 1

En este paso **no vamos a desarrollar todavía frontend, backend, RAG ni agentes LangChain**. Vamos a construir una base de evidencia que impedirá que Claude Code trate afirmaciones pedagógicas, comparaciones comerciales o reglas heurísticas como verdades universales.

El resultado quedará versionado dentro del repositorio y será consultable más adelante, pero **no se cargará automáticamente en todas las sesiones**. Eso sería contrario al principio de contexto mínimo y relevante.

---

# 1. Qué significa “auditar científicamente”

Auditar científicamente no significa buscar una página que coincida con lo que afirma el curso.

Significa separar:

```text
Lo que afirma el curso
        ↓
Qué tipo de afirmación es
        ↓
Qué evidencia podría demostrarla
        ↓
Qué fuentes existen
        ↓
Qué limitaciones tienen
        ↓
Qué conclusión está realmente permitida
        ↓
Cómo afecta al proyecto
```

Una afirmación puede ser:

- Correcta y bien sustentada.
- Correcta, pero con alcance limitado.
- Parcialmente correcta.
- Una heurística profesional.
- Una opinión o taxonomía pedagógica.
- Volátil porque depende de precios, versiones o productos.
- Obsoleta.
- No sustentada.
- Contradicha por la documentación actual.

## Regla fundamental

> **No encontrar evidencia no demuestra automáticamente que una afirmación sea falsa.**

En ese caso, el estado correcto es:

```text
NO SUSTENTADA
```

No:

```text
FALSA
```

Solamente usaremos `CONTRADICHA` cuando exista evidencia suficientemente directa en contra.

---

# 2. Fecha de corte de la auditoría

Como solicitaste datos hasta julio de 2026, los documentos registrarán:

```yaml
knowledge_cutoff: 2026-07-31
audit_performed_at: 2026-08-05
```

Esto significa:

- Podemos consultar las páginas el 5 de agosto de 2026.
- Solo podemos incorporar acontecimientos, versiones o cambios publicados hasta el **31 de julio de 2026**.
- Una página actualizada en agosto puede utilizarse para consultar información histórica solamente si identifica claramente que el evento ocurrió antes del corte.
- No se mezclarán cambios posteriores a julio.

Esta distinción permite reproducir la auditoría en el futuro.

---

# 3. Jerarquía de fuentes

No todas las fuentes tienen el mismo valor.

## Nivel A — Evidencia primaria

La prioridad más alta:

- Artículos revisados por pares.
- Papers originales.
- Repositorios oficiales de una investigación.
- Documentación técnica oficial.
- System cards.
- Especificaciones oficiales.
- Resultados oficiales del benchmark.
- Comunicados del creador de un producto.
- Datos oficiales de precios y versiones.

## Nivel B — Evidencia institucional secundaria

- DORA.
- Linux Foundation.
- Organizaciones de investigación reconocidas.
- Documentación de estándares.
- Informes técnicos institucionales.

## Nivel C — Evidencia secundaria

- Análisis de especialistas.
- Medios técnicos reconocidos.
- Revisiones independientes.
- Reproducciones de experimentos.

Sirven para complementar, no para reemplazar una fuente primaria disponible.

## Nivel D — Evidencia débil

- Publicaciones en redes sociales.
- Reddit.
- Videos.
- Blogs sin metodología.
- Comparativas sin datos reproducibles.
- Afirmaciones de vendedores sobre competidores.

No las usaremos para establecer una conclusión importante, salvo que sean el objeto que estamos auditando.

---

# 4. Sistema de clasificación

Cada afirmación tendrá tres dimensiones independientes.

## 4.1 Estado de evidencia

| Código | Estado | Significado |
|---|---|---|
| `VERIFIED` | Verificada | La fuente respalda directamente la afirmación |
| `PARTIAL` | Parcialmente verificada | Existe respaldo, pero el curso exagera o generaliza |
| `HEURISTIC` | Heurística | Regla práctica útil, no ley demostrada |
| `UNSUPPORTED` | No sustentada | No se encontró evidencia suficiente |
| `CONTRADICTED` | Contradicha | Evidencia actual contradice la afirmación |
| `OUTDATED` | Obsoleta | Fue cierta o razonable, pero dejó de estar vigente |

## 4.2 Estabilidad temporal

| Código | Significado |
|---|---|
| `STABLE` | Poco probable que cambie rápidamente |
| `VERSIONED` | Depende de una versión concreta |
| `VOLATILE` | Puede cambiar en semanas o meses |

## 4.3 Confianza

| Grado | Significado |
|---|---|
| `A` | Fuente primaria directa y conclusión clara |
| `B` | Evidencia sólida con alguna limitación |
| `C` | Evidencia indirecta, incompleta o muy contextual |
| `D` | Hipótesis o recomendación todavía no evaluada |

De esta forma no reducimos todo a “verdadero o falso”.

---

# 5. Resultado de la auditoría del Módulo 1

Los cuatro documentos del módulo presentan los tres pilares como herramienta, contexto y prompt; después proponen taxonomías de herramientas, reglas de gestión del contexto, archivos persistentes y patrones de prompting. fileciteturn9file0L2-L2 fileciteturn10file0L2-L2 fileciteturn13file0L2-L2 fileciteturn16file0L2-L2

La auditoría muestra que el **modelo mental general es útil**, pero el módulo mezcla cinco cosas diferentes:

```text
Resultados científicos
+
documentación oficial
+
experiencia profesional
+
taxonomías pedagógicas
+
instantáneas comerciales
```

Estas categorías no deben recibir el mismo peso.

---

## 5.1 Lección 1 — Modelo mental de los tres pilares

| ID | Afirmación resumida | Veredicto | Corrección científica |
|---|---|---|---|
| `M1-001` | Herramienta, contexto y prompt son tres pilares co-iguales | `HEURISTIC / C` | Es un modelo pedagógico útil, pero no se encontró un experimento que demuestre que sus efectos sean universalmente “co-iguales” |
| `M1-002` | El modelo ya no es el cuello de botella | `PARTIAL / B` | El modelo no explica por sí solo el resultado, pero puede seguir siendo un cuello de botella según la tarea, el lenguaje, el agente y el nivel de dificultad |
| `M1-003` | METR encontró que la IA hacía a desarrolladores experimentados 19% más lentos | `VERIFIED / A` | Correcto para el entorno específico estudiado: desarrolladores OSS experimentados, sus propios repositorios y herramientas de comienzos de 2025 |
| `M1-004` | Los desarrolladores creían ser más rápidos aunque fueron más lentos | `VERIFIED / A` | El estudio encontró una diferencia importante entre percepción y tiempo observado |
| `M1-005` | En febrero de 2026 el efecto cambió a −18% | `PARTIAL / A` | Ese fue el estimado bruto para desarrolladores originales, con intervalo de −38% a +9%; METR considera los nuevos datos una señal poco fiable |
| `M1-006` | Los nuevos participantes mostraron −4% | `PARTIAL / A` | Correcto como estimación puntual, pero su intervalo de −15% a +9% incluye ausencia de efecto |
| `M1-007` | Copilot produjo 19% menos código original de core developers y 6,5% más revisión | `VERIFIED / B` | Las cifras aparecen en el estudio, pero no deben generalizarse automáticamente a todos los equipos, repositorios o herramientas |
| `M1-008` | La IA traslada trabajo del autor al revisor | `PARTIAL / B` | Es una interpretación coherente con el estudio analizado, no una ley universal |
| `M1-009` | Agente = modelo + scaffolding | `HEURISTIC / B` | Es una abstracción arquitectónica útil, no una ecuación científica completa |
| `M1-010` | OpenAI publicó Harness Engineering en febrero de 2026 | `VERIFIED / A` | La publicación existe y documenta el papel del repositorio, herramientas, restricciones y feedback loops |
| `M1-011` | El harness puede importar tanto o más que pequeñas diferencias entre modelos | `VERIFIED / B` | Está respaldado por experimentos donde la infraestructura cambia varios puntos los resultados de evaluaciones agentic |
| `M1-012` | El modelo no importa frente al harness | `CONTRADICTED / B` | Tanto el modelo como el harness influyen; la evidencia no permite eliminar ninguno de los dos |

El estudio original de METR encontró un aumento del tiempo de finalización del 19%, pero la propia organización lo describe como una instantánea de herramientas de principios de 2025. En febrero de 2026, METR informó estimaciones más favorables, pero advirtió que selección de participantes, remuneración y medición del trabajo paralelo hacían poco fiables las nuevas cifras. citeturn748769search4turn748769search5

El estudio sobre mantenimiento informa el 6,5% adicional de revisión y la caída del 19% en código original de desarrolladores principales, pero es un análisis de actividad OSS, no un RCT que autorice a aplicar esas cifras a todo desarrollo profesional. citeturn748769academia48

DORA ofrece una formulación más prudente: la IA funciona como un **amplificador de fortalezas y debilidades organizacionales**, y las ganancias dependen del sistema que rodea la herramienta. También encontró la tensión entre mayor throughput y mayor inestabilidad cuando la base de ingeniería no es sólida. citeturn748769search0turn748769search8turn748769search16

### Declaración corregida que adoptaremos

```text
El rendimiento del desarrollo asistido por IA depende conjuntamente
de las capacidades del modelo, el harness, el contexto, la calidad
de la especificación, los mecanismos de verificación y el sistema
de ingeniería de la organización.

Ninguno de esos factores debe declararse universalmente irrelevante
o universalmente dominante sin una evaluación sobre la tarea real.
```

---

## 5.2 La comparación 80,9% frente a 45,9%

Esta es una de las correcciones más importantes del módulo.

El curso afirma aproximadamente:

```text
Claude Opus 4.5:
80,9% en SWE-bench Verified
45,9% en SWE-bench Pro

Diferencia:
35 puntos causados por el scaffolding
```

## Qué está verificado

SWE-bench Verified contiene 500 problemas filtrados y revisados por humanos. SWE-bench Pro contiene 1.865 instancias procedentes de 41 repositorios y fue creado para aumentar dificultad, diversidad y resistencia a contaminación. Por lo tanto, **no son el mismo conjunto de problemas**. citeturn715058search14turn715058search2

Anthropic reportó para Opus 4.5:

```text
SWE-bench Verified:
80,90% sin thinking
80,60% con configuración de thinking descrita

SWE-bench Pro en su propia evaluación:
aproximadamente 52%
```

La tabla pública de Scale mostró aproximadamente:

```text
45,89%
```

para Opus 4.5 bajo otra configuración de agente/evaluación. citeturn715058search40turn715058search43

## Qué no puede concluirse

No es válido afirmar:

```text
Toda la diferencia de 35 puntos se debe al harness.
```

Cambiaron simultáneamente:

- Dataset.
- Repositorios.
- Lenguajes.
- Dificultad.
- Distribución de tareas.
- Controles de contaminación.
- Scaffolding.
- Presupuesto de ejecución.
- Posiblemente configuración de razonamiento.
- Metodología de evaluación.

La propia investigación de Anthropic confirma que la infraestructura de un benchmark agentic puede producir diferencias de varios puntos; en sus experimentos con Terminal-Bench 2.0, la diferencia entre configuraciones llegó a seis puntos. Esto demuestra que el harness importa, pero no que explique por sí solo los 35 puntos comparados por el curso. citeturn461702search4

### Veredicto

```yaml
claim_id: M1-013
status: PARTIAL
confidence: A
problem: causal attribution not established
```

### Declaración corregida

```text
Opus 4.5 obtuvo resultados muy diferentes en SWE-bench Verified
y SWE-bench Pro. Esa diferencia no mide exclusivamente el harness,
porque los benchmarks y las configuraciones también son diferentes.

Los resultados demuestran que un score no debe interpretarse fuera
del dataset, scaffold, infraestructura, presupuesto y protocolo con
los que se obtuvo.
```

---

## 5.3 Lección 2 — La herramienta

| ID | Afirmación | Veredicto | Uso en el proyecto |
|---|---|---|---|
| `M1-014` | Existen cuatro categorías canónicas A/B/C/D | `HEURISTIC / C` | Puede utilizarse como taxonomía de trabajo, no como estándar formal |
| `M1-015` | IDE, CLI, nube y herramientas especializadas son modos diferentes | `VERIFIED / B` | La distinción es operativamente útil |
| `M1-016` | Completion y agentic son modos distintos | `VERIFIED / B` | Útil, aunque existe un continuo entre ambos |
| `M1-017` | Si toca varios archivos, siempre requiere modo agentic | `HEURISTIC / C` | Regla razonable, no obligación universal |
| `M1-018` | Los umbrales de 50k y 500k LoC determinan herramienta | `UNSUPPORTED / D` | No se usarán como política |
| `M1-019` | Una herramienta concreta es mejor para Rust, Java o .NET | `UNSUPPORTED / D` | Requiere evaluaciones comparables y actuales por repositorio |
| `M1-020` | Los modelos locales satisfacen automáticamente compliance | `CONTRADICTED / B` | Alojamiento local no garantiza cumplimiento; también importan datos, controles, contratos, auditoría y operación |
| `M1-021` | El stack híbrido A+B+D es el patrón senior universal | `HEURISTIC / C` | Puede servir como referencia, no como requisito |
| `M1-022` | Solo cuatro benchmarks merecen utilizarse | `HEURISTIC / C` | Es una selección editorial, no una lista científica completa |
| `M1-023` | Comparar scores de distintos vendors sin igualar harness es engañoso | `VERIFIED / A` | Se adoptará como regla de evaluación |
| `M1-024` | Elegir herramienta según tarea y control humano | `VERIFIED / B` | Se adoptará como principio de decisión |
| `M1-025` | Claude Code es adecuado para este proyecto | `PROJECT_DECISION` | Lo usamos por su harness CLI, herramientas y porque es el entorno elegido, no porque esté probado como mejor para todo |

OpenAI documentó que su experiencia construyendo con agentes dependió de diseñar entornos, repositorios legibles, feedback loops, pruebas y restricciones mecánicas. También reconoce expresamente que esa experiencia pertenece a un repositorio y una inversión concretos, por lo que no debe generalizarse automáticamente. citeturn461702search1

### Decisión para nuestro proyecto

No escribiremos:

```text
Claude Code es la mejor herramienta.
```

Escribiremos:

```text
Claude Code es la herramienta principal seleccionada para este
proyecto debido a su integración con terminal, Git, lectura y edición
de archivos, ejecución de verificaciones, Plan Mode, skills, hooks,
subagentes y MCP.

La decisión se evaluará mediante resultados del propio proyecto:
calidad, regresiones, costo, tiempo, adherencia a instrucciones
y porcentaje de cambios aceptados después de revisión.
```

---

## 5.4 Precios, modelos y ventanas: contenido volátil

La tabla del curso era una instantánea de abril de 2026. No debe convertirse en conocimiento persistente.

Para el 31 de julio de 2026:

- Anthropic ya había presentado Claude Opus 4.8 el 28 de mayo, por lo que Opus 4.7 había dejado de ser la versión más reciente de esa línea. citeturn576234search3
- OpenAI había lanzado GPT-5.6 de forma general el 9 de julio de 2026, por lo que GPT-5.4 tampoco era ya la referencia más reciente. citeturn576234search0
- Gemini 3.1 Pro Preview tenía un límite oficial de entrada de 1.048.576 tokens, no dos millones como indica la tabla del módulo. citeturn497116search0
- GitHub cambió Copilot a facturación basada en AI Credits el 1 de junio de 2026; un crédito equivale a 0,01 USD y el consumo depende de modelo y tokens. citeturn576234search2turn576234search4

| ID | Afirmación | Estado |
|---|---|---|
| `M1-026` | Opus 4.7 es el Claude más reciente | `OUTDATED / A` |
| `M1-027` | GPT-5.4 es el GPT más reciente | `OUTDATED / A` |
| `M1-028` | Gemini 3.1 Pro tiene 2M de contexto | `CONTRADICTED / A` |
| `M1-029` | La tabla de precios de abril sigue vigente | `OUTDATED / A` |
| `M1-030` | El modelo disponible determina permanentemente la herramienta | `CONTRADICTED / B` |

### Regla que adoptaremos

```text
No introducir tablas de precios, versiones o modelos cambiantes
en AGENTS.md o CLAUDE.md.

Cuando sean necesarias, se documentarán en archivos fechados con:

- observed_at
- valid_through
- official_source
- region
- plan
- currency
- tax assumptions
```

---

## 5.5 Lección 3 — Contexto

| ID | Afirmación | Veredicto | Matiz |
|---|---|---|---|
| `M1-031` | Más contexto puede reducir calidad | `VERIFIED / A` | Respaldado por estudios y documentación |
| `M1-032` | Todos los modelos siempre degradan sin excepción | `PARTIAL / B` | Fue observado en determinados modelos y tareas; no demuestra una ley para todo modelo futuro |
| `M1-033` | La ventana máxima es un techo, no un objetivo | `VERIFIED / B` | Buen principio operativo |
| `M1-034` | La información en el medio puede recibir peor uso | `VERIFIED / A` | Respaldado por Lost in the Middle |
| `M1-035` | La degradación empieza universalmente entre 30% y 50% | `UNSUPPORTED / D` | Depende del modelo, tarea y composición del contexto |
| `M1-036` | A 50% empieza el deterioro notable | `HEURISTIC / D` | No es límite científico universal |
| `M1-037` | A 70% siempre se debe compactar | `HEURISTIC / D` | Puede ser útil, pero debe medirse |
| `M1-038` | A 90% siempre debe reiniciarse | `HEURISTIC / D` | No existe como ley general |
| `M1-039` | Después de 15–20 turnos debe reiniciarse | `UNSUPPORTED / D` | Los turnos no miden su cantidad ni densidad de tokens |
| `M1-040` | La atención cuadrática explica directamente el context rot | `PARTIAL / C` | Es una explicación simplificada; arquitecturas e inferencia modernas complican esa causalidad |
| `M1-041` | Los distractores similares interfieren | `VERIFIED / B` | Respaldado por evaluaciones de contexto largo |
| `M1-042` | El contexto debe curarse, no acumularse | `VERIFIED / A` | Se adoptará |
| `M1-043` | La gestión activa mejora agentes de largo horizonte | `VERIFIED / A` | Respaldado por investigación de 2026 |
| `M1-044` | El agentic search siempre supera al RAG | `UNSUPPORTED / D` | Anthropic recomienda estrategias just-in-time o híbridas según la tarea |
| `M1-045` | Write, Select, Compress, Isolate es una taxonomía útil | `HEURISTIC / B` | Útil como modelo operativo, no única taxonomía posible |

Chroma evaluó 18 modelos y encontró que el rendimiento se vuelve menos fiable a medida que aumenta el input, incluso en tareas simples. La conclusión válida se limita a los modelos, configuraciones y tareas estudiados; no demuestra que cada modelo futuro falle en un porcentaje idéntico de su ventana. citeturn919460search8

`Lost in the Middle` mostró que el desempeño suele ser superior cuando la información relevante está al principio o al final y puede degradarse cuando se encuentra en la zona central. citeturn919460search1

NoLiMa encontró degradación fuerte al exigir asociaciones semánticas sin coincidencia literal: a 32K tokens, 11 de 13 modelos cayeron por debajo de la mitad de su baseline corto; GPT-4o pasó de 99,3% a 69,7%. citeturn919460search0

LOCA-bench encontró deterioro en escenarios agentic con crecimiento controlado del contexto y mejoras sustanciales mediante técnicas avanzadas de gestión. En julio de 2026, trabajos de ACL también reportaron beneficios de administrar el contexto como una parte activa del agente, no como un historial append-only. citeturn919460academia48turn919460search2turn919460search7

### Regla corregida para nuestro proyecto

No usaremos 50/70/90 como una ley.

Usaremos señales observables:

```text
Compactar o reiniciar cuando aparezca una o más señales:

- Claude pierde una restricción previamente establecida.
- Repite exploraciones ya realizadas.
- Confunde archivos o decisiones.
- Recupera instrucciones obsoletas.
- La tarea cambia de objetivo.
- Finaliza un hito natural.
- /context muestra crecimiento que ya no aporta señal.
- La sesión contiene grandes outputs de logs o investigación.
- Una nueva tarea necesita un conjunto de archivos diferente.
```

Claude Code confirma que su rendimiento puede deteriorarse mientras el contexto se llena y recomienda administrarlo de forma activa. `/context` permite inspeccionar qué lo consume; `/compact` resume el historial; los archivos raíz de instrucciones se vuelven a cargar después de compactar. citeturn416647search1turn416647search5

---

## 5.6 `AGENTS.md` y `CLAUDE.md`

| ID | Afirmación | Veredicto |
|---|---|---|
| `M1-046` | AGENTS.md apareció en agosto de 2025 | `VERIFIED / A` |
| `M1-047` | Superó 60.000 proyectos OSS | `VERIFIED_AS_VENDOR_REPORTED / B` |
| `M1-048` | Fue aportado a AAIF bajo Linux Foundation | `VERIFIED / A` |
| `M1-049` | Claude Code lee AGENTS.md nativamente | `CONTRADICTED / A` |
| `M1-050` | Puede mantenerse AGENTS.md como fuente portable | `VERIFIED / A` |
| `M1-051` | CLAUDE.md puede importar AGENTS.md | `VERIFIED / A` |
| `M1-052` | Un único archivo gigante mejora el contexto | `CONTRADICTED / A` |
| `M1-053` | CLAUDE.md debe aspirar a menos de 200 líneas | `VERIFIED_GUIDANCE / A` |
| `M1-054` | Instrucciones especializadas deben moverse a rules o skills | `VERIFIED_GUIDANCE / A` |

OpenAI y Linux Foundation confirman que AGENTS.md fue lanzado en agosto de 2025, superó 60.000 proyectos según los datos publicados por OpenAI y fue aportado a la Agentic AI Foundation en diciembre de 2025 junto con MCP y goose. citeturn232113search0turn232113search1

Sin embargo, la documentación actual de Claude Code dice expresamente que Claude Code lee `CLAUDE.md`, no `AGENTS.md`. Para portabilidad recomienda importar:

```md
@AGENTS.md
```

dentro de `CLAUDE.md`. citeturn416647search4

Anthropic recomienda apuntar a menos de 200 líneas por `CLAUDE.md`; los documentos largos consumen contexto y reducen adherencia. Las reglas por ruta y skills permiten cargar contenido solamente cuando corresponde. citeturn495608search0turn495608search6

---

## 5.7 Write, Select, Compress e Isolate

Los cuatro verbos del curso son una buena síntesis, pero deben entenderse como un modelo de ingeniería.

```text
WRITE
Persistir fuera de la ventana.

SELECT
Traer únicamente lo relevante.

COMPRESS
Sustituir historial voluminoso por un resumen de alta señal.

ISOLATE
Enviar una subtarea a otra ventana o proceso.
```

Anthropic describe estrategias equivalentes:

- Recuperación just-in-time.
- Compaction.
- Notas estructuradas.
- Subagentes.
- Arquitecturas multiagente.
- Contexto mínimo de alta señal. citeturn731058search0

LangChain Deep Agents distingue contexto de entrada, contexto runtime, compresión, aislamiento y memoria a largo plazo. citeturn731058search12

Los subagentes de Claude Code trabajan en una ventana separada y devuelven principalmente su resultado resumido, por lo que sirven para aislar lecturas, búsquedas o logs que no deben inundar el hilo principal. citeturn416647search6

### Decisión

Adoptaremos los cuatro verbos como marco operativo, no como afirmación de que son la única taxonomía científica posible.

---

## 5.8 Lección 4 — Prompt e integración

| ID | Afirmación | Veredicto | Corrección |
|---|---|---|---|
| `M1-055` | “Think step by step” ya no sirve | `PARTIAL / C` | Puede ser innecesario en modelos razonadores, pero no es universalmente inútil |
| `M1-056` | Chain-of-thought es contraproducente | `UNSUPPORTED_AS_UNIVERSAL / D` | Depende del modelo, modalidad y tarea |
| `M1-057` | Few-shot es poco importante | `PARTIAL / C` | Anthropic sigue recomendando ejemplos diversos y canónicos |
| `M1-058` | La persona “eres experto” casi nunca ayuda | `UNSUPPORTED_AS_UNIVERSAL / D` | Debe evaluarse por tarea |
| `M1-059` | XML y encabezados ayudan a delimitar secciones | `VERIFIED_GUIDANCE / A` | Útiles especialmente con inputs complejos |
| `M1-060` | Prefilling está disponible de forma general | `PARTIAL / A` | No está disponible con extended thinking |
| `M1-061` | Más de 2.000 tokens convierte un prompt en malo | `UNSUPPORTED / D` | No existe un umbral universal de 2.000 |
| `M1-062` | Un prompt debe contener la mínima estructura suficiente | `VERIFIED_GUIDANCE / A` | Minimal no significa necesariamente corto |
| `M1-063` | Criterios de éxito mejoran el trabajo agentic | `VERIFIED_GUIDANCE / A` | Deben ser comprobables |
| `M1-064` | Dar al agente una forma de verificar es de alto impacto | `VERIFIED_GUIDANCE / A` | Se adoptará como requisito |
| `M1-065` | Plan Mode debe usarse siempre | `CONTRADICTED / A` | Añade overhead; se recomienda para cambios inciertos, complejos o multiarchivo |
| `M1-066` | Explore → Plan → Implement es un patrón válido | `VERIFIED_GUIDANCE / A` | Especialmente para trabajo complejo |
| `M1-067` | Test-first siempre es la mejor estrategia | `HEURISTIC / C` | Muy útil para comportamientos verificables, pero no toda tarea exige el mismo orden |
| `M1-068` | Writer/Reviewer puede detectar defectos | `HEURISTIC / B` | Debe medirse mediante evaluaciones del proyecto |
| `M1-069` | Outcome y criterios son mejores que microgestionar cada paso | `VERIFIED_GUIDANCE / B` | Siempre que existan restricciones suficientes |
| `M1-070` | Un prompt largo es necesariamente peor | `CONTRADICTED / B` | Lo perjudicial es el ruido y la baja señal, no una longitud aislada |

Anthropic recomienda encontrar el conjunto mínimo de información que describa completamente el comportamiento esperado. Aclara expresamente que “mínimo” no significa necesariamente “corto”; también sigue recomendando ejemplos pocos, diversos y canónicos. citeturn731058search0

Los delimitadores XML o encabezados ayudan a estructurar contenido, aunque la importancia del formato exacto puede disminuir a medida que mejoran los modelos. citeturn527563search8

El prefilling existe, pero solamente en modos sin extended thinking. Por eso no debe documentarse como técnica siempre disponible. citeturn527563search1

La documentación de Claude Code recomienda proporcionar tests, outputs esperados, capturas o verificaciones que permitan comprobar el trabajo. También recomienda explorar, planificar e implementar cuando el cambio es complejo; advierte que Plan Mode añade overhead en cambios triviales. citeturn495608search3turn495608search9

---

# 6. Conclusiones que adoptaremos para el proyecto

## Conservar como principios fuertes

```text
1. El modelo aislado no determina el resultado.

2. El harness y los mecanismos de verificación importan.

3. El contexto es finito y debe curarse activamente.

4. Más contexto no significa automáticamente mejor resultado.

5. CLAUDE.md debe ser conciso y de alta señal.

6. La información especializada debe cargarse bajo demanda.

7. Los subagentes sirven para aislar investigación voluminosa.

8. Los prompts necesitan objetivo, criterios de éxito,
   restricciones y referencias relevantes.

9. Claude debe disponer de una forma determinista de comprobar
   su trabajo.

10. Los benchmarks solo son comparables cuando se conocen
    dataset, scaffold, presupuesto e infraestructura.
```

## Conservar como heurísticas, no como leyes

```text
- Los tres pilares son exactamente co-iguales.
- Las cuatro categorías A/B/C/D son canónicas.
- 50k y 500k líneas determinan la herramienta.
- 50% / 70% / 90% determinan la gestión del contexto.
- Una sesión debe reiniciarse después de 15–20 turnos.
- Un prompt de más de 2.000 tokens es incorrecto.
- Una herramienta específica siempre gana en cierto lenguaje.
- Test-first es obligatorio para toda tarea.
```

## Corregir

```text
- Claude Code no lee AGENTS.md directamente.
- Gemini 3.1 Pro no tenía 2M de entrada; tenía 1.048.576.
- Opus 4.7 ya no era el Claude más reciente en julio de 2026.
- GPT-5.4 ya no era el GPT más reciente en julio de 2026.
- La diferencia Verified/Pro no puede atribuirse solo al harness.
- Chain-of-thought no es universalmente inútil o perjudicial.
- Prefilling no funciona con extended thinking.
```

---

# 7. Artefactos que crearemos

En el repositorio nuevo:

```text
docs/
└── research/
    └── module-01/
        ├── README.md
        ├── methodology.md
        ├── evidence-matrix.md
        ├── source-register.md
        └── project-implications.md
```

## Responsabilidad de cada archivo

### `README.md`

Índice del estudio:

- Propósito.
- Fecha de corte.
- Commit del curso auditado.
- Archivos.
- Cómo interpretar estados.
- Cómo actualizar la auditoría.

### `methodology.md`

Método:

- Pregunta de auditoría.
- Jerarquía de fuentes.
- Estados.
- Reglas de causalidad.
- Reglas temporales.
- Tratamiento de evidencia contradictoria.
- Cómo auditar benchmarks.
- Limitaciones.

### `evidence-matrix.md`

La matriz completa con al menos las 70 afirmaciones atómicas anteriores.

### `source-register.md`

Registro reproducible de fuentes:

```yaml
source_id:
title:
organization:
authors:
source_type:
published_at:
retrieved_at:
knowledge_cutoff_eligible:
authority_level:
peer_review_status:
claims_supported:
limitations:
canonical_url:
archived_url:
```

No todos los campos aplicarán a todas las fuentes.

### `project-implications.md`

Qué cambia para nuestro proyecto:

- Qué prácticas adoptamos.
- Qué prácticas no adoptamos.
- Qué hipótesis evaluaremos localmente.
- Qué información no debe ir en `CLAUDE.md`.
- Qué métricas recogeremos más adelante.

---

# 8. Preparar el repositorio de referencia

No copies el curso dentro del nuevo repositorio.

Un repositorio Git anidado podría:

- Contaminar el proyecto.
- Ser agregado accidentalmente.
- Crear problemas con submódulos.
- Añadir material que no pertenece al producto.
- Inflar el contexto.

Desde la raíz de `conversational-ai-agent-platform`, sal una carpeta:

```bash
cd ..
```

Clona una copia de referencia:

```bash
git clone --depth 1 https://github.com/Diiegoal/CursoIA.git CursoIA-reference
```

Cuando ya exista:

```bash
git -C CursoIA-reference pull --ff-only
```

Registra exactamente qué commit estamos auditando:

```bash
git -C CursoIA-reference rev-parse HEAD
```

Guarda temporalmente el SHA que aparece.

Después regresa:

```bash
cd conversational-ai-agent-platform
```

Verifica:

```bash
git status
```

Debe continuar limpio.

---

# 9. Crear la rama del Paso 2

Ejecuta:

```bash
git switch -c docs/module-01-evidence-audit
```

Comprueba:

```bash
git branch --show-current
git status
```

Resultado esperado:

```text
docs/module-01-evidence-audit
```

---

# 10. Abrir Claude Code con acceso limitado al curso

Ejecuta:

```bash
claude --add-dir ../CursoIA-reference
```

Claude puede pedir autorización para acceder al directorio adicional.

Autoriza únicamente:

```text
../CursoIA-reference
```

No autorices tu carpeta completa de documentos ni tu directorio personal.

Esto aplica en la práctica `SELECT`:

```text
No entregamos todos tus archivos.
Entregamos únicamente el repositorio nuevo y el curso de referencia.
```

Dentro de Claude Code ejecuta:

```text
/status
```

Después:

```text
/context
```

Comprueba que el contexto no contiene accidentalmente otros proyectos.

---

# 11. Primera ejecución: Plan Mode

Activa Plan Mode con `Shift + Tab` hasta que la interfaz indique que Claude no editará archivos.

Pega este prompt:

```text
Trabaja exclusivamente en modo de análisis y planificación.

NO crees, edites, elimines ni renombres archivos todavía.
NO instales dependencias.
NO generes código de aplicación.
NO modifiques README.md.
NO ejecutes comandos destructivos.
NO uses información posterior al 31 de julio de 2026.

OBJETIVO

Planificar una auditoría científica y técnica del Módulo 1 del repositorio
de referencia disponible en:

../CursoIA-reference/Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/

Debes leer íntegramente los cuatro archivos Markdown vigentes de esa carpeta.

La auditoría deberá producir después, pero todavía no crear:

docs/research/module-01/README.md
docs/research/module-01/methodology.md
docs/research/module-01/evidence-matrix.md
docs/research/module-01/source-register.md
docs/research/module-01/project-implications.md

FECHA DE CORTE

knowledge_cutoff: 2026-07-31
audit_performed_at: 2026-08-05

METODOLOGÍA OBLIGATORIA

1. Descomponer las afirmaciones del curso en claims atómicos.
2. No tratar una afirmación compuesta como una sola fila.
3. Distinguir:
   - hecho empírico;
   - interpretación;
   - recomendación;
   - heurística;
   - taxonomía pedagógica;
   - afirmación comercial;
   - información volátil.
4. Priorizar papers, documentación oficial, system cards,
   especificaciones y resultados oficiales.
5. No usar blogs SEO, contenido generado, Reddit o videos como
   evidencia principal.
6. No confundir ausencia de evidencia con falsedad.
7. No comparar benchmarks sin registrar dataset, scaffold,
   infraestructura, presupuesto y protocolo.
8. No atribuir causalidad cuando la evidencia solo muestra asociación.
9. No copiar párrafos completos de las fuentes.
10. Toda conclusión debe registrar limitaciones.

ESTADOS PERMITIDOS

VERIFIED
PARTIAL
HEURISTIC
UNSUPPORTED
CONTRADICTED
OUTDATED
PROJECT_DECISION

ESTABILIDAD PERMITIDA

STABLE
VERSIONED
VOLATILE

CONFIANZA PERMITIDA

A
B
C
D

FUENTES MÍNIMAS QUE DEBES LOCALIZAR

- METR: estudio de productividad de julio de 2025.
- METR: actualización metodológica de febrero de 2026.
- DORA State of AI-assisted Software Development 2025.
- Paper arXiv 2510.10165, versión revisada en 2026.
- OpenAI: Harness engineering, febrero de 2026.
- Anthropic: Quantifying infrastructure noise in agentic coding evals.
- OpenAI/SWE-bench: SWE-bench Verified.
- Scale AI: SWE-bench Pro.
- System card de Claude Opus 4.5.
- Chroma: Context Rot.
- Lost in the Middle, TACL 2024.
- NoLiMa, ICML 2025.
- LOCA-bench, febrero de 2026.
- Context as a Tool, ACL Findings 2026.
- Anthropic: Effective context engineering for AI agents.
- Documentación de Claude Code sobre best practices.
- Documentación de Claude Code sobre memory.
- Documentación de Claude Code sobre context window.
- Documentación de Claude Code sobre subagents.
- Documentación de Claude Code sobre features/rules/skills.
- Linux Foundation y OpenAI sobre AGENTS.md y AAIF.
- Anthropic: lanzamiento de Opus 4.8.
- OpenAI: lanzamiento de GPT-5.6.
- Google: Gemini 3.1 Pro Preview.
- GitHub: billing de Copilot desde junio de 2026.

SALIDA DE ESTA FASE

Devuélveme solamente un plan.

El plan debe incluir:

1. Lista de los cuatro archivos leídos.
2. SHA del commit de CursoIA auditado.
3. Inventario inicial de afirmaciones.
4. Fuentes que buscarás.
5. Estructura exacta de cada archivo.
6. Riesgos de alucinación o sobreinterpretación.
7. Validaciones finales.
8. Archivos que permanecerán explícitamente sin modificar.

No ejecutes todavía el plan.
```

---

# 12. Cómo revisar el plan

No apruebes inmediatamente.

Comprueba:

```text
[ ] Identificó los cuatro archivos correctos.
[ ] Registró el commit SHA.
[ ] No pretende copiar el curso al repositorio nuevo.
[ ] No propone crear aplicación o instalar LangChain.
[ ] Separa hechos de recomendaciones.
[ ] Incluye las fechas de corte.
[ ] Prioriza fuentes primarias.
[ ] No propone tratar benchmarks distintos como equivalentes.
[ ] Incluye limitaciones.
[ ] Solo modificará docs/research/module-01/.
```

Cuando el plan incluya archivos ajenos al paso, corrige:

```text
Reduce el alcance. En este paso solo puedes crear los cinco archivos
bajo docs/research/module-01/. No modifiques ningún otro archivo.
Devuelve el plan corregido, sin ejecutarlo.
```

---

# 13. Ejecutar la auditoría

Cuando el plan sea correcto, cambia de Plan Mode a modo normal.

Pega:

```text
Ejecuta el plan aprobado.

ALCANCE ESTRICTO

Crea exclusivamente:

docs/research/module-01/README.md
docs/research/module-01/methodology.md
docs/research/module-01/evidence-matrix.md
docs/research/module-01/source-register.md
docs/research/module-01/project-implications.md

No modifiques ningún otro archivo.
No instales dependencias.
No generes código.
No crees CLAUDE.md ni AGENTS.md todavía.
No uses información posterior al 31 de julio de 2026.

REGLAS DE INVESTIGACIÓN

- Lee íntegramente los cuatro archivos del Módulo 1.
- Usa WebSearch y WebFetch solamente cuando sean necesarios.
- Prioriza fuentes oficiales y papers originales.
- Cuando una fuente comercial evalúe su propio producto, indícalo.
- Cuando no exista evidencia suficiente, usa UNSUPPORTED.
- Cuando una regla sea experiencia profesional, usa HEURISTIC.
- Cuando haya cambiado por versión o fecha, usa OUTDATED.
- No inventes DOI, autores, fechas, cifras ni URLs.
- No copies grandes fragmentos de las fuentes.
- Parafrasea y registra la fuente canónica.
- Registra tanto evidencia favorable como limitaciones.

EVIDENCE MATRIX

Crea al menos 70 claims atómicos.

Cada claim debe contener:

- claim_id
- lesson
- original_claim_summary
- claim_type
- evidence_status
- temporal_stability
- confidence
- source_ids
- evidence_summary
- limitations
- corrected_statement
- project_implication
- review_trigger

Usa identificadores M1-001, M1-002, etc.

Incluye obligatoriamente claims separados sobre:

- Los tres pilares como co-iguales.
- “El modelo ya no es el cuello de botella”.
- METR 2025.
- Actualización METR 2026.
- Paper 2510.10165.
- 80,9% versus 45,9%.
- Atribución de los 35 puntos al harness.
- Agente = modelo + scaffolding.
- Taxonomía A/B/C/D.
- Completion frente a agentic.
- Umbrales por líneas de código.
- Recomendaciones por lenguaje.
- Privacidad y compliance.
- Precios.
- Listas de modelos.
- Benchmarks.
- Context rot.
- Lost in the Middle.
- NoLiMa.
- LOCA-bench.
- Umbrales 50/70/90.
- Regla de 15–20 turnos.
- AGENTS.md.
- CLAUDE.md.
- Límite recomendado de 200 líneas.
- Write, Select, Compress e Isolate.
- Subagentes.
- Agentic search frente a RAG.
- Chain-of-thought.
- Few-shot.
- Persona prompting.
- XML.
- Prefilling.
- Umbral de 2.000 tokens.
- Criterios de éxito.
- Plan Mode.
- Test-first.
- Writer/Reviewer.
- Explore → Plan → Implement → Verify.

SOURCE REGISTER

Asigna IDs S-001, S-002, etc.

Para cada fuente registra:

- title
- authors_or_organization
- source_type
- publication_date
- retrieval_date
- knowledge_cutoff_eligible
- authority_level
- peer_review_status
- claims_supported
- limitations
- canonical_url

PROJECT IMPLICATIONS

Separa:

1. Prácticas adoptadas.
2. Heurísticas que necesitan evaluación local.
3. Afirmaciones descartadas.
4. Información volátil que no debe ir en CLAUDE.md.
5. Métricas que mediremos posteriormente.
6. Preguntas todavía abiertas.

FINALIZACIÓN

Antes de terminar:

1. Relee los cinco archivos.
2. Comprueba que no haya TODO, TBD, FIXME ni citas inventadas.
3. Confirma que ninguna fuente posterior al cutoff afecte conclusiones.
4. Confirma que toda cifra tenga fuente.
5. Confirma que ninguna conclusión exceda la evidencia.
6. Ejecuta git diff --check.
7. Muestra:
   - archivos creados;
   - cantidad de claims;
   - cantidad de fuentes;
   - distribución por estado;
   - limitaciones pendientes.

No hagas commit.
```

---

# 14. Revisión manual

Cuando Claude termine, sal:

```text
/exit
```

Ejecuta:

```bash
find docs/research/module-01 -maxdepth 1 -type f -print
```

Debes obtener los cinco archivos.

Después:

```bash
wc -l docs/research/module-01/*.md
```

No existe un límite estricto de 200 líneas para estos documentos porque **no se cargarán automáticamente**. La recomendación de 200 líneas aplica especialmente a `CLAUDE.md`, que entra completo en el contexto de cada sesión. Los documentos de investigación pueden ser más extensos y cargarse bajo demanda. citeturn495608search6

Busca marcadores incompletos:

```bash
rg -n "TODO|TBD|FIXME|PLACEHOLDER|INSERTAR|PENDIENTE DE COMPLETAR" docs/research/module-01
```

Resultado esperado:

```text
Sin resultados
```

Busca fechas posteriores al corte:

```bash
rg -n "2026-08|2026-09|agosto de 2026|septiembre de 2026" docs/research/module-01
```

Debe estar vacío, excepto que `audit_performed_at` sea `2026-08-05`. Esa fecha es de ejecución, no de conocimiento.

Comprueba diferencias:

```bash
git diff --stat
git diff --check
git status --short
```

Resultado esperado en `git status --short`:

```text
?? docs/research/module-01/
```

Ningún otro archivo debe aparecer.

---

# 15. Revisión independiente con una sesión limpia

La misma sesión que escribió la auditoría puede estar sesgada por sus propias conclusiones.

Abre una sesión nueva:

```bash
claude --add-dir ../CursoIA-reference
```

No reanudes la sesión anterior.

Pega:

```text
Realiza una revisión independiente y de solo lectura.

No edites archivos.
No ejecutes comandos que modifiquen estado.
No uses información posterior al 31 de julio de 2026.

Revisa:

docs/research/module-01/README.md
docs/research/module-01/methodology.md
docs/research/module-01/evidence-matrix.md
docs/research/module-01/source-register.md
docs/research/module-01/project-implications.md

Compara la auditoría con los cuatro documentos originales disponibles en:

../CursoIA-reference/Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/

Busca específicamente:

1. Claims importantes omitidos.
2. Claims compuestos que deberían dividirse.
3. Causalidades no demostradas.
4. Generalizaciones desde muestras limitadas.
5. Benchmarks comparados sin igualdad metodológica.
6. Fuentes comerciales tratadas como evidencia independiente.
7. Información posterior al cutoff.
8. Cifras sin fuente.
9. URLs incorrectas.
10. Estados VERIFIED demasiado fuertes.
11. Afirmaciones marcadas falsas cuando solo carecen de evidencia.
12. Recomendaciones confundidas con resultados científicos.
13. Contradicciones entre evidence-matrix y project-implications.
14. Material copiado excesivamente de las fuentes.

Devuelve un informe con:

- BLOCKERS
- MAJOR FINDINGS
- MINOR FINDINGS
- VERIFIED WITHOUT ISSUE
- RECOMMENDED CORRECTIONS

No edites nada.
```

## Interpretación

- `BLOCKER`: debe corregirse.
- `MAJOR`: debe corregirse antes del commit.
- `MINOR`: corrige cuando mejora claridad o trazabilidad.
- `VERIFIED WITHOUT ISSUE`: sección aceptada.

Cuando existan cambios, abre otra sesión o vuelve a la primera y proporciona exclusivamente las correcciones aprobadas:

```text
Aplica solamente las siguientes correcciones de la revisión independiente:

[PEGA AQUÍ LAS CORRECCIONES APROBADAS]

No cambies ningún otro contenido.
Después ejecuta git diff --check.
No hagas commit.
```

---

# 16. Validación final

Ejecuta:

```bash
git diff --check
```

Después:

```bash
git status --short
```

Y:

```bash
git diff -- docs/research/module-01
```

Comprueba los criterios:

```text
[ ] Solo existen los cinco archivos permitidos.
[ ] La fecha de corte es 2026-07-31.
[ ] Se registró el SHA de CursoIA.
[ ] Hay al menos 70 claims atómicos.
[ ] Toda cifra importante tiene fuente.
[ ] Las heurísticas están identificadas.
[ ] La información comercial está marcada VOLATILE.
[ ] Los benchmarks incluyen limitaciones.
[ ] La diferencia 80,9/45,9 no se atribuye solo al harness.
[ ] 50/70/90 no aparece como ley científica.
[ ] Claude Code no figura como lector nativo de AGENTS.md.
[ ] La ventana de Gemini 3.1 Pro figura como 1.048.576.
[ ] Opus 4.8 y GPT-5.6 aparecen en la corrección temporal.
[ ] No hay arquitectura de producto inventada.
[ ] No hay dependencias instaladas.
[ ] No existen secretos.
[ ] git diff --check no muestra errores.
```

---

# 17. Commit del Paso 2

Agrega solamente la investigación:

```bash
git add docs/research/module-01
```

Verifica lo preparado:

```bash
git diff --cached --stat
git diff --cached --check
```

Crea el commit:

```bash
git commit -m "docs: audit module 1 claims and evidence"
```

Sube la rama:

```bash
git push -u origin docs/module-01-evidence-audit
```

Crea el pull request:

```bash
gh pr create \
  --base main \
  --head docs/module-01-evidence-audit \
  --title "docs: audit Module 1 claims and evidence" \
  --body "## Summary

- Audits the claims from Module 1 against primary and official sources.
- Separates verified findings, partial evidence, heuristics, unsupported claims, outdated information, and project decisions.
- Establishes a reproducible evidence register with a knowledge cutoff of July 31, 2026.
- Records practical implications for the conversational AI agent project.

## Scope

Documentation only. No application code, dependencies, architecture, CLAUDE.md, AGENTS.md, MCP configuration, hooks, or agent definitions were added.

## Validation

- Independent review performed in a clean Claude Code session.
- No evidence after the July 31, 2026 cutoff used.
- git diff --check passes.
- Every numerical claim is linked to a registered source."
```

Después:

```bash
gh pr view --web
```

Revisa el PR y confirma que solo contiene:

```text
docs/research/module-01/
```

Cuando todo sea correcto, puedes fusionarlo desde GitHub o mediante:

```bash
gh pr merge --squash --delete-branch
```

Luego sincroniza `main`:

```bash
git switch main
git pull --ff-only
git status
```

Resultado final esperado:

```text
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

---

# Criterio de finalización del Paso 2

El paso estará terminado cuando:

```text
[ ] El curso se clonó fuera del repositorio del producto.
[ ] Se registró el commit exacto auditado.
[ ] Se crearon los cinco documentos.
[ ] Hay al menos 70 claims atómicos.
[ ] Cada claim tiene estado, estabilidad y confianza.
[ ] Existe un registro reproducible de fuentes.
[ ] Se documentaron limitaciones y correcciones.
[ ] Se realizó una segunda revisión en contexto limpio.
[ ] No se creó código de aplicación.
[ ] No se creó todavía CLAUDE.md ni AGENTS.md.
[ ] El cambio quedó registrado mediante PR.
[ ] main volvió a quedar limpio.
```

Con esto no habremos “demostrado que el curso está bien o mal”. Habremos hecho algo más útil: convertirlo en conocimiento trazable, con alcance, limitaciones y reglas claras sobre qué puede utilizarse para dirigir nuestro proyecto.

**¿Deseas continuar con el Paso 3 de 16: comprender y poner en práctica desde la raíz los conceptos modelo, copiloto, agente, harness, scaffolding, tool, contexto, memoria y prompt?**

---

## Usuario

Absolutamente todo funciono, el proyecto esta en https://github.com/DiiegoA/conversational-ai-agent-platform, me seguiras guiando en el proyecto paso a paso, detalladamente, explicando cada concepto desde sus fundamentos, sin omitir informacion, poniendo en practica todo el contenido para realizar el proyecto completo, al terminar cada paso me preguntaras si deseo continuar con el siguiente paso, cada paso usara su maxima ventana de contexto, seguimos con el mismo proyecto real, profesional, full stack, el agente ia conversacional, creadolo con Claude Code, continuemos con el Paso 3 de 16: comprender y poner en práctica desde la raíz los conceptos modelo, copiloto, agente, harness, scaffolding, tool, contexto, memoria y prompt, investiga exhaustivamente y busca en fuentes confiables sin inventar datos para hacer este paso 3, con datos mas recientes hasta Agosto 2026, si me entiendes?. 

---

## ChatGPT

Sí, te entendí. En este paso vamos a convertir los conceptos del Módulo 1 en **arquitectura mental y reglas operativas del proyecto**: qué es cada capa, qué responsabilidades tiene, qué no debe hacer y cómo Claude Code las distingue en la práctica. Primero verificaré el estado real del repositorio y después contrastaré cada concepto con documentación oficial y literatura técnica vigente hasta el **7 de agosto de 2026**.

---

## ChatGPT

La verificación del repositorio también quedó bien: el Paso 2 está fusionado en `main` mediante el commit `3226146a2ecb7a8dc903fbfc20651cc7f3ccd377`, y la auditoría terminó siendo mucho más rigurosa de lo mínimo: **238 claims y 45 fuentes**. Eso nos permite usar en este paso únicamente conceptos que sobrevivieron a la auditoría, y etiquetar como convención cualquier cosa que siga siendo una decisión de proyecto. 

---

## ChatGPT

# Paso 3 de 16 — Fundamentos reales de un sistema agentic

Sí. Seguimos sobre `DiiegoA/conversational-ai-agent-platform`. Verifiqué que el Paso 2 ya está fusionado en `main` y que la auditoría dejó **238 afirmaciones analizadas y 45 fuentes**, así que no necesitamos volver a aceptar las afirmaciones del curso como dogma: desde ahora distinguiremos evidencia, convención y decisión de proyecto. fileciteturn7file0L2-L2

Hay además una corrección importante a tu frase “usar la máxima ventana de contexto”: **vamos a usar el máximo contexto útil, no a intentar llenar la ventana**. Claude Code documenta que cada archivo leído y cada resultado de herramienta entra al contexto, mientras que Anthropic recomienda buscar el conjunto más pequeño de tokens de alta señal que permita resolver correctamente la tarea. citeturn403331search4turn892766search2

En este paso todavía **no instalaremos LangChain, no programaremos backend/frontend, no crearemos `CLAUDE.md`, `AGENTS.md`, MCP, hooks, skills ni subagentes personalizados**. Primero necesitamos que el vocabulario arquitectónico quede completamente claro.

---

# 1. El objetivo del Paso 3

Al terminar debes ser capaz de mirar cualquier sistema de IA y señalar sin confundir:

```text
MODELO
   ↓
PROMPT + CONTEXTO
   ↓
respuesta o solicitud de TOOL
   ↓
HARNESS / RUNTIME ejecuta la tool
   ↓
resultado de la tool
   ↓
nuevo CONTEXTO
   ↓
MODELO vuelve a decidir
   ↓
...
   ↓
respuesta final
```

Y además distinguir:

```text
MEMORIA
    ≠
CONTEXTO

PROMPT
    ⊂
CONTEXTO

TOOL CALL
    ≠
EJECUCIÓN DE LA TOOL

MODELO
    ≠
AGENTE

AGENTE
    ≠
HARNESS

COPILOTO
    ≠
AGENTE necesariamente

SCAFFOLDING
    ≈
estructura que rodea al modelo

HARNESS
    =
runtime/control que opera esa estructura
    [convención que adoptaremos en este proyecto]
```

Claude Code documenta exactamente su ciclo como **gather context → take action → verify results**, y dice explícitamente que los modelos razonan mientras las herramientas actúan; Claude Code funciona como el *agentic harness* alrededor del modelo. citeturn403331search2

---

# 2. Empecemos desde la raíz: ¿qué ocurre en una sola llamada a un modelo?

Imagina que por ahora no existe LangChain, Claude Code, memoria, RAG ni herramientas.

Tenemos solo:

```text
Usuario
   ↓
texto
   ↓
MODELO
   ↓
texto
```

Por ejemplo:

```text
Usuario:
¿Cuánto es 25 × 4?

        ↓

modelo

        ↓

100
```

Eso **no necesita un agente**.

El modelo es el motor de inferencia. LangChain actualmente lo describe como el **reasoning engine** de los agentes: interpreta información, puede decidir qué herramienta solicitar, interpretar resultados y decidir cuándo producir una respuesta final. Pero los modelos también pueden utilizarse completamente solos, fuera de cualquier agente. citeturn209538search0

Esta distinción parece sencilla, pero será una de las más importantes de todo nuestro proyecto.

---

# 3. Concepto 1 — MODELO

## Definición operativa

Para nuestro proyecto:

> **Modelo:** sistema de inferencia entrenado que recibe un contexto de entrada y produce una salida.

La salida puede ser:

```text
texto
datos estructurados
tool-call request
razonamiento soportado por el proveedor
multimodalidad
```

LangChain documenta hoy precisamente esas capacidades: generación, razonamiento, structured output, multimodalidad y tool calling. citeturn209538search0

## Qué hace el modelo

Puede decidir:

```text
Necesito responder directamente.
```

o:

```text
Necesito consultar una herramienta.
```

Por ejemplo:

```text
Usuario:
¿Cuál es el saldo actual de mi cuenta?

                    ↓

MODELO

                    ↓

No conozco el saldo.
Necesito solicitar:

get_account_balance(
    account_id="..."
)
```

Muy importante:

### El modelo todavía NO consultó la cuenta.

Solo produjo algo equivalente a:

```json
{
  "tool": "get_account_balance",
  "arguments": {
    "account_id": "123"
  }
}
```

LangChain lo deja muy claro: cuando un modelo standalone produce un tool call, **tu aplicación debe ejecutar la herramienta y devolverle el resultado**. Cuando utilizas un agente, el agent loop automatiza esa ejecución. citeturn209538search0

Por tanto:

```text
Modelo solicita acción
        ≠
acción ejecutada
```

---

# 4. Una forma extremadamente importante de visualizarlo

Piensa en el modelo como un **cerebro sin manos**.

Puede decir:

```text
"Necesito leer customer.json"
```

pero no puede mágicamente leerlo.

Necesita algo que transforme:

```text
intención
```

en:

```text
operación real
```

Ahí aparecen las tools.

---

# 5. Concepto 2 — TOOL

## Definición

> **Tool:** capacidad ejecutable, expuesta al modelo mediante un contrato estructurado, que permite consultar información o provocar una acción fuera de la generación normal del modelo.

Ejemplos futuros de nuestro agente:

```text
search_knowledge_base
get_customer_profile
create_support_ticket
schedule_appointment
send_email
query_database
retrieve_document
```

En Claude Code ya estás utilizando tools, aunque no hayas programado ninguna.

Por ejemplo:

```text
Read
Edit
Bash
Glob
Grep
WebSearch
WebFetch
Agent
MCP tools
```

Claude Code documenta que son precisamente las tools las que convierten al modelo en algo capaz de interactuar con el proyecto. citeturn403331search2

---

# 6. Una tool tiene un contrato

Conceptualmente:

```text
TOOL
├── name
├── description
├── input schema
├── implementación
└── output
```

Por ejemplo:

```text
name:
get_order_status

description:
Obtiene el estado actual de un pedido.

inputSchema:
{
  "order_id": "string"
}

output:
{
  "status": "shipped",
  "estimated_delivery": "..."
}
```

Esto importa muchísimo porque el modelo no ve tu código como lo ve un programador.

Ve principalmente algo parecido a:

```text
Nombre:
get_order_status

Qué hace:
Obtiene el estado de un pedido.

Argumentos:
order_id: string
```

A partir de ese contrato decide si usarla.

Anthropic insiste en que las herramientas deben tener funciones bien diferenciadas, descripciones claras, parámetros inequívocos y resultados eficientes en tokens; herramientas ambiguas o demasiado solapadas dificultan las decisiones del agente. citeturn892766search2turn892766search6

---

# 7. La tool no tiene que ser una API

Una tool puede envolver prácticamente cualquier capacidad controlada:

```text
función Python
API REST
consulta SQL
filesystem
motor de búsqueda
servicio externo
shell
servicio MCP
código propio
sistema empresarial
```

Ejemplo:

```python
@tool
def calculate_total(price: float, quantity: int) -> float:
    return price * quantity
```

O conceptualmente:

```text
Tool:
search_products

↓ ejecuta

GET /products/search?q=...
```

---

# 8. TOOL CALL vs TOOL EXECUTION

Esta diferencia debe quedarte grabada:

```text
MODELO
genera:
tool_call

        ↓

HARNESS/RUNTIME
valida y ejecuta

        ↓

TOOL

        ↓

tool_result

        ↓

HARNESS
lo agrega al estado/contexto

        ↓

MODELO
lo interpreta
```

LangChain documenta exactamente este ciclo. citeturn209538search0turn209538search5

---

# 9. ¿Qué ocurre cuando añadimos una tool?

Pasamos de:

```text
Usuario
   ↓
Modelo
   ↓
Respuesta
```

a:

```text
Usuario
   ↓
Modelo
   ↓
"Necesito tool X"
   ↓
runtime ejecuta X
   ↓
resultado
   ↓
Modelo
   ↓
Respuesta
```

Y ahora estamos acercándonos a un agente.

---

# 10. Concepto 3 — AGENTE

No existe una única definición universal de “agent”.

Anthropic reconoce explícitamente esa ambigüedad, pero hace una distinción muy útil:

- **workflow:** LLM y tools siguen rutas predefinidas por código;
- **agent:** el LLM decide dinámicamente qué proceso y qué herramientas utilizar. citeturn892766search1

LangChain usa una definición equivalente: un agente combina modelos y tools y ejecuta tools en un loop hasta alcanzar una condición de parada. citeturn403331search8

Para nuestro proyecto adoptaremos:

> **Agente:** sistema en el que un modelo participa repetidamente en un ciclo de decisión, puede seleccionar herramientas y adaptar los siguientes pasos según resultados intermedios hasta alcanzar un objetivo o una condición de parada.

---

# 11. El agent loop

El núcleo más sencillo puede visualizarse así:

```text
              ┌───────────────────┐
              │      USUARIO      │
              └─────────┬─────────┘
                        │
                        ▼
              ┌───────────────────┐
              │      CONTEXTO     │
              └─────────┬─────────┘
                        │
                        ▼
              ┌───────────────────┐
              │      MODELO       │
              └─────────┬─────────┘
                        │
             ┌──────────┴──────────┐
             │                     │
             ▼                     ▼
       RESPUESTA FINAL         TOOL CALL
                                     │
                                     ▼
                               EJECUTAR TOOL
                                     │
                                     ▼
                               TOOL RESULT
                                     │
                                     ▼
                            actualizar estado/
                                contexto
                                     │
                                     └───────────┐
                                                 │
                                                 ▼
                                               MODELO
```

Pseudocódigo conceptual:

```python
while not finished:

    model_output = model(context)

    if model_output.is_tool_call:
        result = execute_tool(model_output.tool)
        context.add(result)

    else:
        return model_output
```

Ese pequeño `while` es una de las ideas fundamentales de toda la ingeniería de agentes.

Anthropic llega a resumir el agente moderno como un LLM utilizando herramientas autónomamente dentro de un loop. citeturn892766search2

---

# 12. Entonces Claude Code es un agente

Sí.

Pero más precisamente:

```text
Claude Code
    =
aplicación/harness agentic

Claude
    =
modelo utilizado dentro del harness
```

Claude Code te ofrece:

```text
loop
tools
filesystem
terminal
Git
permisos
context management
memory
plan mode
subagents
skills
MCP
hooks
verification
```

La documentación oficial lo denomina explícitamente un **agentic assistant** y dice que Claude Code constituye el *agentic harness* alrededor de Claude. citeturn403331search2

---

# 13. Concepto 4 — COPILOTO

Aquí existe mucha confusión porque “copilot” no es una categoría arquitectónica precisa.

Es principalmente una **relación de interacción con el humano**:

> **Copiloto:** sistema de IA cuyo papel principal es asistir a una persona que conserva supervisión y dirección sobre el trabajo.

Puede ser:

```text
autocompletado
chat
editor asistido
agente
reviewer
planner
```

El ejemplo perfecto es GitHub Copilot. Su propia documentación tiene:

```text
Ask mode
Edit mode
Agent mode
Plan mode
```

Es decir, el mismo producto llamado “Copilot” incluye experiencias no agentic y agentic. citeturn892766search4

Por eso:

```text
copiloto
    ≠
agente
```

aunque:

```text
un copiloto PUEDE contener un agente.
```

Claude Code también puede ocupar el rol de copiloto para nosotros porque:

```text
nosotros dirigimos
Claude Code ejecuta
nosotros revisamos
```

Pero arquitectónicamente Claude Code es un sistema agentic.

---

# 14. Diferencia práctica

Una sugerencia inline:

```text
function calculate() {
    ...
```

es asistencia tipo copiloto.

Pero:

```text
"Investiga por qué falla este test,
encuentra los archivos relacionados,
modifica lo necesario,
ejecuta la suite y verifica la solución."
```

activa comportamiento agentic.

La diferencia está mucho menos en el marketing del producto y mucho más en:

```text
quién decide los pasos
+
quién selecciona las tools
+
si existe un loop adaptativo
```

---

# 15. Concepto 5 — HARNESS

Este es uno de los conceptos centrales del Módulo 1.

En julio de 2026 Microsoft publicó una formulación particularmente clara:

> un harness proporciona el loop, planificación, memoria, gestión de contexto, aprobaciones y telemetría que convierten un modelo en un agente capaz de actuar. citeturn143219search1

Claude Code utiliza el mismo vocabulario para describirse a sí mismo. citeturn403331search2

## Definición que adoptaremos

> **Agent harness:** runtime y plano de control que rodea al modelo, administra el ciclo agentic y conecta razonamiento con herramientas, estado, contexto, memoria, permisos, ejecución y verificación.

---

# 16. ¿Qué suele contener un harness?

Conceptualmente:

```text
HARNESS
│
├── Agent loop
│
├── Model adapter
│
├── Tool registry
│
├── Tool executor
│
├── Context builder
│
├── State management
│
├── Memory
│
├── Compaction
│
├── Planning
│
├── Permissions
│
├── Human approval
│
├── Retry/error handling
│
├── Guardrails
│
├── Subagents
│
├── Observability
│
├── Evaluation hooks
│
└── Stop conditions
```

No todos los harness contienen todo eso.

Un harness mínimo podría ser únicamente:

```text
while:
 model
 tool
 model
```

Uno profesional añade progresivamente controles.

Microsoft Agent Framework, por ejemplo, incluye actualmente planificación, listas de tareas, compaction, file memory, file access y aprobación de tools dentro de su harness. citeturn143219search8

---

# 17. Por qué el harness importa

Porque el mismo modelo puede estar dentro de sistemas radicalmente diferentes.

Por ejemplo:

```text
                 Claude
                   │
        ┌──────────┼──────────┐
        ▼          ▼          ▼
   Chat simple  Claude Code   otro harness
```

El modelo puede ser similar, pero cambia:

```text
qué archivos puede leer
qué tools conoce
qué permisos tiene
cómo conserva estado
cómo valida resultados
cómo compacta contexto
qué instrucciones recibe
cómo maneja errores
qué observabilidad existe
```

Por eso no debemos evaluar un modelo aislado como si fuese todo el sistema.

Pero recuerda la auditoría del Paso 2: **no tenemos evidencia para afirmar que el harness siempre pesa más que el modelo**. Esa jerarquización quedó rechazada en nuestro propio repositorio. fileciteturn8file0L2-L2

---

# 18. Concepto 6 — SCAFFOLDING

Aquí tenemos que ser especialmente rigurosos.

No existe una diferenciación universal y normalizada entre:

```text
harness
scaffolding
```

Microsoft, de hecho, dice literalmente que el harness es el **scaffolding** que convierte un language model en un agent. citeturn143219search1

Por tanto sería incorrecto enseñarte:

> “La industria define oficialmente harness como X y scaffolding como Y.”

No existe tal estándar universal.

## Para evitar ambigüedad adoptaremos una convención interna

### Scaffolding

Lo usaremos para hablar de las **piezas estructurales/configurables** alrededor del modelo:

```text
instructions
prompts
tool schemas
skills
memory layout
rules
subagent definitions
middleware
policies
docs
context strategy
```

### Harness

Lo usaremos para el **runtime que opera esas piezas**:

```text
loop
ejecución
orquestación
estado
tool dispatch
permissions
retry
context assembly
telemetry
```

Visualmente:

```text
                 SCAFFOLDING
      ┌──────────────────────────────┐
      │ instructions                 │
      │ tools                        │
      │ skills                       │
      │ memory strategy              │
      │ policies                     │
      │ subagent definitions         │
      │ context rules                │
      └──────────────┬───────────────┘
                     │
                     ▼
              ┌──────────────┐
              │   HARNESS    │
              │   runtime    │
              └──────┬───────┘
                     │
                     ▼
                  MODEL
```

Repito: **esta separación será una `PROJECT_CONVENTION`**, no una verdad científica.

---

# 19. Framework ≠ harness ≠ runtime

Este concepto será vital cuando lleguemos a LangChain.

La documentación actual del ecosistema LangChain distingue expresamente:

```text
Deep Agents
= agent harness

LangChain
= agent framework

LangGraph
= orchestration runtime

LangSmith
= tracing/evaluation/prompts/deployment platform
```

citeturn403331search7

Eso nos permite entender por qué decir:

> “Voy a usar LangChain”

todavía no describe una arquitectura.

---

# 20. Qué es un framework

Un framework te proporciona abstracciones y componentes reutilizables.

LangChain ofrece principalmente:

```text
models
tools
agents
middleware
messages
structured output
integrations
context engineering abstractions
```

citeturn403331search3turn209538search1

Pero el framework no es necesariamente el proceso concreto que estará ejecutando nuestro producto.

---

# 21. Qué es un runtime

Un runtime es la infraestructura donde vive y avanza la ejecución.

LangGraph está diseñado como runtime/orquestador para:

```text
state
durable execution
streaming
persistence
human-in-the-loop
long-running agents
```

citeturn403331search7

---

# 22. Qué es Deep Agents

Actualmente LangChain lo describe como un **agent harness** construido encima de LangGraph y LangChain, con capacidades como:

```text
planning
subagents
filesystem
context management
```

citeturn403331search7

### Pero atención

Esto NO significa:

```text
"Nuestro proyecto usará Deep Agents."
```

Todavía no hemos decidido eso.

El Módulo 4 determinará si nuestro problema necesita:

```text
LangChain create_agent

o

LangGraph personalizado

o

Deep Agents

o

una combinación
```

El concepto viene antes que la tecnología.

---

# 23. Concepto 7 — CONTEXTO

Esta palabra suele utilizarse de manera demasiado amplia.

## Definición rigurosa

Anthropic:

> contexto = conjunto de tokens incluidos cuando se realiza la inferencia del LLM. citeturn892766search2

Para nuestro proyecto:

> **Contexto:** información efectivamente disponible para el modelo durante una invocación concreta.

La palabra clave es:

**efectivamente disponible.**

---

# 24. Tener acceso ≠ estar en contexto

Supongamos que nuestro repositorio futuro tenga:

```text
10.000 archivos
```

Claude Code puede tener permiso de filesystem sobre los 10.000.

Eso significa:

```text
ACCESIBLES
```

No:

```text
10.000 archivos ya dentro del contexto.
```

Cuando Claude usa:

```text
Read backend/auth/service.py
```

ese contenido entra al contexto.

Claude Code documenta precisamente que cada lectura añade contenido a la ventana. citeturn403331search4

---

# 25. El contexto de Claude Code

Puede contener, entre otras cosas:

```text
system instructions
tu prompt actual
historial de conversación
respuestas anteriores
archivos leídos
resultados de Bash
resultados de Git
CLAUDE.md
auto memory
reglas cargadas
skills cargadas
tool definitions
MCP tool definitions
resúmenes de subagents
```

citeturn403331search0turn403331search4

Observa algo:

```text
Repositorio
    ≠
contexto

Internet
    ≠
contexto

Base de datos
    ≠
contexto

Memoria almacenada
    ≠
contexto
```

Solo entran al contexto cuando algún mecanismo las selecciona y las introduce.

---

# 26. Fórmula mental del contexto

Para nuestro producto podemos pensar:

```text
Context_t =
    system_instructions
  + current_user_message
  + selected_conversation_history
  + selected_state
  + recalled_memory
  + retrieved_knowledge
  + available_tool_definitions
  + relevant_tool_results
  + runtime_metadata
```

No es una fórmula matemática del proveedor.

Es nuestro modelo mental.

El subíndice:

```text
t
```

significa que el contexto cambia en cada paso.

---

# 27. Ejemplo

Turno inicial:

```text
Context₀

system prompt
+
"¿Dónde está mi pedido?"
+
tool definitions
```

Modelo:

```text
Necesito order_id.
```

Usuario:

```text
ABC123
```

Ahora:

```text
Context₁

system prompt
+
pregunta original
+
respuesta del agente
+
ABC123
+
tools
```

Modelo solicita:

```text
get_order("ABC123")
```

Resultado:

```text
shipped
```

Ahora:

```text
Context₂

...
+
tool call
+
tool result
```

Y solo entonces el modelo puede contestar correctamente.

---

# 28. Context engineering

No significa:

```text
meter todo
```

Significa:

```text
seleccionar lo adecuado
en el momento adecuado
en el formato adecuado
```

Anthropic lo describe como curar el conjunto óptimo de tokens durante la inferencia y recomienda *just-in-time context*: mantener referencias ligeras y cargar datos progresivamente cuando el agente los necesita. citeturn892766search2

LangChain lleva esa idea a tres planos:

| Plano | Qué controla |
|---|---|
| Model context | lo que ve el modelo |
| Tool context | lo que las tools pueden leer/escribir |
| Life-cycle context | lo que ocurre entre pasos: summarization, guardrails, logging, etc. |

citeturn209538search1

---

# 29. Concepto 8 — MEMORIA

Aquí aparece otra confusión muy común:

```text
memoria = contexto
```

No.

## Definición que adoptaremos

> **Memoria:** información persistida para poder recuperarse y utilizarse posteriormente.

Una memoria guardada en PostgreSQL que nunca recuperamos no está dentro del contexto del modelo.

Por tanto:

```text
MEMORIA
   ↓ retrieval
CONTEXTO
   ↓
MODELO
```

---

# 30. Memoria de corto plazo

En nuestro futuro agente conversacional:

```text
Usuario:
Mi nombre es Laura.

Turno 2:
¿Cuál es mi nombre?

Agente:
Laura.
```

Para lograrlo debemos conservar estado de la conversación.

LangChain llama esto **short-term memory** y la asocia al thread. Se almacena dentro del estado del agente y puede persistirse mediante un `checkpointer`. citeturn209538search2turn209538search4

Conceptualmente:

```text
thread_abc
├── messages
├── state
├── tool results necesarios
└── otros datos conversacionales
```

---

# 31. Memoria de largo plazo

Ahora:

```text
Conversación lunes:
"Prefiero respuestas en español."

Conversación viernes nueva:
"Explícame este documento."
```

El agente podría recuperar:

```text
preferencia:
language = es
```

aunque sea otro thread.

LangChain define long-term memory precisamente como información persistente **a través de conversaciones y threads**, almacenada mediante stores. citeturn403331search5

---

# 32. La distinción que utilizaremos

```text
SHORT-TERM MEMORY
scope:
thread/conversación

ejemplo:
historial actual


LONG-TERM MEMORY
scope:
usuario/aplicación entre conversaciones

ejemplo:
preferencias persistentes
```

Más adelante probablemente tendremos:

```text
PostgreSQL
```

como una de las posibilidades de persistencia, pero no lo decidiremos en este paso.

---

# 33. STATE ≠ MEMORY exactamente

El `state` es:

> datos estructurados del estado actual de ejecución.

Por ejemplo:

```json
{
  "authenticated": true,
  "conversation_id": "...",
  "current_intent": "...",
  "messages": []
}
```

Cuando ese estado se persiste para reutilizarlo, parte puede actuar como memoria.

LangChain actualmente trata `State` como short-term memory dentro del agente, pero conceptualmente es útil mantener la distinción porque no todo dato de runtime es algo que queramos “recordar”. citeturn209538search1turn209538search3

---

# 34. RAG ≠ memoria

Esto será fundamental para nuestro futuro agente.

Supón que tenemos:

```text
manuales
políticas
documentación
PDF
FAQ
catálogo
```

Los indexamos y recuperamos fragmentos relevantes mediante RAG.

Eso es:

```text
KNOWLEDGE
```

no necesariamente:

```text
MEMORY
```

Ejemplo:

```text
Manual:
"La garantía es de 12 meses."

        ↓ retrieval

contexto del modelo
```

Eso es conocimiento recuperado.

En cambio:

```text
"Este usuario ya reportó el televisor
con serial XYZ la semana pasada."
```

podría ser memoria o dato operacional.

Esta distinción nos evitará crear más adelante una arquitectura donde todo sea llamado incorrectamente “RAG”.

---

# 35. Claude Code también tiene memoria

Pero **no confundiremos esa memoria con la memoria del producto**.

Claude Code documenta actualmente dos mecanismos entre sesiones:

```text
CLAUDE.md
    =
instrucciones persistentes escritas por nosotros

Auto memory
    =
notas que Claude guarda sobre aprendizajes/patrones
```

Cada nueva sesión comienza con una ventana nueva. citeturn403331search0

El `MEMORY.md` automático tiene un comportamiento concreto: las primeras 200 líneas o 25 KB, lo que ocurra primero, se cargan al comenzar la conversación; los archivos temáticos adicionales se consultan bajo demanda. citeturn403331search0

---

# 36. Tenemos, por tanto, DOS mundos diferentes

## Mundo A — Memoria del agente desarrollador

```text
Claude Code
├── CLAUDE.md
├── auto memory
├── rules
├── skills
└── sesión de desarrollo
```

## Mundo B — Memoria de nuestro producto

```text
Conversational AI Agent
├── short-term conversation state
├── checkpointer
├── long-term memory store
└── customer/application memory
```

Nunca deben mezclarse.

Una preferencia que Claude Code recuerde sobre cómo programamos **no puede convertirse accidentalmente en una memoria de los usuarios finales**.

---

# 37. Concepto 9 — PROMPT

Ahora llegamos al componente más visible.

## Definición

> **Prompt:** instrucción o entrada comunicada al modelo para orientar su comportamiento o resolver una tarea.

Ejemplo:

```text
Analiza este error y encuentra su causa.
```

Pero existe más de una clase de mensaje.

Podemos tener:

```text
system instructions
developer instructions
user message
tool results
assistant history
```

No conviene llamar “prompt” indistintamente a todo el contexto.

---

# 38. Prompt ⊂ Contexto

Esta relación debe quedar memorizada:

```text
┌─────────────────────────────────────────┐
│                CONTEXTO                 │
│                                         │
│ system instructions                     │
│                                         │
│  ┌────────────────────────────┐         │
│  │        USER PROMPT         │         │
│  └────────────────────────────┘         │
│                                         │
│ conversation history                    │
│ retrieved knowledge                     │
│ memory recalled                         │
│ tool definitions                        │
│ tool results                            │
│ runtime information                     │
└─────────────────────────────────────────┘
```

Anthropic distingue precisamente prompt engineering de context engineering: el primero optimiza instrucciones; el segundo administra todo lo que llega a la inferencia, incluidos tools, MCP, datos externos e historial. citeturn892766search2

---

# 39. El prompt no debe cargar todo el proyecto

Un prompt como:

```text
Aquí tienes nuestras 150 reglas...
Aquí tienes arquitectura...
Aquí tienes 20 archivos...
Aquí tienes convenciones...
Ahora corrige este typo.
```

es contrario a nuestro diseño.

Lo correcto será:

```text
PROMPT
→ objetivo específico

PERSISTENT CONTEXT
→ normas que siempre importan

RULES
→ instrucciones por área

SKILLS
→ procedimientos bajo demanda

FILES
→ información descubierta just-in-time

TOOLS
→ acciones
```

Eso es precisamente lo que iremos construyendo en los pasos posteriores.

---

# 40. MCP tampoco es una tool

Otro concepto que debemos adelantar porque lo encontraremos más adelante.

MCP es:

```text
PROTOCOLO
```

No:

```text
una tool
```

La especificación MCP consultada distingue tres primitivas del servidor:

```text
Prompts
Resources
Tools
```

citeturn143219search4

## MCP Tool

Capacidad ejecutable:

```text
create_ticket
query_database
send_message
```

## MCP Resource

Información:

```text
file://...
db-schema://...
document://...
```

## MCP Prompt

Plantilla/instrucción reutilizable.

La propia especificación caracteriza:

```text
Prompts   → user-controlled
Resources → application-controlled
Tools     → model-controlled
```

citeturn143219search4

Esto será muy importante en el Paso 13.

---

# 41. Tools y seguridad

El modelo puede decidir:

```text
Quiero ejecutar delete_customer(...)
```

Eso no significa que deba permitírsele.

El harness debe poder aplicar:

```text
permissions
validation
human approval
sandbox
authorization
audit
```

MCP recomienda explícitamente que las aplicaciones permitan intervención humana para denegar tool invocations sensibles. citeturn143219search10

Por eso:

```text
seguridad crítica
        ≠
"Le dije en el prompt que no lo hiciera"
```

La aplicaremos más adelante mediante controles deterministas.

---

# 42. Relacionemos todos los conceptos

Esta es nuestra arquitectura conceptual general:

```text
                           USUARIO
                              │
                              │ prompt
                              ▼
                    ┌──────────────────┐
                    │     HARNESS      │
                    │                  │
                    │ Context Builder  │◄──── MEMORY
                    │ State Manager    │
                    │ Permissions      │◄──── POLICIES
                    │ Tool Registry    │
                    │ Agent Loop       │
                    │ Verification     │
                    └────────┬─────────┘
                             │
                             │ contexto
                             ▼
                    ┌──────────────────┐
                    │      MODEL       │
                    │                  │
                    │    reasoning     │
                    └───────┬──────────┘
                            │
                  ┌─────────┴─────────┐
                  │                   │
                  ▼                   ▼
             FINAL OUTPUT          TOOL CALL
                                      │
                                      ▼
                              ┌───────────────┐
                              │     TOOL      │
                              └───────┬───────┘
                                      │
                                      ▼
                                  RESULT
                                      │
                                      └─────────────►
                                             nuevo contexto
```

---

# 43. Entonces, ¿qué es realmente un agente?

No es:

```text
modelo
```

Ni simplemente:

```text
modelo + prompt
```

Para nuestro vocabulario:

```text
AGENT
=
comportamiento emergente del loop

MODEL
=
motor de decisión

HARNESS
=
runtime/control del loop

TOOLS
=
capacidades

CONTEXT
=
working information

MEMORY
=
persisted information

PROMPT
=
current instruction/input

SCAFFOLDING
=
estructura/configuración alrededor del sistema
```

---

# 44. Workflow vs Agent

Tenemos que agregar este concepto aunque no aparezca en la lista inicial porque evita uno de los mayores errores arquitectónicos.

## Workflow

El desarrollador fija la ruta:

```text
Step A
 ↓
Step B
 ↓
if X:
   Step C
else:
   Step D
```

El modelo puede participar, pero no determina el flujo principal.

## Agent

El modelo decide:

```text
¿qué tool uso?
¿qué investigo?
¿qué hago después?
¿terminé?
```

Anthropic recomienda workflows cuando el proceso es predecible y agentes cuando se necesita flexibilidad y decisión dinámica. citeturn892766search1

Nuestro producto probablemente terminará siendo **híbrido**:

```text
deterministic workflow
        +
agentic decisions
```

Pero eso se decidirá en planificación, no hoy.

---

# 45. El error de convertir todo en agente

Por ejemplo, esto:

```text
validar email
```

no necesita un LLM que “razone” si el email cumple una regex.

Podemos usar código determinista.

Esto:

```text
"comprende qué necesita el cliente,
decide qué fuente consultar,
recupera información,
pregunta datos faltantes
y decide qué acción corresponde"
```

sí podría justificar agentic behavior.

Anthropic recomienda empezar con la solución más sencilla posible y aumentar complejidad solamente cuando aporte valor, porque los agentes intercambian mayor coste y latencia por flexibilidad. citeturn892766search1

---

# 46. El mapa actual del ecosistema LangChain

Para que desde ahora utilicemos los términos correctamente:

```text
┌──────────────────────────────────────────────┐
│                 LANGSMITH                    │
│ tracing · evals · observability · deploy     │
└──────────────────────────────────────────────┘

┌──────────────────────────────────────────────┐
│                DEEP AGENTS                   │
│ optional batteries-included agent harness    │
└──────────────────────────────────────────────┘

┌──────────────────────────────────────────────┐
│                 LANGCHAIN                    │
│ models · tools · agents · middleware         │
│ integrations · context engineering           │
└──────────────────────────────────────────────┘

┌──────────────────────────────────────────────┐
│                 LANGGRAPH                    │
│ orchestration runtime · state · persistence  │
│ durable execution · HITL · streaming         │
└──────────────────────────────────────────────┘
```

Esta clasificación es la que publica actualmente el propio proyecto LangChain. citeturn403331search3turn403331search7

---

# 47. Pero tenemos DOS agentes diferentes en nuestro proyecto

Esto es crucial.

## Agente 1 — Claude Code

Nos ayuda **a construir** la aplicación.

```text
NOSOTROS
   ↓
Claude Code
   ↓
código/documentación/configuración
```

## Agente 2 — Conversational AI Agent

Es el **producto que construiremos**.

```text
USUARIO FINAL
   ↓
frontend
   ↓
API/backend
   ↓
nuestro agent harness
   ↓
modelo
   ↓
tools / knowledge / memory
```

Claude Code no será automáticamente el runtime del usuario final.

---

# 48. Arquitectura conceptual del sistema de construcción

Hoy estamos aquí:

```text
                         NOSOTROS
                            │
                            │ task prompt
                            ▼
                   ┌──────────────────┐
                   │   CLAUDE CODE    │
                   │     HARNESS      │
                   └────────┬─────────┘
                            │
              ┌─────────────┼─────────────┐
              │             │             │
              ▼             ▼             ▼
            Read           Bash          Git
            Edit         WebSearch      etc.
              │             │
              └──────┬──────┘
                     ▼
                  CONTEXT
                     │
                     ▼
                  CLAUDE
                   MODEL
```

La documentación oficial de Claude Code confirma esta arquitectura de modelo + tools + harness. citeturn403331search2

---

# 49. Arquitectura conceptual del futuro producto

Todavía abstracta:

```text
                      END USER
                          │
                          ▼
                       FRONTEND
                          │
                          ▼
                         API
                          │
                          ▼
                 ┌────────────────┐
                 │ AGENT HARNESS  │
                 │                │
                 │ context        │
                 │ state          │
                 │ loop           │
                 │ policies       │
                 │ tools          │
                 │ memory         │
                 └───────┬────────┘
                         │
                         ▼
                       MODEL
                         │
                 ┌───────┴─────────┐
                 │                 │
                 ▼                 ▼
             TOOL CALL         FINAL ANSWER
                 │
                 ▼
      ┌─────────────────────────┐
      │ APIs · RAG · DB · etc.  │
      └─────────────────────────┘
```

No hemos elegido todavía:

```text
modelo
database
vector store
frontend framework
backend framework
provider
auth
deployment
Deep Agents vs create_agent vs LangGraph
```

Eso es intencional.

---

# 50. Diez invariantes que registraremos

Estas sí serán reglas conceptuales del proyecto:

```text
I-01
El modelo no se considera equivalente al agente.

I-02
Una solicitud de tool del modelo no equivale
a la ejecución real de la tool.

I-03
Las acciones con efectos externos pertenecen
al runtime/harness y sus controles.

I-04
Información accesible no significa información
presente en contexto.

I-05
La memoria almacenada no influye al modelo
hasta que es recuperada/incluida en contexto.

I-06
El prompt es parte del contexto, no todo el contexto.

I-07
"Copilot" describe principalmente un rol/producto
de asistencia, no una arquitectura técnica universal.

I-08
Workflow y agent se distinguen según si la ruta
está predefinida o es decidida dinámicamente.

I-09
Harness y scaffolding son términos parcialmente
solapados; nuestra separación será una convención
interna explícita.

I-10
La memoria de Claude Code y la memoria del producto
son sistemas diferentes y nunca deben mezclarse.
```

---

# 51. Ahora vamos a poner todo esto en práctica con Claude Code

No quiero que estos conceptos queden como teoría.

Crearemos esta documentación:

```text
docs/foundations/module-01/
├── README.md
├── 01-conceptual-model.md
├── 02-agent-loop-and-harness.md
├── 03-context-memory-prompt.md
├── 04-builder-vs-product-boundaries.md
├── 05-practical-lab.md
└── sources.md
```

A diferencia de `CLAUDE.md`, estos documentos **no se cargan automáticamente en cada sesión**, así que pueden ser exhaustivos.

---

# 52. Fase A — Preparar Git

Desde la raíz del proyecto:

```bash
git switch main
git pull --ff-only
git status
```

Comprueba el último commit:

```bash
git log -1 --oneline
```

Deberías ver algo relacionado con:

```text
3226146 docs: audit module 1 claims and evidence (#1)
```

Yo ya verifiqué el commit completo en GitHub:

```text
3226146a2ecb7a8dc903fbfc20651cc7f3ccd377
```

Ahora revisa herramientas:

```bash
mise run versions
```

Tu `mise.toml` actualmente registra Node 24.19.0, Python 3.14.6, GitHub CLI 2.97.0 y una baseline para Claude Code 2.1.222, además de Git, Docker y Compose. fileciteturn10file0L2-L2

No uses un eventual cambio de versión autoactualizada de Claude como razón para detener este paso; el propio archivo indica que Claude Code se autoactualiza y que esa cifra es una baseline.

---

# 53. Crea la rama

```bash
git switch -c docs/module-01-conceptual-foundations
```

Comprueba:

```bash
git branch --show-current
git status
```

Esperamos:

```text
docs/module-01-conceptual-foundations
```

y working tree limpio.

---

# 54. Fase B — Laboratorio: mirar el harness desde dentro

Abre:

```bash
claude
```

No uses `/init`.

No crearemos todavía archivos de instrucciones.

Ejecuta:

```text
/status
```

Luego:

```text
/context
```

Y:

```text
/memory
```

### En `/memory`

Solo observa.

No agregues ni elimines nada.

La documentación actual indica que `/memory` permite inspeccionar `CLAUDE.md`, reglas y auto memory cargados para el proyecto. citeturn403331search0

---

# 55. Primer experimento — distinguir acceso de contexto

Dentro de Claude Code pega:

```text
Trabaja exclusivamente en modo de solo lectura.

No crees, edites, elimines ni renombres archivos.
No instales dependencias.
No cambies configuración.
No escribas memoria.
No hagas commits.

Quiero observar tu agentic loop.

1. Indica primero, sin leer archivos nuevos, qué información del
   repositorio ya está efectivamente disponible en tu contexto actual.

2. Distingue explícitamente entre:
   - información actualmente en contexto;
   - información a la que puedes acceder mediante tools pero que todavía
     no has leído.

3. Después utiliza únicamente las tools mínimas necesarias para verificar:
   - la rama actual;
   - el último commit;
   - el título de README.md;
   - cuántos claims registra
     docs/research/module-01/README.md.

4. Para cada acción indica:
   - qué decisión requirió el modelo;
   - qué tool ejecutó el harness;
   - qué resultado volvió al contexto.

5. Al final representa esta sesión mediante:

   PROMPT
      ↓
   MODEL DECISION
      ↓
   TOOL CALL
      ↓
   TOOL EXECUTION
      ↓
   TOOL RESULT
      ↓
   UPDATED CONTEXT
      ↓
   MODEL RESPONSE

No modifiques nada.
```

---

# 56. Qué tienes que observar

No te centres únicamente en la respuesta.

Mira la interfaz.

Deberías observar acciones semejantes a:

```text
Read(...)
Bash(...)
```

Es decir:

```text
Claude/model
    ↓ decide
"Bash git branch..."
    ↓
Claude Code harness
    ↓ ejecuta
git branch...
    ↓
stdout
    ↓
vuelve al modelo
```

Eso es el agent loop real.

---

# 57. Ejecuta `/context` otra vez

Después del experimento:

```text
/context
```

Compara con el estado anterior.

El objetivo conceptual es comprobar:

```text
ANTES
no había leído X

DESPUÉS
X entró mediante tool result/file read
```

Claude Code documenta que precisamente las lecturas, respuestas y resultados van ocupando la ventana. citeturn403331search4

---

# 58. Segundo experimento — memoria vs contexto

Pega:

```text
Solo lectura.

Explícame, basándote exclusivamente en el estado observable de esta
sesión, la diferencia entre:

1. lo que recuerdas porque está en el historial de esta conversación;
2. lo que proviene de auto memory;
3. lo que provendría de CLAUDE.md si existiera;
4. lo que aprendiste leyendo archivos mediante tools;
5. información del repositorio que aún no has leído.

No escribas memoria.
No modifiques archivos.

Si algo no puede determinarse con certeza desde /memory o /context,
indícalo como desconocido; no lo infieras.
```

Esto convierte la teoría en una observación práctica.

---

# 59. Fase C — Plan Mode para documentar los fundamentos

Cambia a Plan Mode.

En Claude Code normalmente puedes alternarlo con:

```text
Shift + Tab
```

hasta que aparezca Plan Mode.

Ahora pega:

```text
Trabaja exclusivamente en Plan Mode.

NO crees ni edites archivos.
NO instales dependencias.
NO generes código de aplicación.
NO crees CLAUDE.md.
NO crees AGENTS.md.
NO crees rules, skills, hooks, subagents ni MCP.
NO cambies mise.toml.
NO modifiques la auditoría existente.
NO uses información posterior al 7 de agosto de 2026.

OBJETIVO

Planificar la documentación conceptual del Paso 3 del Módulo 1
para este repositorio.

Debes estudiar primero:

- README.md
- mise.toml
- docs/research/module-01/README.md
- docs/research/module-01/methodology.md
- docs/research/module-01/project-implications.md

y respetar todas las conclusiones y limitaciones de la auditoría.

Después consulta fuentes primarias/oficiales actuales necesarias para
verificar los conceptos hasta 2026-08-07.

FUENTES PRIORITARIAS

- Claude Code:
  - How Claude Code works
  - Memory
  - Context window

- Anthropic:
  - Building effective agents
  - Effective context engineering for AI agents
  - Writing effective tools for AI agents

- LangChain:
  - Models
  - Tools
  - Agents
  - Context engineering
  - Short-term memory
  - Long-term memory
  - LangGraph overview

- Model Context Protocol:
  - Architecture
  - Server primitives
  - Tools
  - Resources
  - Prompts

- OpenAI:
  - Harness engineering, febrero de 2026

- Microsoft Agent Framework:
  - Agent Harness documentation/publications de junio-julio de 2026

Puedes usar papers fundacionales como ReAct o Toolformer únicamente
para contexto histórico cuando aporten algo que las fuentes actuales
no expliquen.

ARTEFACTOS A PLANIFICAR

Crear exclusivamente:

docs/foundations/module-01/README.md
docs/foundations/module-01/01-conceptual-model.md
docs/foundations/module-01/02-agent-loop-and-harness.md
docs/foundations/module-01/03-context-memory-prompt.md
docs/foundations/module-01/04-builder-vs-product-boundaries.md
docs/foundations/module-01/05-practical-lab.md
docs/foundations/module-01/sources.md

REQUISITOS CONCEPTUALES

Debes definir rigurosamente y diferenciar:

- model
- copilot
- agent
- workflow
- harness
- scaffolding
- framework
- runtime
- tool
- tool call
- tool execution
- context
- context window
- context engineering
- state
- short-term memory
- long-term memory
- persistent instructions
- prompt
- system instructions
- retrieved knowledge
- RAG
- MCP tool
- MCP resource
- MCP prompt

IMPORTANTE

No presentes como estándar una distinción harness/scaffolding que
no existe universalmente.

Registra explícitamente como PROJECT_CONVENTION:

scaffolding =
componentes estructurales/configurables que rodean al modelo.

harness =
runtime/plano de control que ejecuta y coordina esas piezas.

Debes explicar que la literatura a menudo solapa ambos términos.

También debes distinguir claramente:

Claude Code como agente/harness de DESARROLLO

vs

el conversational AI agent que será el PRODUCTO.

Nunca mezcles sus:
- memorias;
- prompts;
- tools;
- usuarios;
- permisos;
- runtime;
- observabilidad.

INVARIANTES

Incluye como mínimo:

I-01 modelo != agente
I-02 tool call != tool execution
I-03 acciones con efectos pertenecen al runtime/harness
I-04 acceso a información != información en contexto
I-05 memoria almacenada != contexto hasta recuperarla
I-06 prompt es subconjunto del contexto
I-07 copilot no es una arquitectura agentic universal
I-08 workflow != agent
I-09 harness/scaffolding es una distinción interna documentada
I-10 memoria de Claude Code != memoria del producto

LANGCHAIN

Documenta la separación actual:

- LangChain = agent framework
- LangGraph = orchestration runtime
- Deep Agents = agent harness
- LangSmith = tracing/evaluation/prompts/deployment platform

Pero NO selecciones todavía Deep Agents ni ninguna arquitectura.

No instales el ecosistema LangChain en este paso.

FUENTES

sources.md debe registrar para cada fuente:

- source_id
- title
- organization/authors
- source_type
- publication_date cuando exista
- retrieved_at = 2026-08-07
- canonical_url
- concepts_supported
- limitations
- whether it is a living document

Cada afirmación factual importante debe apuntar a una fuente.
Distingue vendor documentation de evidencia experimental.

SALIDA

Devuélveme únicamente:

1. archivos que leíste;
2. fuentes que verificaste;
3. estructura detallada de los siete documentos;
4. conceptos cubiertos por cada uno;
5. riesgos de confusión conceptual;
6. criterios de validación;
7. lista explícita de archivos que NO modificarás.

NO ejecutes el plan.
```

---

# 60. Revisa el plan antes de aprobarlo

Comprueba estas condiciones:

```text
[ ] Solo propone los siete archivos permitidos.
[ ] No crea CLAUDE.md.
[ ] No crea AGENTS.md.
[ ] No instala LangChain.
[ ] No selecciona todavía modelo.
[ ] No selecciona framework frontend/backend.
[ ] No selecciona base de datos.
[ ] Distingue model de agent.
[ ] Distingue tool call de tool execution.
[ ] Distingue agent de harness.
[ ] Marca harness/scaffolding como convención interna.
[ ] Distingue context de memory.
[ ] Distingue prompt de context.
[ ] Distingue state de long-term memory.
[ ] Distingue RAG de memory.
[ ] Distingue Claude Code del futuro product agent.
[ ] Distingue LangChain/LangGraph/Deep Agents/LangSmith.
[ ] Respeta las conclusiones del Paso 2.
[ ] Usa fuentes primarias.
[ ] No presenta marketing de vendor como evidencia experimental.
[ ] No usa información posterior a 2026-08-07.
```

Si falla alguno, dile:

```text
Corrige el plan sin ejecutarlo.

[describe exactamente el punto que incumplió]

Mantén el alcance exclusivamente en los siete documentos de
docs/foundations/module-01/.
```

---

# 61. Fase D — Ejecutar el plan

Cuando esté perfecto, sal de Plan Mode al modo normal.

Pega:

```text
Ejecuta exactamente el plan aprobado.

ALCANCE ESTRICTO

Crea exclusivamente:

docs/foundations/module-01/README.md
docs/foundations/module-01/01-conceptual-model.md
docs/foundations/module-01/02-agent-loop-and-harness.md
docs/foundations/module-01/03-context-memory-prompt.md
docs/foundations/module-01/04-builder-vs-product-boundaries.md
docs/foundations/module-01/05-practical-lab.md
docs/foundations/module-01/sources.md

No modifiques ningún otro archivo.

NO:

- instales dependencias;
- generes aplicación;
- crees CLAUDE.md;
- crees AGENTS.md;
- crees .claude/;
- crees MCP;
- crees hooks;
- crees skills;
- crees subagents;
- selecciones modelos;
- selecciones infraestructura;
- inventes arquitectura de producto.

CALIDAD

Cada concepto debe incluir cuando aplique:

1. definición operativa;
2. qué responsabilidad posee;
3. qué NO posee;
4. relación con los demás conceptos;
5. ciclo de vida;
6. ejemplo en Claude Code;
7. ejemplo futuro en nuestro producto;
8. error conceptual común;
9. implicación de ingeniería;
10. fuentes.

DIAGRAMAS

Incluye diagramas Markdown/Mermaid o ASCII para:

A. llamada standalone a un modelo;
B. tool-calling loop;
C. agent loop;
D. model vs harness vs tools;
E. context vs memory;
F. Claude Code como builder agent;
G. futuro conversational agent como product agent;
H. LangChain ecosystem layers.

No presentes los diagramas como especificación de arquitectura definitiva
del producto.

05-practical-lab.md

Registra únicamente observaciones que puedas derivar de lo que realmente
ocurrió en esta sesión.

No inventes tool calls ni contenido de /context o /memory.

Distingue:

OBSERVED
DOCUMENTED
PROJECT_CONVENTION
FUTURE_DECISION

INVARIANTES

Registra I-01 a I-10 exactamente y explica la razón de cada uno.

FUENTES

Usa preferentemente documentación oficial y publicaciones primarias.
No copies párrafos extensos.
Parafrasea.
No inventes URL, fecha, versión ni cita.

Para documentación viva indícalo explícitamente.

KNOWLEDGE DATE

verified_through: 2026-08-07

Esto NO modifica el knowledge_cutoff de la auditoría del Paso 2.

VALIDACIÓN FINAL

Antes de terminar:

1. relee los siete documentos;
2. verifica que no existan contradicciones entre ellos;
3. busca TODO/TBD/FIXME/placeholders;
4. verifica que harness/scaffolding figure como PROJECT_CONVENTION;
5. verifica que Claude Code memory y product memory estén separados;
6. verifica que no se haya seleccionado todavía Deep Agents;
7. verifica que ninguna fuente futura a 2026-08-07 se use;
8. ejecuta git diff --check;
9. ejecuta git status --short;
10. informa qué archivos creaste.

No hagas commit.
```

---

# 62. Fase E — Validación desde la terminal

Sal de Claude Code:

```text
/exit
```

Comprueba archivos:

```bash
find docs/foundations/module-01 -maxdepth 1 -type f -print | sort
```

Debe haber exactamente siete.

Después:

```bash
git status --short
```

Esperamos solamente:

```text
?? docs/foundations/module-01/
```

---

# 63. Busca contenido incompleto

```bash
rg -n "TODO|TBD|FIXME|PLACEHOLDER|PENDIENTE|POR COMPLETAR" \
  docs/foundations/module-01
```

Esperamos:

```text
sin resultados
```

---

# 64. Busca términos fundamentales

```bash
rg -n \
  "model|copilot|agent|workflow|harness|scaffolding|tool|context|memory|prompt|LangChain|LangGraph|Deep Agents|LangSmith" \
  docs/foundations/module-01
```

Queremos comprobar cobertura, no contar ocurrencias.

---

# 65. Verifica nuestra convención

```bash
rg -n "PROJECT_CONVENTION|PROJECT CONVENTION" \
  docs/foundations/module-01
```

Debe aparecer claramente alrededor de:

```text
harness
vs
scaffolding
```

---

# 66. Verifica que no se hayan creado prematuramente archivos del harness

```bash
git status --short | \
grep -E 'CLAUDE\.md|AGENTS\.md|\.claude|\.mcp\.json' || true
```

Esperamos:

```text
sin salida
```

---

# 67. Comprueba formato Git

```bash
git diff --check
```

Esperamos:

```text
sin salida
```

---

# 68. Fase F — Reviewer independiente

El mismo agente que escribió la documentación puede defender sus propios errores.

Abre una sesión completamente nueva:

```bash
claude
```

No uses `--resume`.

Pega:

```text
Realiza una revisión adversarial independiente y de SOLO LECTURA.

No modifiques archivos.
No escribas memoria.
No instales nada.
No hagas commit.

Revisa todos los archivos de:

docs/foundations/module-01/

y contrástalos con:

docs/research/module-01/README.md
docs/research/module-01/project-implications.md

Verifica fuentes primarias cuando sea necesario.

Busca específicamente estos errores:

1. modelo y agente tratados como equivalentes;
2. tool call confundido con tool execution;
3. tool confundida con MCP;
4. copilot presentado como arquitectura formal;
5. agent y workflow confundidos;
6. harness y agent tratados como sinónimos;
7. harness/scaffolding presentado como diferencia universal;
8. framework, runtime y harness confundidos;
9. contexto confundido con todo lo accesible;
10. memoria confundida con contexto;
11. state confundido con long-term memory;
12. RAG confundido con memory;
13. prompt confundido con context completo;
14. Claude Code memory confundida con product memory;
15. CLAUDE.md descrito como product system prompt;
16. el modelo descrito como ejecutor directo de side effects;
17. una tool sin runtime/harness executor;
18. LangChain confundido con LangGraph;
19. Deep Agents seleccionado prematuramente;
20. LangSmith presentado como agent runtime;
21. una decisión futura presentada como arquitectura aceptada;
22. vendor guidance presentada como evidencia experimental;
23. afirmaciones que contradigan la auditoría del Paso 2;
24. información posterior a 2026-08-07;
25. URLs, fechas o citas que no puedan verificarse.

CLASIFICA LOS HALLAZGOS:

BLOCKER
MAJOR
MINOR
NO ISSUE

Para cada BLOCKER o MAJOR:

- archivo;
- sección;
- afirmación problemática;
- por qué es incorrecta;
- evidencia;
- corrección mínima propuesta.

No edites nada.
```

---

# 69. Corrige solo hallazgos reales

Si existen `BLOCKER` o `MAJOR`, abre la sesión de implementación o una nueva y pega:

```text
Aplica exclusivamente estas correcciones verificadas:

[pegar findings]

No amplíes el alcance.
No cambies arquitectura.
No modifiques archivos fuera de docs/foundations/module-01/.
No introduzcas contenido nuevo que no sea necesario para resolver
los findings.

Después ejecuta:

git diff --check
git status --short

No hagas commit.
```

---

# 70. Revisión manual final

Ejecuta:

```bash
git diff --stat
git diff --check
git status --short
```

Después lee especialmente:

```bash
less docs/foundations/module-01/04-builder-vs-product-boundaries.md
```

Ese documento será crítico porque debe impedir esta contaminación futura:

```text
Claude Code development memory
         ↓ ✗
product user memory
```

y esta otra:

```text
Claude Code CLAUDE.md
         ↓ ✗
runtime system prompt del producto
```

---

# 71. Definition of Done del Paso 3

Antes del commit debemos poder marcar:

```text
[ ] Modelo está definido independientemente del agente.
[ ] Tool call está separado de tool execution.
[ ] Agent está explicado mediante un loop.
[ ] Workflow está separado de agent.
[ ] Copilot figura como rol/product experience, no arquitectura universal.
[ ] Harness figura como runtime/plano de control.
[ ] Scaffolding figura como término solapado con harness.
[ ] La separación harness/scaffolding está marcada PROJECT_CONVENTION.
[ ] Contexto significa información efectivamente presentada a la inferencia.
[ ] Acceso y contexto están separados.
[ ] Memoria y contexto están separados.
[ ] Short-term y long-term memory están separados.
[ ] State y memory están relacionados pero no confundidos.
[ ] RAG y memory están separados.
[ ] Prompt aparece como parte del contexto.
[ ] MCP tool/resource/prompt están diferenciados.
[ ] LangChain/LangGraph/Deep Agents/LangSmith están diferenciados.
[ ] Claude Code está separado del futuro product agent.
[ ] Sus memorias están separadas.
[ ] Sus prompts están separados.
[ ] Sus tools están separadas.
[ ] No se ha seleccionado todavía arquitectura definitiva.
[ ] No se instalaron dependencias.
[ ] No existe CLAUDE.md todavía.
[ ] No existe AGENTS.md todavía.
[ ] No existe .claude/ todavía.
[ ] No hay secretos.
[ ] Reviewer independiente no dejó BLOCKERS.
[ ] git diff --check pasa.
```

---

# 72. Commit

Cuando todo esté correcto:

```bash
git add docs/foundations/module-01
```

Comprueba exactamente qué estás preparando:

```bash
git diff --cached --stat
git diff --cached --check
```

Commit:

```bash
git commit -m "docs: establish agentic system foundations"
```

Push:

```bash
git push -u origin docs/module-01-conceptual-foundations
```

---

# 73. Pull Request

```bash
gh pr create \
  --base main \
  --head docs/module-01-conceptual-foundations \
  --title "docs: establish agentic system foundations" \
  --body "## Summary

Establishes the conceptual foundations used by the project to reason about agentic systems.

Documents and differentiates:

- models
- copilots
- agents and workflows
- harnesses and scaffolding
- frameworks and runtimes
- tools and tool execution
- context and context engineering
- state and memory
- prompts
- RAG and retrieved knowledge
- MCP primitives
- Claude Code as the builder agent versus the future conversational product agent

## Key constraint

The harness/scaffolding distinction is explicitly recorded as a project convention, not an industry-standard taxonomy.

## Scope

Documentation only.

No application code, dependencies, CLAUDE.md, AGENTS.md, rules, skills, hooks, subagents, MCP configuration, model selection, or product architecture were added.

## Verification

- Sources verified through 2026-08-07.
- Existing Module 1 evidence audit respected.
- Independent fresh-context review completed.
- git diff --check passes."
```

Mira el PR:

```bash
gh pr view --web
```

Verifica que el diff solo contenga:

```text
docs/foundations/module-01/
```

---

# 74. Fusionar

Cuando esté correcto:

```bash
gh pr merge --squash --delete-branch
```

Después:

```bash
git switch main
git pull --ff-only
git status
```

Esperamos:

```text
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

---

# Lo más importante que debes haber aprendido

Si solo recuerdas un diagrama de este paso, que sea este:

```text
                           MEMORY
                             │
                             │ retrieve
                             ▼
USER PROMPT ───────► CONTEXT BUILDER
                             │
                             ▼
                           MODEL
                             │
                   ┌─────────┴─────────┐
                   │                   │
             FINAL RESPONSE        TOOL CALL
                                       │
                                       ▼
                                   HARNESS
                                       │
                                  validation
                                  permission
                                  execution
                                       │
                                       ▼
                                      TOOL
                                       │
                                       ▼
                                  TOOL RESULT
                                       │
                                       ▼
                              STATE / CONTEXT
                                       │
                                       └──────► MODEL
```

Y alrededor de todo eso:

```text
SCAFFOLDING
=
instructions + tools + policies + skills +
memory strategy + context strategy + configuration

HARNESS
=
runtime que coordina y ejecuta el sistema
```

con la advertencia:

```text
esa última separación es nuestra convención interna;
la industria utiliza ambos términos de forma parcialmente solapada.
```

El resultado del Paso 3 no es todavía “más código”. Es algo más importante para las etapas siguientes: **ya sabemos exactamente qué estamos construyendo cuando decimos agente y qué pieza será responsable de cada comportamiento**. Eso evitará que más adelante llamemos “memoria” a RAG, “agente” al modelo, “tool” a MCP, “contexto” a todo el repositorio o “LangChain” a toda la arquitectura.

**¿Deseas continuar con el Paso 4 de 16: auditar Claude Code como nuestra herramienta agentic, entender profundamente su harness —modos, permissions, tools, sandbox, checkpoints, context, Plan Mode y ejecución— y definir exactamente cómo lo utilizaremos profesionalmente durante el resto del proyecto?**
